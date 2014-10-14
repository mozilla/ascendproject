---
layout: post
title:  "Week 4 - A Bugs Life"
author: Becky
date:   2014-10-03
categories: becky
---


We split up at some point and went over our bugs with a partner. I really had my heart set on doing Bug [924029](https://bugzilla.mozilla.org/show_bug.cgi?id=924029). I was really nervous though because I had no idea what I was getting myself into. As you may recall the first week of school we had 30 minutes to do something. Anything. And I had chose to work with x-ray goggles. I had a hard time getting the goggles to work on another page - I think because I was feeling so nervous about having enough time so I decided since it was working on the x-ray goggles page I should do that. So I had a few reasons why I was here put up a picture of my kiddos and called it a day. Went to save and thought better make sure there is nothing else I want to add. I n something and I guess because I'm used to hitting go back on my phone when a pop up comes I can generally tell it to go away by pressing the back space when I did it said I you sure and I pressed it again...without thinking about it. It left the page I was on and all the work I had done. This bug suggest that there should be an auto save feature. Naturally I felt compelled to have this so that no one else would lose there 20 minutes of hard work. However once I presented it to Lukas we went into IRC to find one of the people involved with the bug. They had said they were going to icebox the bug for now and I thought it may be a good opportunity to revisit and see what would happen. I was really panicked. I hadn't realized when I asked her to look over my bug that I would be jumping into IRC trying to find one of the people involved with the bug. I was really panicked. I hadn't realized when I asked her to look over my bug that I would be jumping into IRC talking to find one of the people involved with the bug. I was really panicked. I hadn't realized when I asked her to look over my bug that I would be jumping into IRC talking to someone. He welcomed me and and said hey. I then wrote Hello. He hadn't capitalized his hey. I shouldn't capitalized mine. hello. Ok that seems better. Maybe too formal? Hi. No wait, hi. there hi. Perfect send. Man that shouldn't be so stressful. I imagine this is going to get easier with time. He mentioned that they weren't exactly sure what they wanted yet and so probably not something I want to try out especially for a first bug. They had said they were going to icebox the bug for now and I thought it may be a good opportunity to revisit and see what would happen. He mentioned that they weren't exactly sure what they wanted yet and so probably not something I want to try out especially for a first bug. So I was on to a new bug.

After looking into  I decided on bug 1019657 about the pop up event box and the text box. When they don't have text in them they collapse into nothing. This is what was going on with the pop up event:

<img src="https://www.evernote.com/shard/s146/sh/a541bd51-31be-4228-8774-e0f8384ff930/0a5cbca6bb6f9ba49bb7d1769ed81a12/deep/0/Popcorn-Maker.png" alt="Popcorn%20Maker" />

I asked the mentor if I could have the bug since it hadn't been worked on and I thought it would be a good first bug. Something I could handle and start to understand the process.

<img src="https://www.evernote.com/shard/s146/sh/ab6e44a2-d2ce-4777-a0bd-6f2466084af5/17876fe9c7c26ce650e7fda3d7547ade/deep/0/1019657---text-and-popup-event-height-while-empty.png" alt="1019657%20%E2%80%93%20text%20and%20popup%20event%20height%20while%20empty" />

 An hour and a half later that bug was mine. I was really excited. To be honest I didn't actually think I would be legitimately excited over having a bug but I was. I had been assigned something, and it was up to me to fix it. Check it out!

<img src="https://www.evernote.com/shard/s146/sh/345e4268-cee2-4237-a4a7-f815d977e763/2c13067b51e260d65de3b761c791f167/deep/0/This-bug-belongs-to-me-now!.png" alt="This%20bug%20belongs%20to%20me%20now!" />

You may notice in that image it says assigned to: RebeccaScheffler....because....it's my bug.

The next day I set up my environment. I googled webmaker github and found instructions [here](https://github.com/mozilla/popcorn.webmaker.org). After cloning popcorn I had a very big problem with node. I forgot that we had installed homebrew on our computers earlier. So I googled how to install node and installed it from source. Which took a long time and I kept getting errors. It was all extremely frustrating. My screen was full of errors, by the end of the day I was pretty sure I was going to cry.

<img src="https://www.evernote.com/shard/s146/sh/8a7d4dc0-84da-42c5-a187-bee2c1e36ca3/18dda03d286be6217ee2ac8f73db63a6/deep/0/errors-galore-2.png" alt="errors%20galore%202" />

The next day I worked with Lisa a lot and she helped me walk through the list of errors and actually after we fixed one or two the rest went away too.

Things ran way more smooth after that. I was able to run "node server" and get a local working popcorn page. That was pretty cool. Really pretty cool.

<img src="https://www.evernote.com/shard/s146/sh/7293e211-92c5-4d5e-a4ec-4460641c6655/db7f73a0722d6b5a6bf98323c0214aa9/deep/0/14,-2-29-PM-(PNG-Image,-1365---681-pixels)---Scaled-(83-).png" alt="14,%202:29%20PM%20(PNG%20Image,%201365%C2%A0%C3%97%C2%A0681%20pixels)%20-%20Scaled%20(83%25)" />

So I started dinking around...right clicked the pop up box and chose the Inspect Element option. There I could hover over code and see where I was working. It took me a bit to find out where I wanted to be. I started with changing the px but I was concerned if the text got bigger the box would stay the same and the font would out grow out of the box. I vaguely remember talking about ems at the beginning of Ascend. I tried that out and it seemed to work out well. See?!

<img src="https://www.evernote.com/shard/s146/sh/e072dc63-d7bb-4625-9697-6285f6993b62/873205c2787b9d2caca9107e98c0d753/deep/0/the-change-on-element-inspector.png" alt="the%20change%20on%20element%20inspector" />


But now I had to find the real code instead of just changing it temporarily  on the website. I really didn't have any idea where to start so I just started going through each folder to see if anything sounded promising. It didn't. Eventually I had to ask Lukas how you find the bit of code to change. She asked me where I changed it on in the inspection place. I really didn't know I just kind of found the code by messing around. But I love taking screen shots so I showed her that. Turns out you can just open the entire popcorn

By the end of week 4 both of them were ready to go and ready to make a second patch.

<img src="https://www.evernote.com/shard/s146/sh/45cdfc9d-cf00-4416-9246-db734b6c93f1/7cf0e2955d08a5bfdb584df2bb417c9b/deep/0/Popcorn-Maker-and-popcorn.webmaker.org---node---123-28.png" alt="Popcorn%20Maker%20and%20popcorn.webmaker.org%20%E2%80%94%20node%20%E2%80%94%20123%C3%9728" />
