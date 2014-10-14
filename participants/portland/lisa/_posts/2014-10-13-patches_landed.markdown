---
layout: post
title:  "Patches Landed!"
author: Lisa Hewus Fresh
date:   2014-10-13
categories: lisa
---

I had the worst night's sleep in a long time. Just before I went to bed the night before, I noticed that a participant's blog had only the alt text showing up for two of their images. One image was correct and they obviously made it past Travis so it was unusual. Apparently my brain thought it was terribly odd and needed to be fixed <em>now</em>! I tried to solve it over and over in my dreams and this awakened me several times. I never did come up with a solution though.

All of this waking caused me to be late out of bed so I was rushing around all morning. I couldn't be late being early! Some days I just don't know about me. Anyway, I made it at my usual early time so all was well. We had our check-ins and lots of us were sad about this being our last week. I feel awful when I think about it so I try not to. We had some time to work on our tasks before the All Hands meeting and just about this time I got notification that one of my patches had landed! Finally! The All Hands meeting was great and there are some exciting Mozilla things to come in the very near future.

I decided I would spend some time looking at OPW projects since I wasn't on a bug rollercoaster any longer. The site said that most projects had many applications and to consider one of two that hadn't received any. I looked at one and didn't feel it was a good fit at all. The other one was ok but not something I was terribly excited about. I would probably learn a lot though so I decided to try to set up their dev environment. That required either installing directly on my computer or installing on a virtual machine. I opted for the VM since I didn't know where this would go anyway.

There were several operating system choices but they were all Linux-based. I don't know a thing about Linux but how hard could it be. I randomly chose Debian. I started up VirtualBox, created a new Debian VM, and then quickly realized it was going to want an install disk. Crap. Off I went searching for the ISO files. That was going to be a lengthy download even with the speedy Mozilla internet connection. It took about 30 minutes to download the three images so I read up on the project and what their software does. I also stopped briefly for lunch which was delicious Thai food! Yum!

Once the images were downloaded I installed Debian. It was ridiculously easy and I was up and running before I knew it, or so I thought. Next it was time to install their stuff. Well that's when everything got complicated. I got permission errors and missing package errors left and right. Ugh! It wanted to read off of the install ISO but that was on my real computer (that sounds odd) and it's not a matter of just dragging and dropping into the VM. I had to download it again! Another 30 minutes just for the first ISO since that was all I needed. I did more reading of the project and then watched the last two minutes of the download at which point it completely failed due to a lack of disk space. Wow, really? I was juuuuuuust a bit frustrated so I deleted the VM and started over. I created this one with a larger hard drive and more memory. I also paid more attention when installing and set up a package source so it wouldn't ask for the ISO images. Handy! Things were moving along much better this time. I got Debian up and running and started installing the other software and once again it asked for the ISO. What the crap?! I did a bit of searching and found I needed to comment out a line in the sources file to stop it from asking for a disk image. That worked much better!

Somewhere in all of the above nonsense I got notification that my other patch landed! Two in one day! One was fairly insignificant but it still needed to be done and I did it so I'm happy.

We had to break for 10-15 minutes and then work on our talks right afterward. Bleh, stress, stress, stress. I started sweating just thinking about it. Adam and I went into a small room and had to practice just our first minute with each other and then give feedback. It wasn't awful. We decided we were going to try to give our talks as soon as possible and just get it over with!

I went back to my laptop and started installing the required software for the project and it churned away happily. And then it finished with some sort of error although the application was running. I had no idea what the errors meant but it was time to check out and I had to leave as soon as possible to take Michael to the airport.

I kind of ran out and met Wayne and Michael downstairs. They had dropped Andrew off nearby so he could work on an issue building Perl on a Vax? with a fellow OpenBSD committer. Yeah, I have NO idea either. We had an uneventful drive to the airport and headed back home. We weren't here long before Andrew said he was done for the night so I drove back down and picked him up. We grabbed dinner while we were down there and once again I wanted Los Gorditos. I really can stop any time. We got everything to go and the whole family was very happy with their food. That should go without saying because Los Gorditos is really good.

Today I learned that our friends Dan and Jessie had their third baby. A daughter named Opal Mae.
