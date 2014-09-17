---
layout: post
title:  "Using Multiple Types of Firefox"
date:   2014-09-18
categories: tina
---

<!--
1) profile manager
2) download all firefoxes
3) install all firefoxes
4) run firefoxes with profiles
-->


## By Tina

###Overview

To run different versions of Firefox at the same time takes some prior setup.
I am going to assume first that you have the release version of firefox installed.
To mean: you have (or should first) installed the version of firefox from [getfirefox.com](http://www.getfirefox.com).
With firefox installed, yet *not* running, open up your terminal application.

###Opening Firefox Profile Manager

For MacOSX:

    /Applications/Firefox.app/Contents/MacOS/firefox --profile-manager

For Windows/*nix systems:

    firefox --profile-manager

In the profile manager: make 3 additional profiles and name them

    "aurora", "beta", and "nightly"

Uncheck the box that says

    "Use the selected profile without asking at startup"

Hopefully your profile manager window looks something like this.

![profile manager screenshot](../_img/profile-manager.png)

###Downloading Other Firefoxes

First let's proceed to [mozilla.org/beta](http://www.mozilla.org/beta).
From here you want to download and then install the Aurora version of Firefox.
