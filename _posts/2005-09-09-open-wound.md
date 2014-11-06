---
title: Open Wound
author: matt_butler
layout: post
permalink: /open-wound/
categories:
  - digital
  - language
  - projects
---
[View the project page][1]

I. When a TAG button is pressed

1. Accept any amount of text from a field called INPUT. Perform a part-of-speech tagging and display the tagged words in a text field called TAGGED OUTPUT. The value of the TAGGED OUTPUT field might look/NN something/NN like/IN this/DET ./PP 

2. Copy each word (without its POS tag) into an appropriate field based on it&#8217;s part-of-speech. The user may delete words or add their own words. Make all words lowercase.

II. When a GENERATE button is pressed

1. Accept a value the user has inputed in the COMMON field. The value can be from 0-100. The number corresponds to an array that contains the 1000 most common words in the English language. (For example, a value of 20 in the COMMON text field means the 20 most common words will not be substituted in the next step.)

2. Substitute each of the words or punctuation marks in the TAGGED OUTPUT field with a different word or punctuation mark from the corresponding POS field unless that word is in the range specified by the COMMON value in which case it is not substituted. Display the result in a SUBSTITUTION text field. 

3. Capitalize any letter directly following the PP, Punctuation, Sentence Ender tag then remove the POS tags from the SUBSTITUTION text. Display the new text in a field called RECOMBINED.

 [1]: http://mbutler.org/openwound/