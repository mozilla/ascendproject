---
layout: post
title:  "Bash Drills"
date:   2014-10-03
categories: resources
---
This is a compiled series of exercises from Zed Shaw's [Command Line Crash Course] [1] so we have a one hour drills session to do together. 

Making Directories (mkdir)
--------------------------
	mkdir temp

	mkdir temp/stuff

	mkdir temp/stuff/things

	mkdir -p temp/stuff/things/fran/jo/alice/jane

	mkdir temp/stuff/"I have fun"

Make a ton of directories
-------------------------
	for i in {1..20}; do mkdir temp/folder$i; done

	for i in {1..20}; do mkdir temp/folder$i/dir$i; done

Check your work
---------------
	ls -lR temp


Changing Directories (cd)
-------------------------
	cd to the jo directory with one command.

	cd back to temp with one command, but not further above that.

	Find out how to cd to your "home directory" with one command.

	cd to your Documents directory, then find it with your file browser.

	cd to your Downloads directory, then find it with your file browser.

	Find another directory with your file browser, then cd to it.

	Remember when you put quotes around a directory with spaces in it? You can do that with any command. For example, if you have a directory I Have Fun, then you can do: cd "I Have Fun"

List Directory (ls)
-------------------
(Start at ~ or $HOME)

	cd temp
	ls

	cd stuff
	ls

	cd things
	ls

	cd fran
	ls

	cd jo
	ls

	cd alice
	ls

	cd jane
	ls

	cd ..
	ls

	cd ../../../
	ls

	cd ../../
	ls

	pwd

Moving Around (pushd, popd)
---------------------------
(Start at ~ or $HOME)
<pre>
$ cd temp
$ mkdir -p i/like/icecream
$ pushd i/like/icecream
~/temp/i/like/icecream ~/temp
$ popd
~/temp
$ pwd
~/temp
$ pushd i/like
~/temp/i/like ~/temp
$ pwd
~/temp/i/like
$ pushd icecream
~/temp/i/like/icecream ~/temp/i/like ~/temp
$ pwd
~/temp/i/like/icecream
$ popd
~/temp/i/like ~/temp
$ pwd
~/temp/i/like
$ popd
~/temp
$ pushd i/like/icecream
~/temp/i/like/icecream ~/temp
$ pushd
~/temp ~/temp/i/like/icecream
$ pwd
~/temp
$ pushd
~/temp/i/like/icecream ~/temp
$ pwd
~/temp/i/like/icecream
$
</pre>

Copy A File (cp)
----------------

(Start at ~ or $HOME)

	cd temp
	cp iamcool.txt neat.txt
	ls

	cp neat.txt awesome.txt
	ls

	cp awesome.txt thefourthfile.txt
	ls

	mkdir something
	cp awesome.txt something/
	ls

	ls something/

	cp -r something newplace
	ls newplace/

	Use the cp -r command to copy more directories with files in them
	Copy a file to your home directory or desktop


Moving (mv)
-----------
(Start at ~ or $HOME)

	cd temp
	mv awesome.txt uncool.txt
	ls

	mv newplace oldplace
	ls

	mv oldplace newplace
	ls


	Move a file in the newplace directory to another directory then move it back.


[1]: http://cli.learncodethehardway.org/book       "Command Line Crash Course"