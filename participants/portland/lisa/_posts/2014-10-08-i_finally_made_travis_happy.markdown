---
layout: post
title:  "I Finally Made Travis Happy"
author: Lisa Hewus Fresh
date:   2014-10-08
categories: lisa
---

I am definitely not a true Portlander because I should be lying and saying what horrible weather we are having but I can't. Today was incredible! I was up early and out the door but Roberto and Frankie were still sleeping so I wouldn't be able to say goodbye. I'll see them again soon though since they plan on moving here!

I was excited to get to class. Well I'm always excited to get to class but I was extra excited today because we got our computers back and it would be business as usual. I really wanted to get back to working on <a href="https://travis-ci.org/" target="_blank">Travis-CI</a> and hopefully get a clean build. I wasn't, however, looking forward to messaging my code reviewer but I knew I needed to rip off that band-aid and say something. Check-ins were mostly great but some people were not having the best of days.

We had about an hour to work on our bugs and such so I got busy and started chipping away at the errors I was getting. I FINALLY figured out the correct file path for images and blog posts and that was a huge step forward. I also messaged my code reviewer and he did take some time to look at the code. He also gave me a different path to go down for this bug so it may not be dead after all! I was stressing about there being a problem but this just might work out.

Kronda came in and went over more features of Wordpress and I really appreciated it. She gave us all sorts of advice and showed us so many helpful things! She covered plugins, themes, spam, SEO and a lot more. It's apparent I have barely scratched the surface of Wordpress but Kronda is a wealth of information.

After Kronda's talk we got back to our bugs. I just plodded along working on error after error until it was lunch time. Most everyone left but I was straggling and running one more rake test so I ended up meeting up with Kronda, Lukas and Katt by the elevators. The four of us went to <a href="http://www.losgorditospdx.com/locations/perla/" target="_blank">Los Gorditos.</a> I had vegan taquitos with potatoes and soy curls (a terrible name for a delicious food). The food was really, really good but the company was great.

Back to Travis! I was down to about 25 errors! I worked on them and made the penultimate fix! The last fix was one I needed to go over with Lukas since it was above the participants directory. Once that change was made I pushed to Github and.......fail! Grrr....now it was throwing a certificate error on the Moztrap site. I can't control that one so I added an ignore in the Rakefile and ran another rake test. Holy shit it finally passed! Only 18 builds later it passed! Look at how beautiful this is.

<a href="http://lisa.hewus.com/wp-content/uploads/2014/10/Travis_CI_Passed.png"><img class="aligncenter size-full wp-image-244" src="http://lisa.hewus.com/wp-content/uploads/2014/10/Travis_CI_Passed.png" alt="Travis Passed" width="825" height="311" /></a>
<a href="http://lisa.hewus.com/wp-content/uploads/2014/10/Travis_CI_Passed2.png"><img class="aligncenter size-full wp-image-243" src="http://lisa.hewus.com/wp-content/uploads/2014/10/Travis_CI_Passed2.png" alt="Travis Passed" width="802" height="209" /></a>

Of course this is just on my Github repo so it still has to be merged in and there will be a tiny bit of configuration on the actual <a href="https://github.com/mozilla/ascendproject" target="_blank">Ascend repo</a> but it should work with not too much trouble. Now I need to write a best practices so participants will know how things should be formatted. Having Travis running will allow them to see if their pull requests can merge in without causing a build failure.

I wanted to start writing the best practices but it was time to do some more practice exercises for our talks. Katt was able to join us for this one! We had to pair up and write up a talk about our first pet or the lack thereof. This was intended to make it no pressure and about something fairly easy. We also had to record ourselves giving the talk and then watch it with our partner and critique it. Writing it up was not bad at all. Recording it was another story. I have a lot of work to do there. I have to find a way to be even a little comfortable with the way I look and sound. Lots of work there. Anyway, all in all it was a great day in class.

I headed home, had an uneventful ride home on the Max, walked part way home with my neighbor and then stopped to pet BowWow (a tiny dog with quite the adventurous life) and talk with Maggie and Eric his owners. As I got to our block I saw Wayne, Alice and Jason outside in front of our house with Lily and Ladybug. The dogs saw me and came running as fast as they could, both ridiculously happy to see me and very interested in the scent of BowWow on my hands. It was another one of those perfect movie moments. I swear my life is too good to be true.

I barely had time to put my stuff down and say hello to the rest of my family before we had to run to the airport and pick up our friend Michael. He lives in Massachusetts and was flying in for an optometrist conference. He hadn't ever visited Portland before and was looking forward to checking it out. We met Josh and Michael in Lake Havasu and became pretty close to them. We'd love it if they moved here but they have since adopted two amazing little boys and are very settled where they are.

We came back home, gave Michael a quick, partial tour of the house before Alice walked over and then walked around the corner to the Thai place for dinner. Jayde didn't want to join us since she's not a fan of Thai but Natale, Wayne, Andrew, Alice, Michael, and I had a great dinner and laughed a lot. Michael was getting tired so we headed back home. As we were walking, Alice and Natale heard something. Alice saw something she thought was a bag so walked toward it but then it moved causing her to jump and scream, startling the rest of us. I suppose you had to be there but it was hilarious! Oh, it ended up being a cat.

Today I learned what <a href="http://www.merriam-webster.com/dictionary/emesis" target="_blank">emesis</a> means and it turns out Alice doesn't like when we talk about it during dinner. Naturally we talked about it a lot.
