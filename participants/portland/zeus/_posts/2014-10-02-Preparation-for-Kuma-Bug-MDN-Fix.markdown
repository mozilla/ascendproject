### Thursday Oct 2
   ---------------
So Ubuntu is my new operating system for the next days. And it crashed and crashed. After a day of super heat and sweaty walk, in a strange place. After finding a cyber cafe to join in. Not to say that finding fast connection, was very challenging. 

- Installed vidyo. Made local test. 
------
I made an run to install Vidyo. For  Ubuntu? I wondered. 
I decided to list the steps I took today as a reference. 


~~~
                sudo dpkg -i VidyoDesktopInstaller-ubuntu-TAG_VD_3_0_4_001.deb
~~~

- Logged into Smuxi chat IRC 
--------
OK, that part is accomplished, Now I don't have an ICR client, Colloquy is what we used for MAC, well they don't do a MAC version. 

I like mibbit. and it cool. IRC Cloud is cool too. I installed Smuxi and it works fine because it has intergration messages like Colloquy does for MAC.

~~~
                sudo apt-get install smuxi
~~~

Build Firefox in Ubuntu
-------

- Non bug related I was able to re-download the code to build Firefox and starting doing the mach build
~~~
                python boostrap.py
~~~
                     this returned errors at the end
~~~
                git clone gecko-dev
~~~
Make configuration file for the build. 
~~~
                ac_add_options --enable-debug > mozconfig 

                ac_add_options --disable-optimize > mozconfig
~~~
            
First Bug Comment
------            
- Read some comments and invested in helping and learning what are we doing today.
https://bugzilla.mozilla.org/show_bug.cgi?id=632204

-- Wrote ideas for bug comment
```
    Bug: 632204
```
    Comment:
```
        "Dear bug 632204 I would like to end your existence by boosting my  knowledge in removing you from the code base. I know who you are, I will  find you, and I will erase you. ( Quote from movie ). (Frantic music  plays here)." 
```
       

       I don't know what else to say. 

       
```
        "Dear sir/Madam, I am Coderburg Vugs-Squasher Prince the Third, I  address this email from a lonely island in Africa, I address this letter  to confirm that you are the lucky person to receive this email about  deleting one in a million bugs. If you are so kind and please provide  access to the richness of deleting this bug number 632204" 
```
       

       

       or

       
```
       "Here, here, I would like to work on this 632204. Thank you."
```
       
Getting back to my bug MDN Captcha for HoneyPOT
-----  

- Re-dowloading process continues from my source code from my own forked GIT  from the mozilla project
- Attended conference online with vidyo with 
- joined the IRC for this bug #mdndev 
- followed the compilation instructions  http://kuma.readthedocs.org/en/latest/installation-vagrant.html


> -   Install VirtualBox 4.x from http://www.virtualbox.org/
>
> -  Go to https://www.virtualbox.org/wiki/Linux_Downloads
>
> -   Selected Trusty 14.04 386 for download
>
> -   in terminal 
>
> 
~~~
    cd Downloads

    sudo dpkg -i virtualbox-4.3_4.3.16-95972~Ubuntu~raring_i386.deb
~~~
> -    Install vagrant >= 1.6 using the installer from vagrantup.com
>
> -  Go to http://www.vagrantup.com/downloads.html
>
> -   Selected 32 bits Ubuntu 
>
> -    In terminal 
>
~~~
    cd Downloads

    sudo dpkg -i vagrant_1.6.5_i686.deb 
~~~
> -    Install the vagrant-vbguest plugin.
> 
> -   Go to https://github.com/dotless-de/vagrant-vbguest
>
> -    Selected Vagrant > 1.1
>
> -   In terminal
~~~
     vagrant plugin install vagrant-vbguest
~~~
> -    Fork the project. (See GitHub and Webdev Bootcamp)
>
> -   In terminal 
~~~
    cd ~/Sites/ 

    git clone https://github.com/zeusintuivo/kuma

    cd kuma

    git remote add mozilla git://github.com/mozilla/kuma.git

    git submodule update --init --recursive
~~~
>
>  -  2. Create a branch for a bug ($ git checkout -b new-issue-888888)
>
> -    In terminal 
~~~
    git checkout -b new-issue-632204

    git submodule update --init --recursive
~~~
>
> -    3. Copy a vagrantconfig_local.yaml file for your VM:
>
> -    In terminal 
>
~~~
    cp vagrantconfig_local.yaml-dist vagrantconfig_local.yaml
~~~
>
> -    4. Start the VM and install everything. (approx. 30 min on a fast net connection).:
>
> -    In terminal 
~~~
    vagrant up
~~~
```
    WAIT 30 minutes

    WAIT and WAIT
```
> -    ^ This crashed in my case:
~~~
                            "
                            It appears your machine doesn't support NFS, or there is not an
                            adapter to enable NFS on this machine for Vagrant. Please verify
                            that `nfsd` is installed on your machine, and try again. If you're
                            on Windows, NFS isn't supported.
                            "
~~~
>
> What do I do ? I Google it 

~~~ 
Googled: "It appears your machine doesn't support NFS, or there is not "
~~~
>
>
>     Found this: https://github.com/edx/edx-platform/wiki/Simplified-install-with-vagrant
>
> -   In terminal
~~~
    sudo apt-get install nfs-common nfs-kernel-server
~~~
    Then
~~~
    vagrant destroy -f && vagrant up
~~~
```
    My connection dropped and the install of the vagrant up

    did not finish.
````
>    - Errors showed up
>
>    *cont next day

~~~
- end of day -
~~~