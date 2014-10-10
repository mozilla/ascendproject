---
layout: post
title:  "Week 3: Dev Environment"
date:   2014-09-26
categories: virginia
---
Monday 9/22
Weekly Mozilla all hands meeting
lunch: Pacific Pie Co
Begin setting up development environment on our MacBooks per [this blog post](http://mallinson.ca/osx-web-development/). Lots of downloading, installing, configuring. Happy to be doing this with the whole group because I'd be a lot more hesitant and grumpy about all this stuff otherwise. With the group, I just do it to keep up with everybody, and i have people to ask if I run into a snag, and then it's done before I know it!

Tuesday 9/23
lunch: carts

Finished setting up dev environment with MySQL and WordPress, per yesterday’s instructions as refined in Kronda’s new blog post:
http://karveldigital.com/setting-wordpress-development-environment-mac-os/

Install a local build of Firefox
This did not mean, as I first thought when I heard the term “you’re going to build Firefox,” that we were going to write code for an entire web browser from scratch. And thank goodness, because it was only allotted 45 mins in our agenda for today.

Lukas walked us through making small changes in the code of Firefox, to change the way tabs behave (new tabs pop up on the left side of current tab instead of the right), and change a tooltip string of our choice, using the example of the refresh button. I chose to change "Reload current page" to "EXCELSIOR!"

We installed a ready-to-use virtual build environment per [this great blog tutorial](http://timtaubert.de/blog/2014/04/a-ready-to-use-virtual-build-environment-for-firefox/), ran a script to build firefox nightly, ran it. That was the relatively straightforward part. The lesson (the hard part) was figuring out how to install git, pull down our patch in the virtual machine, apply it and take a screenshot of the tooltip that we changed to prove the patch worked. I did everything I thought I needed to but I'm still seeing "Reload current page" when I hover over the reload button, so I'll have to work more on this and figure out what I did wrong or didn't do at all.

Wednesday 9/24
Catch everyone up with wordpress and firefox build. I got a bit stuck on WP, couldn't get the page live on Kronda's server, but she later told me it was something she could fix on her end so I did everything right! :)
begin looking into first bug.
lunch: carts

Thursday 9/25
There's a security vulnerability in the bash code so we all downloaded the patch.

Rest of the week: honestly I am typing this in week five because we have so many balls in the air that I didn't finish this blog in a timely manner. So I'm sure some important stuff happened Thursday and Friday but there's been a lot going on. I finished week 4's blog before this one, that's how busy and all over the place things have been for me here. Probably going to abandon this day-by-day structure for weeks 5 and 6. Also feel free to follow my twitter if you want to! I'm [@thayerve](https://twitter.com/thayerve).
