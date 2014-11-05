---
title: How to edit DVD files with Adobe Premiere
author: Matthew Butler
layout: post
permalink: /how-to-edit-dvd-files-with-adobe-premiere
categories:
  - Uncategorized
---
Once in a while you want to grab video from a DVD and edit it in Adobe Premiere.  Here&#8217;s how to do it in Windows.

Use [DVD Decrypter][1] to rip the DVD into a series of Video Object files (.vob).  Find the .vob that has the section you want.

You can&#8217;t import .vob files into Premiere directly due to sketchy timecode issues.  That means you need to convert it.

Use [MPEG Streamclip][2] to convert your .vob to something more appropriate like .dv or .avi.  Before you install MPEG Streamclip, you&#8217;ll want to uninstall Quicktime completely and install [Quicktime Alternative 1.81][3].  Make sure you get version 1.81 specifically.

Once MPEG Streamclip is installed then just open your .vob file.  It will ask if you want to fix the file.  You do.

You should see the video at this point.  From here, export to your favorite format using the options in the File dropdown menu.

Import this newly converted file into Premiere and do your magic!

 [1]: http://www.dvddecrypter.org.uk/SetupDVDDecrypter_3.5.4.0.exe
 [2]: http://www.squared5.com/
 [3]: http://filehippo.com/download_quicktime_alternative/2615/