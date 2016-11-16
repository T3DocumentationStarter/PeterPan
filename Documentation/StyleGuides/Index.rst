
.. include:: ../Includes.txt

=============================================================
Style Guides
=============================================================


Documentation Guides
====================

.. http://docutils.sourceforge.net/docs/ref/rst/directives.html#image

-  |RTDlogo| `Documentation guide <http://www.writethedocs.org/guide/>`__ of WriteTheDocs

.. |RTDlogo| image:: http://www.writethedocs.org/_static/sticker-wtd-colors.png
   :width: 50px
   :target: http://www.writethedocs.org/



Links
=====

-  `The Writer's Handbook: Documentation Styles (writing.wisc.edu)
   <http://writing.wisc.edu/Handbook/Documentation.html>`__
   
-  `Apple Style Guide 2013 (PDF) <https://help.apple.com/asg/mac/2013/ASG_2013.pdf>`__


Related
=======

-  `EPPO - Every page is page one <http://everypageispageone.com/>`__
   Let the reader start reading anywhere.




English: Capitalization in Titles
=================================

2016-11-02

My question at Slack in channel WriteTheDocs/General:

   "Let's say I (from de) want to write documentation for en_US. 
   What are the rules about what words should be capitalized in headlines? 
   Can you point me to some relevant information?"

From the answers:

-  here’s a short summary of the two common choices: 
   http://www.onlinegrammar.com.au/title-and-sentence-case/
   
-  an exhaustive description: 
   http://blog.apastyle.org/apastyle/2012/03/title-case-and-sentence-case-capitalization-in-apa-style.html
   
-  "Based on a tiny bit of prior experience working with writers for whom English
   was not their primary language: if you don't have to match some existing style,
   I'd say the sentence case—capitalizing the first word and any proper nouns
   is a bit easier to explain to others and to maintain."
   
-  "If you're asking about software documentation, there's been a pretty strong 
   trend for a number of years away from title case for any sort of heading or title. 
   Again, my default favorite for writing for the web:"
   https://pages.18f.gov/content-guide/capitalization/
   
-  .. tip::
   
      http://titlecapitalization.com/: Title Capitalization: Your Online Title Case Tool
      
-  "One frustrating trend that I’ve noticed is that enterprise website styles and support
   style guides use title case, and the tech docs rarely use it.
   This creates confusion when people are contributing to both."
   "True, marketing teams still love title case."
   
-  '''There are rules, but even native speakers get them wrong. 
   For example, "the" shouldn't be capitalized but I've seen 
   "How The Product Works" more than a few times. So even if you make a mistake, 
   you'll have plenty of company :) '''


Technical Terms
===============

=================================================== ====================
english                                             deutsch
=================================================== ====================
covering letter                                     Anschreiben
=================================================== ====================


Variable naming
===============

Ranges
------


martin.bless	[5:36 PM]  
Argh, I'm just doing some (Python) programming. If I only could find those non-ambiguous self-documenting variable names. I'm looking for a good naming scheme for ranges, limits, steps, points. And you don't want variable names be toooo long. 
*Example:* An integer variable v is allowed to have values from range 1 to 100. So 1 = minimum value = vmin = lower limit? And 100 = maximum value = vmax = upper limit? What would be the names for 0 and 101 then, the lower limit and upper limit OUTSIDE the legal range? border?

I would love to have a consistent naming scheme. What do you use?

ddbeck	[5:55 PM]  

With the caveat that self-documentation is a myth and there's no substitute for a good docstring, I think the convention is Python is to go for slightly wordier names. So, for instance, I'd expand this variable `v` to be whatever `v` actually represents and go from there. For example if `v` is `velocity` I'd probably go with `max_velocity` and `min_velocity`

As for the question of inclusive or non-inclusive ranges, I don't think naming is going to help you there. That's exactly the sort of thing I'd check the docs for

- range(start, stop, step)
- min\_something, max\_something
- from, to, upto
- first_day, last_day
- border? wall?

