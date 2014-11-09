---
title: 'An XML translation of Dan Graham&#8217;s &#8220;Schema&#8221;'
author: matt_butler
layout: post
permalink: /an-xml-translation-of-dan-grahams-schema/
categories:
  - digital
  - language
  - projects
---
View the complete project [here][1]  
Read Graham&#8217;s [original text][2]  
Featured in the [Rhizome.org Artbase][3]!  
Some discussion:  
[MTAA-RR][4]  
[networked_performance][5]  
[>> mind the __ GAP][6]

< ?xml version="1.0" encoding="UTF-8"?>  
< !ELEMENT SET (PAGE+)>  
< !ELEMENT PAGE (TEXT)>  
< !ATTLIST PAGE  
PERIMETER CDATA #REQUIRED  
PAPER_STOCK CDATA #IMPLIED  
PAPER_WEIGHT CDATA #IMPLIED>

< !ELEMENT TEXT (COLUMN+)>  
< !ATTLIST TEXT  
PERCENT\_OF\_PAGE CDATA #REQUIRED  
FONT CDATA #REQUIRED  
DEPRESSIONS\_ON\_SURFACE CDATA #IMPLIED  
FONT_SIZE CDATA #REQUIRED>

< !ELEMENT COLUMN (LINE+)>  
< !ELEMENT LINE (WORD+)>  
< !ELEMENT WORD (DATA)>  
< !ELEMENT DATA (#PCDATA) >  
< !ATTLIST WORD  
CAPITALIZED (YES | NO) "NO"  
ITALICIZED (YES | NO) "NO"  
NUMBER\_OF\_LETTERS CDATA #REQUIRED  
PART\_OF\_SPEECH (ADJECTIVE | ADVERB | CONJUNCTION | GERUND | INFINITIVE | NOUN | MATH_SYMBOL | NUMERAL | PREPOSITION | PRONOUN | PARTICIPLE | NA) "NA">

 [1]: http://www.mbutler.org/schema/
 [2]: http://www.ubu.com/concept/graham_schema.html
 [3]: http://rhizome.org/object.rhiz?34361
 [4]: http://www.mteww.com/mtaaRR/news/twhid/xml_translation_of_dan_graham_s_schema.html
 [5]: http://www.turbulence.org/blog/archives/001293.html
 [6]: http://www.mindgap.org/index.php/archives/2005/08/25/377/