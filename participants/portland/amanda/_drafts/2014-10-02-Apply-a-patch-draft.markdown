---
layout: post
title:  "Apply a Patch using Virtual Box"
author: amanda houle
date:   2014-Sept-12
categories: amanda
---

1. sudo apt-get install git (use password "firefox-dev" w/o the quotes)
git clone into home directory
change to mozilla-central
****  Google this - how to apply a patch *******
figure out how to get the patch into the build
be in moz-cen and give command to apply patch

Don't pay any attention to stuff below this line
2.  git apply amanda.patch
3. -- stat amanda.patch  (detects errors)
4. git am --signoff < amanda.patch (applies patch)