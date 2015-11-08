# choovinfeeds-openwrt
choovinfeeds-openwrt packages

Openwrt Packages for gas-meter gateway

our gas-meter gateway  pacjages for use on Openwrt hardware. This repository is to be used as feed in the openwrt buildroot.

Casual Build Instructions

Create a buildroot as per instructions on the openwrt website.

Add this repository as a feed in feeds.conf

$ src-git choovinfeeds https://github.com/choovin/choovinfeeds-openwrt

or (if checked out locally)

$ src-link choovinfeeds /choovinfeeds-openwrt/openwrt-feeds

Update feeds and install packages in the buildroot
$ ./script/feeds update -a

$ ./script/feeds install -a

Generate the menuconfig and select the packages you wish to build under the choovinfeeds section.
