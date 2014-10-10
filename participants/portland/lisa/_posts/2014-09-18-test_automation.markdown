---
layout: post
title:  "Test Automation"
author: Lisa Hewus Fresh
date:  2014-09-18
categories: lisa
---
It's raining today! I have really been looking forward to some weather and it's finally here. Lots of people say I will regret wanting it but they haven't lived where I have. This is a welcome change. Morning check-ins were great. It seems many people have been having vivid dreams. They are hilarious to listen to!

Kronda is off at her conference where she is keynoting! We miss her but we have Sam here in her place and he's pretty awesome as well. We started off going over our class agreements and everyone had a lot of input about how we could improve and add to them. It was very interesting to revisit this after nearly two weeks with the project. There were a lot of great modifications and additions. Some changes involved rephrasing and some were the addition of things we, as a group, hadn't originally considered. This group task took us until about 11:00. After that I asked Sam for help with my seemingly endless Git issues. He showed me some amazing Vim commands and also showed me how to record my first macro. That made editing a lot faster. He also had me download <a href="http://www.gitx.org">GitX (the rowanj fork)</a> which is a very handy Git GUI.

At some point during all of this Git stuff I checked up on my bug report and didn't really understand the comments. I showed it to Lukas and she explained that it was progressing and was nominated as a bug that should be fixed. She said that's a good thing so I'm happy.

It was lunch time so Sam and I took a break from his Git repair lesson so that we could eat. Lunch was delicious Thai food! There was the typical "being vegan" issue though. I didn't get my food until everyone else and since everyone else can eat the regular food as well as the vegan food there was not much left of that. Oh well, I enjoyed what I had and there are more than enough snacks in this office so I will definitely never go hungry!

After lunch we began the task of installing and running Mozmill. It's an automated testing framework and a super cool thing about Mozmill is that it can be run against any official build of Firefox. It doesn't require some special test enabled version.

We were given some very basic instructions and some links to follow for more information but not a lot more. I think Lukas wanted us to do a lot more problem solving and figure out how to get it all going ourselves as much as possible. Some were ok with this and some were very frustrated and unsure about what to do but those who got it going were able to help those who were struggling and I think we all eventually got it running!

When a testrun script is invoked it clones the remote test repository, automatically switches to the correct branch for the version of Firefox being tested, runs the tests and then sends the results to the Mozmill dashboard. It was so cool to see the automated tests running! Here are my <a href="http://mozmill-crowd.blargon7.com/#/functional/report/2f982f72826307fed840a3b11c3bbb59"> test results</a>.

I pestered Sam again to help me finish fixing my Git repo because it was now in a partially fixed state but I had absolutely no idea how to proceed on my own. If he wasn't coming back tomorrow I'd be fairly well screwed but luckily he had some time to help me get it done. He showed me how to pick a good point in the history of the remote Ascend repo so that I could cherry-pick my commits from that point forward and get them merged in without all of the extraneous crap I had managed to get in there. He had me delete my, very messy, open pull request first and then showed me how to make a branch called "scout" that would be where I wanted to begin pulling out individual commits. He showed me how to cherry-pick only the commits that I made and then had me make a "safe_point" branch so that I would be able to undo this if I made a mistake. I'm a little bit unclear on the next steps because the day was winding up but I believe I checked out my local gh-pages branch, pulled the remote ascend/gh-pages branch, did a git reset --hard ascend/gh-pages (Sam says this is VERY dangerous! And that he does it all the time), merged in my scout branch, and then did a git push -f to my remote repo. The -f forced the push since the two repositories were different. Once all of that was done I was then able to submit a much cleaner pull request with only my changes. Whew! This all took a bit longer than expected and was preventing Lukas from leaving but it's fixed and I am thankful and relieved!

I walked down to Collective Agency, a co-working space, where Andrew works a couple of days a week with some other Portland GSG employees. He usually would head home after lunch but has been staying there until I get done so we can go home together. I'm pretty sure I talked his ear off about my day.

We got home, went across the street to check out Jason and Alice's beautiful new marmoleum floor in their basement. Wayne picked a bunch of strawberries from our garden. It's weird that we are still getting them. These are the same plants that have been there for a while and they sure didn't produce this long last year.

<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/2014-09-18-18.21.12.jpg"><img class="size-medium wp-image-133" src="http://lisa.hewus.com/wp-content/uploads/2014/09/2014-09-18-18.21.12-225x300.jpg" alt="Strawberries and Wayne" width="225" height="300" /></a>

Andrew made me a tasty muddled strawberry and mint fizzy water.

<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/fizzydrink.jpg"><img class="aligncenter size-medium wp-image-134" src="http://lisa.hewus.com/wp-content/uploads/2014/09/fizzydrink-168x300.jpg" alt="Fizzy Drink" width="168" height="300" /></a>

Today I learned SO many things! Git stuff, Vim stuff, Mozmill stuff, Why we can't have nice things (utf-8, dates, and names), and MOOM! Definitely check out <a title="It's rad!" href="http://manytricks.com/moom/">MOOM</a>.
