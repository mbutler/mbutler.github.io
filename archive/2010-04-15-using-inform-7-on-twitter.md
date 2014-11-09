---
title: Using Inform 7 on Twitter
author: Matthew Butler
layout: post
permalink: /using-inform-7-on-twitter
categories:
  - Uncategorized
---
<a href="http://www.loc.gov/tweet/how-tweet-it-is.html" target="_self">It was announced today</a> that the Library of Congress will digitally archive all public tweets. Every public tweet that&#8217;s been sent since 2006 and every public tweet in the future will be stored on their servers. Of course, your private and reserved messages will remain private, but there is now a serious public archive of our messages to each other. It&#8217;s uncertain whether the Twitter archive will be the *Epic of Gilgamesh* of the year 6000 A.D., but it does have interesting implications for the stories we&#8217;re tweeting at the moment.

It&#8217;s likely this Library of Congress archive will be able to survive a major catastrophe and remain searchable for generations. Not that the United States government isn&#8217;t capable of losing massive amounts of data or that Twitter isn&#8217;t up to the job, but having some very smart archivists working on the problem is a big help. There is a national strategy being formulated right now by the [National Digital Information Infrastructure and Preservation Program][1] to:

> collect, preserve and make available significant digital content, especially information that is created in digital form only, for current and future generations.

There are a lot of great tools for digital preservation, such as the [LOCKSS][2] system from Stanford University Libraries. I trust the Library of Congress is using the best techniques possible to insure our great-great-great-great grandchildren have access to their ancestors digital writing. However, just in case, you should store all of your tweets in the cloud *and* locally so if the Library of Congress loses all of the data in 2,000 years we can piece it together from everyone&#8217;s local cache. FYI.

So what kind of story are we writing about ourselves now that will be studied by future archeologists? Is there a more structured way of writing our tweets to make their job easier?

Tweets, I&#8217;m sure you know, are limited to 140 characters or less. This may seem like an arbitrarily short character string, but it&#8217;s the standard length of most text messages transmitted over cellular networks. Billions of people, [ including those in developing countries][3], have access to cell phones and 140 character messages. It is quickly becoming the standard size to encode one human thought.

This is interesting from a literary standpoint as well. Literature is essentially made from human thoughts encoded into character strings then transcribed in some manner. Poets have been able to manipulate these in elegant and nuanced ways to evoke deep emotion. Take, for instance, this poem:

> so much depends  
> upon
> 
> a red wheel  
> barrow
> 
> glazed with rain  
> water
> 
> beside the white  
> chickens.

A beautiful and terse piece of literature encapsulated into exactly 102 characters, leaving enough room for metadata. If you count up all of the *letters and spaces* you&#8217;ll notice it only adds up to 92 characters. This is because at the end of each line there is a [line break][4] that uses a character, adding an additional 10 characters total to represent William Carlos Williams&#8217; very deliberate and thoughtful typewriter carriage returns. This is a crucial part of *The Red Wheelbarrow *and the poem fails without those 10 characters of code. Therefore we need to encode and pay special attention to subtle changes intended by the author. Here&#8217;s what the poem looks like if we use the \n newline character (from the C programming language) to represent his typewriter carriage returns:

> The Red Wheelbarrow\nby William Carlos Williams\n\nso much depends\nupon\n\na red wheel\nbarrow\n\nglazed with rain\nwater\n\nbeside the white\nchickens.

It is now in a convenient format to send over the network. Whatever is used to render the text on the other end will move the text to the next line whenever it encounters \n

A deliberately strict use of language can be described as [constrained writing][5], a literary technique in which the writer is bound by some condition that forbids certain things or imposes a pattern. This was used by groups such as [Oulipo][6], a gathering of French poets and mathematicians who devised a &#8220;workshop of potential literature&#8221; in the 1960&#8217;s to invent new structures and patterns. For example there was:

> **Snowball**
> A poem in which each line is a single word, and each successive word is one letter longer.

Working within this constraint requires creativity and wit to pull off successfully. As does **this** constraint:

> **Tweet**
> A message less than or equal to 140 characters in length.

You can see where I&#8217;m going with this. By using a tweet as a form of constrained writing we have created the &#8220;potential literature&#8221; to describe a link between human thought and machine language. Micro-format fiction and haikus are nothing new and have been explored thoroughly in Japan where phone novels, known as [keitai shousetsu][7], account for many of the top-selling titles. These individual chapters (text messages) are typically much larger than the 140 character limit of Twitter, however, so more information can be transmitted at once.

If computers were communicating with each other via tweet they could easily encode much more information in the same character length. For example, [it&#8217;s been demonstrated][8] that a recognizable image of the Mona Lisa can be encoded using Chinese characters. The tweet looks like this:

> 圑嘌婂搒孵怤實恄幖戰怴搝愩娻屗奊唀唭嚟帧啜徠山峔巰喜圂嗊埯廇嗕患嚵幇墥彫壛嶂壋悟声喿墰廚埽崙嫖嘵奰恛嬂啷婕媸姴嚥娐嗪嫤圣峈嬻尤囮愰啴屽嶍屽嶰寂喿 嶐唥帑尸庠啞彐啯廂喪帄嗆怠嗙开唅恰唦慼啥憛幮悐喆悠喚忐嗳惐唔戠啹媊婼捐啸抃岖嗅怲幀嗈拀唹坭嵄彠喺悠單囏庰抂唋岰媮岬夣宐彋媀恦啼彐壔姩宔嬀

It&#8217;s a highly compact, elegantly restrained piece that could transmit flags or icons, but impossible for a human to write quickly on her own. We know that we need special codes to convey moods, ineffable thoughts, and complex emotions (Williams&#8217; Carriage Return), so some level of encoding is needed. Hash tags work great for marking up objects, topics, and locations but are not computational. A glue language, such as Inform, would be needed to add programmability to the hash tags. You could obviously send short snippets of Python, each tweet acting as a shared module, but this is still too obfuscated for many readers. Inform is a language developed specifically for both writers and programmers. From the Inform manual:

> Interactive fiction is a literary form which involves programming a computer so that it presents a reader with a text which can be explored. Inform aims to make the burden of learning to program such texts as light as possible. It is a tool for writers intrigued by computing, and computer programmers intrigued by writing. Perhaps these are not so very different pursuits, in their rewards and pleasures

[Inform 7][9] source code has a syntax which resembles natural english, so it&#8217;s fairly easy to read and write. However, it compiles into code understood by a virtual machine (either Z-Machine or Glulx) and can then be run as [interactive fiction][10]. The author is responsible for establishing objects, sets, relationships, containers, labels, descriptions, time, objects, and everything else that goes into the story.

By using Inform to structure tweets, its possible to write collaborative fiction easily accessed by future archive computers.

 [1]: http://www.digitalpreservation.gov/
 [2]: http://lockss.stanford.edu/lockss/Home
 [3]: http://www.nytimes.com/2008/04/13/magazine/13anthropology-t.html
 [4]: http://en.wikipedia.org/wiki/Newline
 [5]: http://en.wikipedia.org/wiki/Constrained_writing
 [6]: http://en.wikipedia.org/wiki/Oulipo
 [7]: http://en.wikipedia.org/wiki/Cell_phone_novel
 [8]: http://www.flickr.com/photos/quasimondo/3518306770/
 [9]: http://inform7.com/
 [10]: http://en.wikipedia.org/wiki/Interactive_fiction