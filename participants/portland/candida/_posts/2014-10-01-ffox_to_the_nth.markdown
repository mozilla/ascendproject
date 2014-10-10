---
layout: post
title:  "Firefox to the Nth Power"
author: Candida Haynes
date:   2014-10-01
categories: candida
---

## A tutorial on using your Mac terminal command line to run different versions of Firefox at once

If you decide to test bugs in different versions of Firefox you may want to run more than one version of Firefox at the same time. If you try to open a second Firefox on a Mac out-of-the-box, you will see an error message like this:

![Error message - Firefox is already open.](/participants/portland/candida/images/profile_dupe_error.png "You cannot open more than one Firefox.")

Fortunately, one of the first things we did at Ascend was set up our computers to run different versions of Firefox at the same time. Here are the steps:

1. Make sure you save these instructions somewhere outside of a Firefox browser. 
2. Close Firefox.
3. Locate the Profile Manager from the Terminal window.
  
![Profile Manager Screenshot](/participants/portland/candida/images/profile_find_terminal.png "Profile Manager")


4. Double-click to open the terminal and navigate to the binary folder that contains Firefox’s Profile Manager. 


In English, that means:
      
- Type or copy and paste the following file path into your command line.

  /Applications/Firefox.app/Contents/MacOS/firefox-bin --ProfileManager

  It will look like this but it will have your hard drive’s name instead of 02100, etc.

   
![Profile Manager Screen and Terminal Shot](/participants/portland/candida/images/terminal_open_profile_mgr.png "Profile Manager screen and terminal shot")


Follow the instructions in the next few panels.

![Profile Manager Screen and Terminal Shot](/participants/portland/candida/images/intro_to_ffox.png "Introduction to Profile Manager screen")

![Screen with newly created profile](/participants/portland/candida/images/normal_firefox.png "the new profile")

I named the new profile for this tutorial ’Normal_Firefox’ (without the quotes).

![Conclusion - Naming the File](/participants/portland/candida/images/done_start_normal_firefox.png "I named the file Normal_Profile")

For fun, I copied and pasted the file path to the user-related data notes that I keep. 

The rest is up to you. Read everything on the screen and decide which choices are best for you. You’re in charge!

Link to I’m in Charge! [coming soon]


Now, create another profile with a different name and a different version of Forefox. Were you able to make profiles for your different versions of Firefox? If so, go claim your [badge](https://badges.mozilla.org/en-US/badges/claim/94x9wp)!

[Claim My Badge!]https://badges.mozilla.org/en-US/badges/claim/94x9wp)

