---
layout: post
title:  "Strikes and Gutters, Ups and Downs"
date:   2014-10-03
categories: peri
author: peri ahmadi
---
Where to start? Hmm...let me see. Well, I guess first things first. On Monday, we sort of settle on a bug that we want to fix. I had a bug picked out which I wrote about in a [previous blog post.](http://ascendproject.org/participants/portland/peri/2014/09/24/Buggybugs/) Well, on the day we start researching how to patch our bugs, I find out that two others had picked that same bug. I don't want to get too hung up on it so I immediately begin looking for a new one. I dig a little deeper this time so I'm sure to pick something no one else was looking at. We team up for this preliminary bug research and my partner Becky, is super helpful and cheerful as always. So we plough (plow?) through the assignment. We're given a set of tasks to complete in working up to commenting on our bug. 

So I find a bug and look into it and go home and when I come in on Tuesday morning--lo and behold--someone had submitted a patch. So I find another. [My bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1001466) seems simple but not too simple, which is what I wanted. Something that won't discourage me by being too difficult for me to tackle, but also something that will challenge me a little. 

I found out everything I could about what I needed to do and met with Lukas and Kronda and was pleased to learn I was on the right track. During the meeting, Lukas also checked to see if we were caught up on each of the assigned tasks we were given. I was all caught up with the exception of having broken images in a [recent blog post.](http://ascendproject.org/participants/portland/peri/2014/09/18/Week2HowTo/) I also had an ongoing problem with my web dev enviroment, but that's all just housekeeping. 

So yay! Strike! Good news! I'm doing a fine job after all!

Here comes the gutter. The down. I get to work on my relatively simple bug. To start I go to test it just to have a control and know what the problem looks like from a test perspective. When I run the jetpack tests, I notice first of all, that the tests are buggy. The automated tests are supposed to open and close windows while they try different things out. Well, at one point the window fails to close. I file a bug report and decide to *only* run the test relevant to my bug. 

I can't.

After hours of running and re-running and trying and re-trying, I enlist Lisa's help. We figure out that I have addon-sdk installed in a different directory and no matter what I command, the tests always run from that other directory. Easy, remove directory. Now go into my repo and rerun the tests. I get:

>#####Warning: your mozrunner package is installed at /Library/Python/2.7/site-packages/mozrunner, which does not seem to be located inside the Jetpack SDK. This may cause problems, and you may want to uninstall the other version. See bug 556562 for more information.#####

OK now I'm getting stressed out. Even writing this blog post is a little stressul. I [see bug 556562](https://bugzilla.mozilla.org/show_bug.cgi?id=556562) and try the workaround in it. Turns out the workaround was written in 2011 and has since become deprecated. So the workaround doesn't work. Now what? 

I meet with Lukas again and she gets me back on track and helps me figure out what to do once I get the tests to run in order to run a diff and compare the test pre and post patch. I come out feeling like I've got new handle on it and it should work. But it doesn't work still. I basically end up back at the beginning. I can get the tests to run but I can't run the specific test I need, nor can I interpret the results. Full cicle. I has sad. 

I get a hold of my mentor on IRC and he tells me to try a bunch of things I've already tried and I feel defeated. Finally, someone else in IRC pipes in with something like, "You don't wanna run jetpack tests on a machine that has mozrunner installed." This is maddening. I just laugh. I know this. The computer has told me this. I've spent two days trying to workaround having mozrunner installed. I decide to uninstall mozrunner. "Permission denied."

AAAAAAHHHHHHHH!! Seriously puter!? What have I ever done to you? Why do you smite me?

I give up. Go out. Have some drinks. And my boyfriend says (a 'duh' moment in retrospect), "You have a virtual machine with Ubuntu installed, have you tried using that?"

HAHAHHA! So simple. Three days! Three days I've been stuck on this and in the end it's such a simple solution. I come in this morning and start my VM, clone my addon-sdk repo, run the tests. Everything works! The tests come out in a neat little text file saying that everything is fine and passed and these errors were logged. 

I go into [bug 556562](https://bugzilla.mozilla.org/show_bug.cgi?id=556562) and leave a comment describing my troubles and how I finally came to a suitable workaround. I specifically point out that I'm a newb and posting in case any other newbs are going through the same thing. Then someone replies, "My workaround was to just use a different computer :/."

Thanks, snarky computer guy :/. 


