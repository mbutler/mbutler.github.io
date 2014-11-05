---
title: How to reinstall the grub bootloader
author: Matthew Butler
layout: post
permalink: /how-to-reinstall-the-grub-bootloader
categories:
  - Uncategorized
---
If you followed my post [How to fix the Windows bootloader][1] and you are also dual booting into Ubuntu, you&#8217;ve probably noticed by now that the Windows bootloader fix wipes out grub.  Never fear, it can be fixed.

First, boot into your Ubuntu Live disc.  This will give you access to your devices, files, and a more importantly, a terminal.

If you&#8217;re using Ubuntu 9.10+ then you&#8217;re using grub2.  Anything earlier and you&#8217;re either using grub or grub legacy.  This little tutorial will only cover grub2 &#8212; sorry.

Ok.  Mount the drive with your Ubuntu installation.  Go to Places and choose your partition.  Verify this partition in the terminal with this command:

<div class="codesnip-container" >
  mount | tail -1
</div>

You should see something like this:

<div class="codesnip-container" >
  /dev/sda2 on /media/0d104aff-ec8c-44c8-b811-92b993823444 type ext4 (rw,nosuid,nodev,uhelper=devkit)
</div>

Copy /media/0d104aff-ec8c-44c8-b811-92b993823444 (whatever yours is) using Ctrl-Shift-C

Now reinstall grub by entering this into terminal:

<div class="codesnip-container" >
  sudo grub-install &#8211;root-directory=/media/0d104aff-ec8c-44c8-b811-92b993823444 /dev/sda
</div>

Obviously, you&#8217;ll want to paste in your own /media/ path you copied from before.  Don&#8217;t use the example path above!

You should see an Installation Complete message.  YAY!

A million things can go wrong with this, so dig around if you have problems.  But in the sage words of the wise IT guru&#8230; &#8220;Works for me!&#8221;

 [1]: http://mattbutler.net/?p=222