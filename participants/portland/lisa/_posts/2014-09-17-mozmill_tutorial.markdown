---
layout: post
title: "Mozmill Tutorial"
date: 2014-09-17
categories: lisa
---
Mozmill is an automated testing framework. If you have run any Moztrap tests you were doing those manually. This is a way to have the computer do many of those tests automatically for you. We still need human testers though! We can figure out all sorts of creative ways to break things but the computer can only test things in the way it was programmed.

This tutorial is compatible with Mac OS X 10.9 running Python 2.7

#Installing Mozmill

If you have pip installed simply run "sudo pip install mozmill" and enter your password.

<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill001.png"><img class="alignleft size-medium wp-image-140" src="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill001-300x146.png" alt="installMozmill001" width="300" height="146" /></a>


Otherwise run the following commands in order making sure each step completes with no errors:

curl -O https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py

<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill002.png"><img class="alignleft wp-image-141 " src="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill002.png" alt="installMozmill002" width="583" height="194" /></a>


sudo python ez_setup.py (requires your password)  
easy_install pip  
pip install mozmill

<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill0031.png"><img class="alignleft size-full wp-image-143" src="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill0031.png" alt="installMozmill003" width="348" height="140" /></a>


Now test to make sure Mozmill has been installed properly by typing - mozmill --v

This should show you the version number and means you have mozmill installed properly.

<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill004.png"><img class="alignleft size-full wp-image-144" src="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill004.png" alt="installMozmill004" width="350" height="169" /></a>


#Clone Test Suite and Automation

Navigate to the directory where you would like to clone the following repositories (/projects, /sites, etc.)  
Clone the test suite repository by typing: git clone https://github.com/mozilla/qa-mozmill-tests  
Clone the automation repository by typing: git clone https://github.com/mozilla/mozmill-automation  

#Set Up Automation

Change directories into mozmill-automation - cd mozmill-automation  
Checkout the hotfix-2.0 branch - git checkout hotfix-2.0  
Run sudo python setup.py develop  
  
<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill0051.png"><img class="alignleft size-full wp-image-147" src="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill0051.png" alt="installMozmill005" width="553" height="171" /></a>

Now if you type testrun_ and tab twice you should see all of the testrun commands available  

<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill006.png"><img class="alignleft size-full wp-image-148" src="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill006.png" alt="installMozmill006" width="492" height="171" /></a>

#Run Automated Functional Tests

Now you are finally ready to run your automated tests! You will need to know the path to the version of Firefox you want to test. The --report portion of the command is the location of the Mozilla dashboard where the results will be sent. The example path may not be where your version is located.  

Run the following command with your Firefox.app path and then the test suite will launch.  

testrun_functional --report=http://mozmill-crowd.blargon7.com/db/ %path_to_firefox% (on Mac to .app)

<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill007.png"><img class="alignleft size-full wp-image-149" src="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill007.png" alt="installMozmill007" width="994" height="94" /></a>

This will take a bit of time but be patient. Take a break or sit and watch in amazement.  

<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill008.png"><img class="alignleft size-full wp-image-152" src="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill008.png" alt="installMozmill008" width="982" height="261" /></a>

When testing has completed you will be given a URL with a unique ID at the end.  

<a href="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill0091.png"><img class="alignleft size-full wp-image-151" src="http://lisa.hewus.com/wp-content/uploads/2014/09/installMozmill0091.png" alt="installMozmill009" width="872" height="177" /></a>


To view your report, put your unique ID at the end of this user-friendly URL (e.g. http://mozmill-crowd.blargon7.com/#/functional/report/2f982f72826307fed840a3b11c3b7f46 ) *this link works for testrun_functional runs.  

To claim your  badge for this tutorial PM me in #ascend with your unique ID and I will award it to you.

Tutorial based on instructions via <a href="https://developer.mozilla.org/en-US/docs/Mozilla/QA/Mozmill_tests" target="_blank">this Mozilla webpage</a>.
