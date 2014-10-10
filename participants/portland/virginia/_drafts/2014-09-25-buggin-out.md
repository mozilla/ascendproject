---
layout: post
title:  "Buggin' Out!"
date:   2014-09-25
categories: virginia
---

We're about halfway through this program now (holy crap), and our goal by the end is to have committed at least one patch of code, so it's time to find a bug to hack!

At first I was looking into whether I might be able to fix one of the bugs that I reported last week, but two were just broken links which are still "unconfirmed," and [the other one](https://bugzilla.mozilla.org/show_bug.cgi?id=1068896) was quickly resolved by a MozTrap developer before I could work on it, though I may not have been able to fix that one on my own anyway.

So using a Bugzilla search for recent, unassigned, non-Firefox OS, good-first-bugs, I found:
[Bug 897382 - Include the update channel in the report even for failed update tests](https://bugzilla.mozilla.org/show_bug.cgi?id=897382).

I've been interested in QA for some time now, and I enjoyed running a few Mozmill tests last week. So of course I already have Mozmill installed, and the bug states very clearly what code needs to be fixed, so it seems doable.
