---
layout: post
title:  "Patchwork"
date:   2014-10-10
categories: peri
author: peri ahmadi
---

So this week was fun. I had a hard time getting my environment set up to test my bug/patch and when I finally got it fixed, I delved into the code around my bug. First thing I did was cut out the code I thought needed to go and paste it in an empty file with //comments for where I cut it from, just in case I broke everything and needed to put it back. 

When I ran the tests, everything was indeed broken. So I put it back to right and started from scratch, trying to understand the code and what I was doing. Amanda came up to me at some point and said something like, "maybe don't delete all of that, but just try to delete small pieces and test it to see if it works." I thought that was good advice so I took out one line. I tested it. Reds are off, greens are showing. Yay. 

So then I didn't know what to do. I fretted over it for days. At this point I was too scared to alter it again thinking I'd break everything. And I became filled with self-doubt. I really don't know anything about code and I'm just shooting in the dark here. 

So I finally went in and talked with Kronda about it and she said to try to take out the parts I wanted to take out but in larger pieces. So I did. I ended up cutting out almost exactly what I cut out my first time altering code. It worked. A week of panic and fretting and my problem all along was a syntax error due to taking out one too many brackets. Alas. 
Live and learn. 

So I got really excited, submitted a pull request, and got some nice feedback from my mentor. It didn't quite land yet, but it will. My mentor's supposed to hook me up with slightly more difficult bugs to work on. Great success!