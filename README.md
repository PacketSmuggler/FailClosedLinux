# FailClosedLinux
Fail closed Linux configuration using OpenVPN, works with Cryptostorm, as well as other providers.

Assumptions:

These instructions assume you're going to build your first system using VirtualBox. A common motivation for reading these insructions is creating a torrent seedbox using a VPS. The differences between the two environments are minor.

http://virtualbox.org

There are a lot of Linux distros out there and for some reason there is a lot of attention on Mint. I don't like Mint for the simple fact that the graphical login defaults to requiring reentry of userid, and I'm forever showing passwords with it. These instructions should work anywhere, but I reach for 64 bit Lubuntu when I need a small Linux distro. If your processor will only virtualize 32 bit operating systems there is a Lubuntu for that as well.

http://lubuntu.net

There are some packages you'll need before you get started. You'll use git to pull configurations for Cryptostorm and gcc and make are required to install the VirtualBox guest utils. 

* apt-get install gcc
* apt-get install git
* apt-get install make


