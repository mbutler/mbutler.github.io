---
title: How to fix the Windows boot loader
author: Matthew Butler
layout: post
permalink: /how-to-fix-the-windows-boot-loader
categories:
  - Uncategorized
---
Sometimes when you&#8217;re messing around with dual booting OSes, you screw up the boot loader.  Eh, it happens.  It&#8217;s sort of the desktop computing equivalent to being waterboarded; you feel an immediate sense of panic and dread but are not actually in any danger.  The boot loader is a BIOS-like menu that allows you to boot your computer into whatever operating systems you have installed.  In my case, I&#8217;m splitting my time between Ubuntu 10.04 and Windows 7.  If you install Ubuntu, it automatically installs the GRUB boot loader which allows you to then drop into Windows 7&#8217;s own loader.  If your computer somehow &#8220;freezes&#8221; on the Windows startup screen you probably need to fix it.  It&#8217;s panic-inducing because it seems you&#8217;re locked out of Windows forever&#8230;. how can you fix Windows if you can&#8217;t get into Windows?!?!

You need to get to a command prompt.  Windows will either run a repair utility which gives you this option or you can run it from the Windows disc.

Once you&#8217;re at the prompt, type this:

<div class="codesnip-container" >
  bootrec /fixmbr
</div>

Press Enter.

Now type this:

<div class="codesnip-container" >
  bootrec /FixBoot
</div>

That&#8217;s it!  Restart your machine and you should be good to go.  That was easier than you thought it&#8217;d be.