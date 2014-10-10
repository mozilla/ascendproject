---
layout: post
title:  "Dive Into Bugs!"
author:     Tina
date:   2014-09-24
categories: tina
---

So we're looking at bugs listed on [bugzilla](bugzilla.mozilla.org) as "good first bugs."
I've found a few that I think seem interesting to work on.

* [1015647](https://bugzilla.mozilla.org/show_bug.cgi?id=1015647) -
This bug involves making some console output text copyable.
I don't know exactly where to start, but I think I'd look at console return perameters and try to make the output text be some hypertext link.
This may involve looking at how firefox interprets text as a link and then doing *that* to the console output.

* [941477](https://bugzilla.mozilla.org/show_bug.cgi?id=941477) -
This bug is more of a request for a mozmill test to be written.
I would start by reading up on mozmill test documentation and then jump right into getting the test written.

* [875773](https://bugzilla.mozilla.org/show_bug.cgi?id=875773) -
Right now when a test to check if an addon is compatible with firefox will only return true or false.
To fix it that return should be true or an error with some description of why there is an error.
So I'd have to read up on the different ways that an addon could fail compatibility tests.

* [992386](https://bugzilla.mozilla.org/show_bug.cgi?id=992386) -
This bug is more of a feature request.
It involves adding an --imgur flag to firefox's screenshot console command that automatically uploads the screenshot to imgur.
This would involve reading about said screenshot command, and the imgur API to integrate the two.

* [1072371](https://bugzilla.mozilla.org/show_bug.cgi?id=1072371) -
I'm not too certain what this one is about.
I guess right now RemoteAddonsParent.jsm is outputting errors, and they need to be resolved.
To start this bug, I would email the mentor and ask for some direction on where the file is, how to get the error, and some steps to start fixing it.

* [1068354](https://bugzilla.mozilla.org/show_bug.cgi?id=1068354) -
This one is my bug!
It might be above my head, but I'd start by finding where the code for about:newtab is located.
Then I'd try and find how a mouse click release event could be used to move the image to the correct location.
If I'm excited to fix any of these bugs it's this one (cause it's mine!), but I also don't want to get too deep too soon.


As it stands now, the imgur request, remoteAddonsParent.jsm, and my bug are at the top of the list.
We'll see which one sounds best to Lukas and Kronda.
Stay tuned!
