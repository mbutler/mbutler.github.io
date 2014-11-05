---
title: Music library metadata cleaning project underway
author: Matthew Butler
layout: post
permalink: /music-library-metadata-cleaning-project-underway
categories:
  - Uncategorized
---
A few days ago I decided it was high time to finally organize the mess that is my music library.  I don&#8217;t have the largest mp3 collection but it&#8217;s still a 100+ GB library, half of which is single-file downloads from the Napster era when we didn&#8217;t have good online databases to correctly tag files as they were ripped from CD.  Most of these files only have the &#8216;Artist&#8217; and &#8216;Title&#8217; title fields filled in, missing the &#8216;Album&#8217;, &#8216;Genre&#8217;, and &#8216;Album Artist&#8217; fields as well as album artwork.  Many of them are only known by their filename and have no metadata at all (*gasp*).

I found an incredible program called [TuneUp][1], which uses the same acoustic fingerprinting technology that Shazam uses to magically listen to a song and tell you what it is.  It&#8217;s not perfect, meaning you have to go through your library file-by-file or album-by-album and verify it&#8217;s correct, but it saves untold hours of work.  It will clean the ID3 tags and standardize it to a Gracenote database then download album artwork when possible.

It was a little bit sad to wipe out the uniquely messy file names  that littered my library.  I found myself slightly wistful replacing the crufty metadata that represented a decade of music downloading with a standardized naming convention.  Some of the songs that I loved dearly were only known to me by such scant information as 02\_djrectangle\_shadowboxin, for example.  It was still the same song, but having it look like everybody else&#8217;s database record made me feel kind of conformist and weird, like I didn&#8217;t do the work to find this music myself.  It was evidence of the early days of file sharing (and many people using my computer to download) and I erased that history in the name of usability.  Fuck it, it&#8217;s 2011.

The tears dried quickly as I realized what I lost in history I gained in overwhelming completeness.  Songs I thought I knew were discovered to be by other artists, obscure mix tapes became evident to me, DJ productions I would have never known were learned, and all of those &#8216;Unknown Artist Track 01&#8242; files suddenly became real songs once again.  Not to mention the thousands of gray boxes that dominated my library became filled with beautiful album covers.  Cover flow in iTunes is actually useful to me now!

One of the best discoveries in this project is the &#8216;Album Artist&#8217; field of ID3.  It is different from the &#8216;Artist&#8217; field in that it easily ties a group of songs together into a unified album.  For example, I have an 8 album set of World music called The Secret Museum of Mankind.  The metadata for this was fairly clean before, except that it was broken into hundreds of individual albums based on Artist.  NOT USEFUL.  By simply adding the value &#8216;Various Artists&#8217; to the &#8216;Album Artist&#8217; field, it tied them all up together into 8 easy-to-use albums just as it was originally intended.  Doing this to all of the messy compilations and mixtapes has done wonders to my iPod.

I&#8217;ve invested about 20 hours into this enormous project so far and estimate I&#8217;m about 40% done.  This is a decade in the making though and worth every minute I&#8217;ve spent tagging.

 [1]: http://www.tuneupmedia.com/index.php