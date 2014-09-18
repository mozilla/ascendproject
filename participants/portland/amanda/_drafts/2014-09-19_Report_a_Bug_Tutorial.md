---
layout: post
title:  "Tutorial: How to Report a Bug"
date:   2014-Sept-19
categories: amanda
---

Having issues with your Firefox browswer?  Want to help with the next version of Firefox?  Want to learn something fun and new? 


	Report a Bug:

	![Alt text][/images/2004_security_bug.jpg] "picture of a bug"


### Test your bug

Is it a bug?  Here are some questions to ask yourself:
* Can I reproduce it?
	- every time OR intermittently
		- if intermittently, can you state about how often?
* Open a Clean Profile in the same version of Firefox that you found the bug.  
(if you haven't set up profiles, go [here](https://support.mozilla.org/en-US/kb/profile-manager-create-and-remove-firefox-profiles))

* Open a Clean Profile in another version of Firefox.
	- for example, if you are reproducing this bug in Firefox Nightly, try and see if you find the same bug in a new Firefox Aurora profile.  (This is called "Regression") (if you haven't set up to run different version of Firefox at the same time, go [here](https://developer.mozilla.org/en-US/docs/Mozilla/Multiple_Firefox_Profiles) first and scroll down to the last three paragraphs titled "Setting up multiple profiles for different Firefox Channels")

### File your bug

After you have completed these tests, head on over to [Bugzilla@Mozilla](https://bugzilla.mozilla.org/).  You'll need to create an account in Bugzilla and later, can sign in using your [Persona Account](https://support.mozilla.org/en-US/kb/what-is-persona-and-how-does-it-work).

* Click on "File a Bug"
![screen shot of bugzilla main page][/images/screen_shot_bugzilla.jpg] "screen shot bugzilla main page"

* Scroll down the list and find the service that you want to report a bug on (ie if you were using Nightly, then click on "Firefox" which is first on the list)
![screen shot of step 1 of 3][/images/screen_shot_bugzilla_1_of_3.jpg] "screen shot bugzilla 1 of 3"

* Type short summary of the issue in the white box just before hitting "find similar issues.”  You'll want to see if someone else has already filed this bug.
![screen shot of step 2 of 3][/images/screen_shot_bugzilla_2_of_3]
- scroll through issues
![screen shot of step 2 of 3][/images/screen_shot_bugzilla_2_of_3_a]

* If you don’t see your issue listed - continue on by clicking on the button "My issue is not listed(see previous screen shot)."

* Fill in report.
![screen shot of step 2 of 3][/images/screen_shot_bugzilla_3_of_3]
- Your summary will already be entered from the previous screen.

- Check to make sure the Product category is still correct.

- Fill in the whitebox for "What did you do."  Try to clearly state the steps that you took to reproduce the bug.  Use
concise, descriptive language as you are guiding someone else on how to follow what you did.

- Fill in the whitebox for "What happened?"  Again, be clear on explaining what the actual results you attained.

- Fill in the next whitebox for "What should have happened?." 