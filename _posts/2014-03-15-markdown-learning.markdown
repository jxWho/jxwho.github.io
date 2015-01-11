---
layout: post
title: "markdown-learning"
date: 2014-03-15 15:42:51 -0400
published: true
comments: true
disqus: y
categories: Markdown
---

#Markdown

###OUTLINE
* What Is Markdown
* Block Elements
 	+ RETURN
 	+ HEADERS
 	+ BLOCKQUOTE
 	+ LISTS
 	+ CODE BLOCKS
* Span Elements
 	+ LINKS
 	+ EMPASHASIS
 	+ IMAGES
 * Misellaneous
 	+ AUTOMATIC LINKS
 	+ BACKSLASH ESCAPES
 * Mrakdown and HTML
 	
## What is Markdown

Markdown is a tool used to change literal text into HTML in a easier way. 
- - -
<!--more-->
###Block Elements
</br>
<span id="return"></span>
#####Paragraphs and Line breaks
How To *RETURN* (insert a blank line):

		
		type "return" twice

Note:

* "Every line break is a \<br />" rule wouldn't work for Markdown.
* Two "RETURN" ends a paragraph

------
#####HEARDERS

Two styles of headers, Settext and atx.

######Settext-style:

	This is an H1
	=============
	
	This is an H2
	-------------

Any number of underlining = or - will work.

######Atx-styl:

	# This is an H1
	## This is an H2
	....
	###### This is an H6
or 

	# This is an H1 #
	## This is an H2 ##
	...
	###### This is an H6 ######
The "close" atx-style is for decoration. The closing hashes don't even have to 
match the number of hashes used to open the header.
***
#####Blockquote:

Use '>' to qutote:

	> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
	> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
	> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
	> 
	> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
	> id sem consectetuer libero luctus adipiscing.

You can also only put the '>' on the start line of a paragraph:

	> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
	consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
	Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

	> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
	id sem consectetuer libero luctus adipiscing.

Nested blockquotes:

	> This is the first level of quoting.
	>
	> > This is nested blockquote.
	>
	> Back to the first level.

Blockquotes with oter Markdown elements:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");
	
***
#####Lists
###### Unordered Lists
	* h
	* j
	* k
	* l
or

	+ h
	+ j
	+ k

or

	- h
	- j
	- k
	
###### Ordered Lists
	1. left
	2. up
	3. down
	4. right
	
---
#####Code BLocks
* Use at least 4 spaces or 1 tab to start a code block.
* use backtick quotes(`) to indicate a span of code

		Use the `printf()` function.
	If there're (`)s in your code, use muliple backticks as the opning
	and closing delimiters:
	
		``There is a literal backtick (`) here.``

---

#####Horizontal Rules

	* * *
	***
	****
	- - -
	---------------

###Span Elements

#####Links
The link text is delimited by '[Description of the link]'

	This is [an example](http://www.google.com/)
	[Google](http://www.google.com/)
	
or use the 

	This is [an example][id] ref
Then, you need to define this anywhere in the document:

	[id]: http://www.google.com/
- - -
#####Empahasis

	*single asterisks*

	_single underscores_

	**double asterisks**

	__double underscores__
	
Correponding results:

	<em>single asterisks</em>

	<em>single underscores</em>

	<strong>double asterisks</strong>

	<strong>double underscores</strong>
- - -
#####Iamges
	![Alt text](/path/to/img.jpg)
	![Alt text](/path/to/img.jpg "Optional title")
	
Or Reference-style image syntax:

	![Alt text][id]

Also, in somewhere

	[id]: url/to/image "Optional title attribute"

- - -



####Misellaneous
#####Automatic Links
	<http://example.com/>
	
Will be turned into:
	
	<a href="http://example.com/">http://example.com/</a>

Likely,

	<address@example.com>
Will be turned into
	
	<ahref="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>
	
- - -

####Backslash Escapes
Markdown allows you to use backslash escapes to generate literal characters for those special characters:

	\*literal asterisks\*
	
Blackslash escape characters:

	\   backslash
	`   backtick
	*   asterisk
	_   underscore
	{}  curly braces
	[]  square brackets
	()  parentheses
	#   hash mark
	+   plus sign
	-   minus sign (hyphen)
	.   dot
	!   exclamation mark
- - -

###MARKDOWN AND HTML



####Atuomatic Escaping For Speical Characters
There are two special characters that demand special treatment in html. They are < and &.

Markdown allows you to use these characters naturally, which means it will escape them for you when necessary.

Like, if you want to include a copy symbol in your atricle, you can write

	&copy;

and Markdown will leave it alone. But if you write:

	AT&T

It will be translated to:

	AT\&amp;T

- - -
##Reference
<http://daringfireball.net/projects/markdown/syntax>

<http://equation85.github.io/blog/markdown-examples/>
