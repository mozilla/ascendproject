---
layout: post
title:  "MozMill Automated Tests Tutorial" 
date:   2014-09-19
categories: jessica
--- 
##How to run automated tests using MozMill on a Mac

Automated testing is fun to watch but beware it will make manual testing seem even more tedious and leave you asking "Why hasn't this test been automated yet?" MozMill is a command line tool that lets you test using Python and Javascript. This tutorial will walk you thorugh the basics of running a MozMill automated test on a MacOSX 10.9.4. I'll admit that I chose this topic for the tutorial so that it would force me to understand more about this process so if you run into any errors in my understanding feel free to let me know. I might have gotten overambitious on this choosing this topic. 

###Brief Overview of Installation on newer Mac (version 10.4 or higher)
 Since my Mac already has Python 2.7 installed (MozMill requires at least Python 2.5) downloading MozMill is as easy as entering 4 lines into the terminal. 

> curl -O https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py

> sudo python ez_setup.py

> sudo easy_install pip

> sudo pip install mozmill

More details on installation [here](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Mozmill#Installation).

###Clone the Automated Test Repository using Git

Using Git we can clone the Automated MozMill test repository with the following command in the terminal: 

>git clone https://github.com/mozilla/mozmill-automation 

###Switch to hotfix-2.0 branch 
We need to switch to the hotfix-2.0 branch because it contains updates we need to run automation tests. So first we change to the newly created mozmill-automation branch. 

> cd mozmill-automation

Next we switch to the hotfix-2.0 branch by typing these lines into our terminal: 

> git checkout hotfix-2.0

> sudo python setup.py develop 

###Run Automated tests 

Now we should be able to run automated tests by entering this in the terminal:  

>testrun_functional --report=http://mozmill-crowd.blargon7.com/db/ /Applications/FirefoxNightly.app

**Note:**  Our pathway (/Applications/FirefoxNightly.app) is specific for Macs using %path_to_firefox% (on Mac to .app)

<!---Here's another prompt to run automated tests: 

>mozmill -t firefox/tests/functional/testPreferences/testRestoreHomepageToDefault.js -b /Applications/FirefoxNightly.app
-->

And behold the computer runs tests for you faster than you could. 

If you could get this working then go ahead and award yourself a badge! 

![Image of Badge](http://chart.apis.google.com/chart?chl=https%3A%2F%2Fbadges.mozilla.org%2Fen-US%2Fbadges%2Fclaim%2Fkvcw3t&chs=200x200&cht=qr&choe=UTF-8) 

You can use this code **kvcw3t** at to redeem your badge [here](https://badges.mozilla.org/). 

Also, feel free to comment on how I could've made these instructions easier to follow. You can check out the official documentation [here](https://developer.mozilla.org/en-US/docs/Mozilla/QA/Mozmill_tests). 