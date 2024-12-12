---
title: How to fix computer booting to busybox / initramfs
author: justin
description: Fixing linux machine booting to busybox / initramfs shell.
layout: post
---
# Fix initramfs
##### The cause
Usually a SSD or HDD is starting to die and the machine can't find the operating system to boot. Sometimes you may have errors on your disk from read and writing to many files, this can also affect USB drives.

##### The fix
1. run `ls` to list all drive locations mine was a nvme drive and you should have an output of something like `/dev/nvme0np1` if it's a USB thumb drive it will read something like `/dev/sda`
2. run `ls -1 /dev/nvme*` to produce the full list of paths on the nvme drive, change nvme to sda for a usb drive.
3. run `fsck /dev/nvme0n1p1` until whatever number it ends with nvme0n1p4 for instance one will be your file system and it may ask to fix corrupted files or errors just press y to fix them.
4. simply type `exit` your system should now boot to the login screen, log in and use your system. I personally do a reboot to see if the issue is fixed once logegd in.
