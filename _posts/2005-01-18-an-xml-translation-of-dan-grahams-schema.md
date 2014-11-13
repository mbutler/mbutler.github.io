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
Featured in the [Rhizome.org Artbase][3] 

In 1966 conceptual artist Dan Graham composed a language based work entitled Schema. The artwork consisted of a formal procedure for how to describe a document, or a "set of pages," with no real reference to the content of that document. This schema, as he called it, shares a remarkable similarity with XML, invented over 30 years later.

The conceptual artists of the late 1960's and early 1970's were interested in the nonvisual abstraction of art and how artworks might be represented as information. Using language in a non-literary and non-poetic manner, they sought to continue the tradition of visual artists in a search for abstraction and minimalism. Many conceptual works of this time were simply words on paper, instructions, or thought experiments. Schema allowed the viewer to be aware of the material nature and structure of the document they were holding -- as well as any document they might hold. Using XML, I have created a machine-readable translation of his important 1966 work.

##SET_OF_PAGES.dtd 

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
 [3]: http://rhizome.org/artbase/artwork/34361/
