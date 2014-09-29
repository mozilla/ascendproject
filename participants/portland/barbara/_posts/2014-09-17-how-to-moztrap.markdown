---
layout: post
title:  "how to moztrap"
date:   2014-09-17
author: "Barbara Miller"
categories: barbara
---

WORK IN PROGRESS

finding and running MozTrap tests for the Firefox web browser

![MozTrap home](images/moztrap-home.png "MozTrap home page")

on your mark
------------

1. Go to [https://moztrap.mozilla.org/](https://moztrap.mozilla.org/)
2. Sign in with your Persona account (it’s a small text link towards the right).
3. Click Run Tests.


get set: find a test suite to run
---------------------------------

![finding a MozTrap test suite to run](images/moztrap-find-test-suite.png "Finding a MozTrap Test Suite")

1. On the next page, select from Products "Desktop Firefox".
2. Select from Versions the version you will test... Nightly will be latest, at the end of the list (35 as of 2014-09-17), preceded by Aurora (currently 34), preceded by Beta (currently 33), preceded by the current release (currently 32).
3. Select from Runs a test to run. (Sometimes, there’ll be no tests listed, when no tests are set up for the version you’ve selected. Return to step 5 to choose another version to test).
4. Set your Build value. You can find this by opening about:config in a new tab or window (be sure to do this in the Firefox version you are testing, which may or may not be the version where you're using MozTrap). You'll probably see a warning: "This might void your warranty!"; click "I'll be careful, I promise!" Now search for "buildid". You'll see several items that have the same value, beginning with the current year. Double click any of those items to open an edit window, then copy the Build value. Click "Cancel" to close the edit window. Return to your MozTrap window, and paste the Build value in its box.
5. Set your Operating System (for us Portland Ascenders, OS X 10.9, or OS X 10.8 if 10.9 is missing) and Platform (OS X) from the dropdown menus. 
6. Click the green "run tests in ..." button.


go! run a test
--------------

![run a MozTrap test](images/run-moztrap-test.png)

1. On the next page, in the list of tests available in your selection, click the little arrow button at the left end of a test line to show its detailed steps.
2. For each step in a test, you can report a failure with the pink button to the left. Reporting a failed step marks the whole test as failed.
3. If the test overall is unclear or otherwise invalid, you can report this using the yellow warning button.
4. If all the steps pass, click on the green PASS TEST button.
5. If there are additional tests in the test suite, you can start again from step 1.


need help?
----------

Check #qa on irc, at irc.mozilla.org.


