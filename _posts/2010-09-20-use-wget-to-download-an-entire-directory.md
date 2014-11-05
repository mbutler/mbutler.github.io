---
title: Use wget to download an entire directory
author: Matthew Butler
layout: post
permalink: /use-wget-to-download-an-entire-directory
categories:
  - Uncategorized
---
Here&#8217;s a simple way to grab and entire directory:

On the command line type

<div class="codesnip-container" >
  wget -r -c -np -e robots=off &#8211;random-wait &#8211;limit-rate=80k <URL>
</div>

That will pull everything recursively without moving up the directory path. If you want to use Coral Cache, tack nyud.net after the URL. Example: http://arcarc.xmission.com.nyud.net/

THAT IS ALL