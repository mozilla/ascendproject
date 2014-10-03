---
layout:     post
author:     Tina
title:      "Fixing my first Bug"
date:       2014-09-11
categories: tina
---

The first bug I chose was actually more of a feature request.
It involved adding an '--imgur' flag to firefox's 'screenshot' command in order to instead upload the image to imgur.com.
At least the concept to me was simple: Make it upload to imgur's API.
I had no idea about the code, but being able to understand the concept can be tricky when looking for your first bug.
But with the concept in hand, I dove right in.

One of the comments(link) on the bug mentioned a specific 'screenshot.js' file that needed to be changed.
So I opened it up and immediately felt that first stomach drop as I didn't understand a lick of what was there.
But with some resilience, and the gcli documentation(link), I started to understand the different chunks of code and where I would need to edit them.
After looking at that code and needing some code to plug into it, I began to examine the imgurAPI.

API is really just a fancy term for "text exchange" from what I've gathered so far.
You send a request to a server using some data-object full of request information, and the server then returns a data-object with more/different information in it.
It's just constructed text communicating with other more-different constructed text.
Perhaps that could actually be said about the entirety of IT but I had a bit of an 'Aha!' moment in my research.

To start testing the imgur API, I decided to make a small webapp that can pull a file off your computer and then upload it to imgur.
Turns out the first part can be handled using an input tag with type="file".
It's the uploading part that had me running in circles.
There were a lot of examples that people had using jquery to make an http request and send that off.
But, with the intention to put the code into firefox's jquery-less source I didn't want to pull in jquery for this one small feature.
There had to be another way.

The secret was the FormData() and XMLHttpRequest() objects that are native to the web.
It was perfect!
I found them through some example code that I then adapted for my particular webapp.
My resulting upload() function is:

      function upload(file) {

          if (!file || !file.type.match(/image.*/)) return;

          var fd = new FormData();
          fd.append("image", file);

          var xhr = new XMLHttpRequest();
          xhr.open("POST", "https://api.imgur.com/3/image");
          xhr.onload = function() {
              var myParagraph = document.getElementById("theReturn");
              var myImage = document.getElementById("theImage");
              var theResponse = xhr.response;
              myParagraph.innerHTML = JSON.stringify(theResponse);
              myImage.src = theResponse.data.link;
          }

          xhr.setRequestHeader('Authorization', 'Client-ID '+ myIDKey);

          xhr.send(fd);
          xhr.responseType = "json";

      }

This function, coupled with a couple helper functions and the proper html ID's, uploads an image to imgur, and on response displays the response as text and displays the image.
One important part is fd.append("image", file), as that is what is adding an 'image' property with a value of the actual png.
You can check the imgurAPI documentation(link) for more properties you could append.
Another important thing is the xhr.onload = function().
This function is what is executed when there is a response from the server.
What the function is doing is taking the response and associating parts of it with parts of the html document.
Here is the full html doc:

        <html>
          <head>
            <meta content="text/html;charset=utf-8" http-equiv="Content-Type">
            <script type="text/javascript">

              var myIDKey = "Register with imgur to get your own auth key.";


              window.onload = function() {
                var myButton = document.getElementById("theButton");
                myButton.addEventListener("click", uploadFile, false);

              };

              function uploadFile() {
                var selected_file = document.getElementById('theFile').files[0];
                upload(selected_file);
              }

              function upload(file) {

                  if (!file || !file.type.match(/image.*/)) return;

                  var fd = new FormData();
                  fd.append("image", file);
                  var xhr = new XMLHttpRequest();
                  xhr.open("POST", "https://api.imgur.com/3/image");
                  xhr.onload = function() {
                      var myParagraph = document.getElementById("theReturn");
                      myParagraph.innerHTML = JSON.stringify(xhr.response);
                      var myImage = document.getElementById("theImage");
                      var theResponse = xhr.response;
                      myImage.src = theResponse.data.link;
                  }

                  xhr.setRequestHeader('Authorization', 'Client-ID '+ myIDKey);

                  xhr.send(fd);
                  xhr.responseType = "json";

              }
            </script>
          </head>
          <body>
            <input type="file" id="theFile">
            <button id="theButton">The button</button>
            <p id="theReturn"></p>
            <img id="theImage"></img>
          </body>
        </html>
