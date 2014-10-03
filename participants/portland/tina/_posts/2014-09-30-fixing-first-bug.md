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

One of the [comments](https://bugzilla.mozilla.org/show_bug.cgi?id=992386) on the bug mentioned a specific 'screenshot.js' file that needed to be changed.
So I opened it up and immediately felt that first stomach drop as I didn't understand a lick of what was there.
But with some resilience, and the gcli (Graphical Command Line Interface) [documentation](https://github.com/joewalker/gcli/blob/master/docs/index.md), I started to understand the different chunks of code and where I would need to edit them.
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
You can check the imgurAPI [documentation](https://api.imgur.com/) for more properties you could append.
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

With the webapp finished, I tried to slap the code into firefox's screenshot command.
That's when I hit another brick wall.
Firefox told me that "FormData is not defined."
What this meant is that FormData objects and XMLHttpRequest were not going to work inside of gcli's code, and I didn't know how to make it work.
What I ended up doing is googling "gcli xmlhttprequest" and I ended up finding "Cc["@mozilla.org/xmlextras/xmlhttprequest;1"].createInstance(Ci.nsIXMLHttpRequest)."
I'm going to be honest: I don't know what this means.
My limited understanding is that the 'Cc' is acting as something like an 'include' from other c-based languages.
With that found, I was pretty estatic!
Now the only thing that I needed was where in the code the actual image was.

This was now the third brick wall that I had to overcome.
In 'screenshot.js' there was a particularly interesting line:

        let data = canvas.toDataURL("image/png", "");

To me it sounds like 'data' contains the data of the actual .png file of the screenshot.
But it wasn't working!
Setting fd.append('image', data) didn't return any image from imgur.
I didn't know what to do.
So again I googled.
I researched .toDataURL and found that I was in fact correct: this was the data of the image, but it's being parsed as a dataURI... which is confusing.
I don't really understand [dataURIs](https://developer.mozilla.org/en-US/docs/Web/HTTP/data_URIs)  just yet, something about embedding data into html.
So again I googled.
A search for "imgur upload dataURI" resulted in some example [code](http://29a.ch/2011/9/11/uploading-from-html5-canvas-to-imgur-data-uri) of someone uploading using these dataURIs.
Instead of trying to just use 'data,' I guess you need to use data.split(',')[1].
I guess 'data' is a string with the image data + some other metadata involved.
So the .split(',')[1] is splitting up 'data' and then only grabbing the second part of it.
Luckily this made some sense after reading more about [dataURIs](https://developer.mozilla.org/en-US/docs/Web/HTTP/data_URIs).

With that last piece found I was pretty much done!
I could use 'screenshot --imgur' to upload a file and have imgur return the uploaded link.
But I wanted my function to do more.
I wanted it to open up the link in a new tab.
After some research, if you use 'window.open(link)' in normal JS then a new tab will try and open.
I say "try" because firefox's preferences can stop pages from opening new tabs.
It was cool being able to do this in my trial webapp, but alas(!), it *again* didn't work in the gcli code.

For those counting at home that's brickwall number 4.
I wanted to just use 'window.open()' but window was already defined in the code to be something other than the window I knew of.
So I googled one more time.
Searching for "gcli open window" I found a [link](https://developer.mozilla.org/en-US/docs/Tools/GCLI/Writing_GCLI_Commands) that I had already seen.
But this time it turns out to be useful!
Gcli commands are given a set of arguments, and a context for the command.
I'm not sure what the context is, but MDN says that 'context' has an '.environment' method(? that might be ruby-speak) from which I can call document.chromeWindow() and gain access to the browser.
Unfortunately for my work, the function grabScreen() that my imgur upload code sits in, is outside the scope of the screenshot function's arguments and context.
To say: the screenshot gcli command, runs with arguments and context, and then passes in those arguments to a separate grabScreen() function.

What I ended up doing is adding in the screenshot context as an argument to pass to grabScreen().
I don't know if that's within any mozilla coding guidelines, but now that I've submitted a patch to bugzilla with those changes, all I can do is wait and see.
