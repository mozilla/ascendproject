---
layout: post
title:  "First Bug Fixed - Code Landed"
date:   2014-10-9
author: Adam
categories: adam
---

One of the major activities that participants of the Ascend Project are doing is working on contributing to open source via working on bugs that were found on Mozilla's <a href="https://bugzilla.mozilla.org/">bugzilla</a> site. We all started choosing the bug(s) we wanted to work on a few weeks ago after having had Bugzilla explained to us in terms of how to navigate the site and how to read the conventions often used when bugs get listed.

I initially had a bit of trouble deciding on what to work on but ended up settling on <a href="https://bugzilla.mozilla.org/show_bug.cgi?id=1025925">bug 1025925</a> that was essentially about making the conventions used in the code base of Fjord consistent. <a href="http://fjord.readthedocs.org/">Fjord</a> is software that runs Mozilla Input which collects actionable feedback regarding Mozilla's different products across all of the platforms that they run on. This feedback is used by multiple teams within Mozilla and is instrumental in figuring out what issues users are facing when using Mozilla's software.

While what I was tasked with doing in terms of fixing the bug was pretty straight forward (changing file names and making sure that the rest of the code base correctly pointed to those files) I chose it and enjoyed fixing it for a number of reasons. One of the reasons was that all of the files were written in Python which is a language that I'm interested in learning. Fixing this bug allowed me a number of chances to look at well written python code. One of the other reasons I chose it was because it was listed as a "good first bug" and had a mentor assigned to it.

I finished fixing the but on Friday October, 3rd and the <a href="https://github.com/mozilla/fjord/pull/355">code landed</a> later that day. It was a really enjoyable process and I'm really that I had a lot of help, especially from <a href="http://bluesock.org/~willg/">Will Kahn-Greene </a>and <a href="https://twitter.com/mythmon">Mike Cooper</a>. It was also all made a lot easier by being able to do this while in the Ascend Project as I was able to be in Mozilla's Portland office and have a number of people within not quite arm's reach to turn to if I had a question that I couldn't quite figure out on my own.