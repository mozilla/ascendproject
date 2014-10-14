---
layout: post
title:  "Week 5 - Death of a bug"
author: Becky
date:   2014-10-03
categories: becky

---


It's the 5th week. That's sad. It is hard to think of being done in such a short time.

Monday the 6th, So this weekend. Man I started feeling sick Saturday and by Monday I felt pretty rotten. Hanging in there though. I got some serious blogging done. Need to catch up on past weeks...especially week 3. Add some of those awesome screenshots I've been taking.
I made a second patch today. but was working on other things too and didn't put it up yet. I can't help but notice no news on my bug from my mentors side.

Tuesday Dia came and was wonderful. She had a lot of energy. She started off saying how unc comfortable we were going to be. That scared me. That is a very big thing to say to...well me. She was going to do things to make us feel out of our box. I never thought it would take so much courage to count as a group. We stood in a circle and when ever we felt ready, took a step in, say "I'm _____, and I am here." and it was so incredibly awkward and I became hyper aware of where my arms were and my heart was beating so fast. It seems so strange to become so nervous about saying a sentence. a small sentence. and then you feel so silly because all the adrenaline is pumping and you think to yourself....I only said my name. That is all. Why would that elicit that kind of response? I  don't know the answer to that. But I do feel closer to the people in the  group because we all did something that made us feel uncomfortable together and that is a bonding experience I guess.
At checkout it was really tuggin on the heart strings. People were so appreciative of the space we have created and it is really difficult to think about not being here in a little over a week. Really hard. And any time anybody cried it was so hard. And then Carmen said something about how she has always been taught to be polite and do for others even if it hurts her. And that just makes me so sad. I feel the same way. But what really upset me was I know my daughter does. And to think I may have done that to her.  Made her think that her thoughts should come after others. I just ugh I don't know I can't help but be sad. She has amazing ideas and she should feel like her ideas are just as valuable as others. And her feelings are just as valid. So infuriating. And how do you teach a balance between being nice, give people the benefit of the doubt...and also freaking take care of yourself and your voice matters. Anyway I love our Ascend therapy sessions

Wednesday: Typo'd Github and wrote Githug what a great command! Probably my favorite thing of the day. I just got a free hug from Virginia!

In the morning most the people working on bugs for webmaker got together to talk to Kate Hudson and Scott Downe. I was super excited/nervous because Scott is the mentor on my bug but I didn't feel like my patch had been looked at and I didn't know how to express that without sounding ungrateful that he was taking the time to help us. We all started in the same room but Jessia and I are working on Popcorn bugs so we asked if we could branch off and dial up Scott from another conference room. Seemed like a optimal usage of time. Luckily we were able to that.

Talking with Kate Hudson and Scott Downe

    -So grateful they were able to take the time to meet with us and help set up dev environments.
    -Jessica and I played musical rooms until we were able to connect with Scott Downe and got some good feed back. Apparently when I submit my patch I'm supposed to click a feedback or a review box to tell the person indicated they should look at it. I didn't know/remember that. So I was holding my breathe thinking it was wrong or the didn't have time to deal with such matters. But now I understand the ? + - for review and feedback.

While we were in our webmaker/popcorn meeting we missed a presentation on wordpress which I may need to get a better idea of what I missed.

I also submitted my 3rd patch to my bug before I left. Hopefully it will land this time, fingers crossed.

I left early to participate in a promotional video for Portland featuring developers in the area. I am not one yet but am on my way. Jonan was really the one featured and they wanted his family (including Ada our lovable golden retriever) in it. So today was kind of crazy on that note. Took the kiddos in a cab, on the train, in a street car, walked a few blocks and put them in daycare (I felt like we should be arguing about where to eat green eggs and ham) then I went off to school. Did the webmaker/popcorn meeting. Then I worked through lunch because I knew I was leaving early and I was still trying to find the code to fix. Tina helped me figure out where to find it from the patch. Sometimes things are right in front of your eyes and you can't see them. I made my third patch and Jonan picked me up with the kiddos. We went down to a park and had to walk down the sidewalk with the kids a few times and then moved to another park. They had a huge green screen behind us and had us stay in a tiny section of the playground...it was a lot of fun and Kaja has blisters from swinging on the cables. We all had a great time. We went out to ice cream for a job well done and the kids and I headed home.

Also would love to find another bug but would like to feel a little more caught up.
I feel like everyone feels so much relief about our presentations. I feel like it complicated things, but gave some good tools to start with. Maybe it didn't complicate it, maybe it just made it feel more real that that is happening and the program is coming to an end.

Near the end of the day I got a message from Scott saying my patch was ready but I need to to do a git pull request. And that made me feel uneasy. I feel less comfortable with git then I did last week. All this week I felt so into my bug and writing blogs for week 4 and the present week....(still need to fill in for week 3) but in all that I haven't pushed anything in awhile. My bad :( Also I cloned the repo for my bug. I believe I know how to do it if I don't need to fork it. I'll go over some notes that I have from the beginning of the program.

Thursday I submitted a pull request to the popcorn repo. It took a bit of refreshing and forking and cloning and deleting clones and recloning but in the end it got pushed up for review.

Okay so 40 minutes ago....seems like a long time to wait to see if it'll be merged. Tick. Tock. Tick. Tock.

<img src="https://www.evernote.com/shard/s146/sh/8c66cfd1-38f3-4b63-8499-0a3428ca5b21/f3565670eea7d3c60372a915847ccfbf/deep/0/Pull-Requests---mozilla-popcorn.webmaker.org.png" alt="Pull%20Requests%20%C2%B7%20mozilla/popcorn.webmaker.org" />


Look it passed Travis:

<img src="https://www.evernote.com/shard/s146/sh/bb5c770c-44ba-4cee-9c0a-808af11f7fb4/01d0c0186d2dad2006d32bd0cdb77f3a/deep/0/Pull-Requests---mozilla-popcorn.webmaker.org.png" alt="Pull%20Requests%20%C2%B7%20mozilla/popcorn.webmaker.org" />

and bam:

<img src="https://www.evernote.com/shard/s146/sh/2858a172-4eae-4e9f-86ac-a56fa98d1d21/385dcd549a61987fbaba1e22f606edf6/deep/0/1019657---text-and-popup-event-height-while-empty.png" alt="1019657%20%E2%80%93%20text%20and%20popup%20event%20height%20while%20empty" />

I totally did a thing!

On to squash more bugs, because I'm a contributor now, it's just this thing I do.

Friday: Still super excited that my bug landed but you may have noticed how anticlimactic it was to "resolve" the bug. There wasn't even an exclamation point. I mean

Status: RESOLVED → VERIFIED

That feels nice to read, but still I was feeling proud and disappointed. At checkout I told the Ascendees that my bug landed and everyone clapped and man that was what I wanted to happen! I was pretty stoked. May even get a gold star out of the deal.

This morning we all needed to do a pull to get the latest version of the ascend project website we are all contributing to. But I have so many blog posts sitting waiting and it is unclear to me how to make things happen the way I need them too. To be able to upload them and hope the corrections and changes I have made are the ones I want.

Then a few of us went into a conference room with Kronda to get a quick presentation on what we missed when we were in the webmaker meeting the other day. Mostly about customizing your wordpress site. So that is what I'm working for the rest of the day.