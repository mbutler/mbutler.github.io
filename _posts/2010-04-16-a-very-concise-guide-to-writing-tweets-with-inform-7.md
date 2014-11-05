---
title: A very concise guide to writing tweets with Inform 7
author: Matthew Butler
layout: post
permalink: /a-very-concise-guide-to-writing-tweets-with-inform-7
categories:
  - Uncategorized
---
Yesterday I wrote that tweets, being archived for future generations, could be enhanced by making them Inform 7 compliant. Not that everything on Twitter should be written in Inform, only that it would be very interesting to have a piece of interactive fiction added to this archive. Since tweets are 140 characters or less, they are roughly the same size as one line of code. Organizing a jumble of code could be extremely challenging, so they would need to be kept fairly basic.

To start, the hash tag #inform7 should be used at the beginning of your tweet to &#8220;initialize&#8221; it and make it available to the potential code base.  If you use Twitter this shouldn&#8217;t be out of the ordinary for you.  Similarly, if you use a language like perl or python, the convention of starting your code a # and a path to the interpreter shouldn&#8217;t be weird at all.

Inform code can be quite complex and describe very sophisticated relationships. For the purposes of using it for tweets it should be kept minimal, so I&#8217;ll only go over the very basics. However if you want to learn more advanced techniques, you can always read through the [Inform 7 manual][1] for a complete guide to this interesting language.

Inform resembles English sentences.  Each line of Inform code is an &#8220;assertion&#8221; or a rule about the world you&#8217;re creating.  The world starts as a formless, empty void; you must create every rule for how your story works.  There are, however, built-in standard rules so you don&#8217;t have to describe the laws of physics, etc. for every story.   If you&#8217;re familiar with programming languages you probably know about [primitive data types][2].  In Inform, the primitives are present tense verbs.  The built-in primitives for Inform are the following:

*   <span style="font-family: lucida grande,geneva,arial,tahoma,verdana,helvetica,helv; font-size: x-small;"><em>to be</em></span>
*   <span style="font-family: lucida grande,geneva,arial,tahoma,verdana,helvetica,helv; font-size: x-small;"><em>to have</em></span>
*   <span style="font-family: lucida grande,geneva,arial,tahoma,verdana,helvetica,helv; font-size: x-small;"><em>to carry</em></span>
*   <span style="font-family: lucida grande,geneva,arial,tahoma,verdana,helvetica,helv; font-size: x-small;"><em>to wear</em></span>
*   <span style="font-family: lucida grande,geneva,arial,tahoma,verdana,helvetica,helv; font-size: x-small;"><em>to contain</em></span>
*   <span style="font-family: lucida grande,geneva,arial,tahoma,verdana,helvetica,helv; font-size: x-small;"><em>to support</em></span>

You can create your own verbs, but for now you should only use these types.

So let&#8217;s write a &#8220;hello world&#8221; Inform 7 tweet!  Remember to start with the hash tag, use the primitive data types (for now), keep it present tense, and keep it under 140 characters total.

> #inform7 Iowa City is a room.

Not very exciting, but it&#8217;s a great start.  Keeping with the interactive fiction convention, a &#8216;room&#8217; is the term for an area of space.  You can use the term &#8216;region&#8217; to describe a larger area that contains a group of rooms.

 [1]: http://inform7.com/learn/man/index.html
 [2]: http://en.wikipedia.org/wiki/Primitive_data_type