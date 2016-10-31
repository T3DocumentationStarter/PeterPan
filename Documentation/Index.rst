.. Tip - just do it:
      don't use TABs (= \t, tabulators)
      replace each TAB by *three blanks* (enable RegExp for Search and Replace in your IDE)
      set TAB width and indentation to THREE in your IDE
      set 'Use blanks instead of TABs' in your IDE


.. With the following include we import some definition. We do this in each and every file.
   so we can change the definition at a single place. Use the relative path to the Includes.txt file,
   which may look as well like ../../../Includes.txt for a deeply nested source file.

.. include:: Includes.txt


.. Usually we define 'php' as default highlight language in Includes.txt.
   With the following 'highlight' directive we switch to reStructuredText as default highlight language.

.. highlight:: rst


.. The following, first section (= headline) is the 'Document Title'.


======================
My Public Info Project
======================


.. The following is 'field list' which is rendered as a horizontal table.
   Think of it as key-value pairs.


:Writing here:    `Martin Bless <martin.bless@mbless.de>`__
:Rendered:        |today|


.. note::

   This is a **one file** documentation. You see: A single text file
   can already convey *a lot* of information!


Docutils and Sphinx
===================

Docutils_ basically deals with single files that contain reStructuredText_.

Sphinx_ builds on Docutils_ and allows to join many single files together to
form a *Documentation Project* like a book. And of course, since Sphinx is all
about creating documentation *projects*, it comes with a beautiful and detailed
documentation itself.

.. tip::

   You have questions about reStructuredText?
   The first thing you should think of is:
   `Visit the Sphinx-Doc website! <http://www.sphinx-doc.org/>`__

.. _Sphinx: http://www.sphinx-doc.org/


Learn about the basics of "reStructuredText"
============================================

Yes, there is original documentation about and around reStructuredText.
But, oh dear, it looks it has never been styled and it may blow your mind at some points
since the details are difficult to understand.
But, there are good news as well:
You can easily start nevertheless. Just use easy markup in the beginning.


A reading that organizes information
------------------------------------

-  `reStructuredText <http://docutils.sourceforge.net/rst.html>`_

   *Note:*
   This document is about "Markup Syntax and Parser Component of `Docutils
   <http://docutils.sourceforge.net/index.html>`_"

   *Note:* "reStructuredText" is ONE word, not two!


User Documentation
------------------

-  `A ReStructuredText Primer <http://docutils.sourceforge.net/docs/user/rst/quickstart.html>`_

   *Note:*
   This document is an informal introduction to reStructuredText.
   The `What Next? <http://docutils.sourceforge.net/docs/user/rst/quickstart.html#what-next>`_
   section in there has links to further resources, including a formal reference.

-  `Quick reStructuredText <http://docutils.sourceforge.net/docs/user/rst/quickref.html>`_

   *Note:*
   This document is just intended as a reminder.
   The full details of the markup may be found on the reStructuredText page.


-  `The reStructuredText Cheat Sheet: Syntax Reminders
   <http://docutils.sourceforge.net/docs/user/rst/cheatsheet.txt>`_

   text only; 1 page for syntax, 1 page directive & role reference


Reference Documentation
-----------------------

-  `An Introduction to reStructuredText <http://docutils.sourceforge.net/docs/ref/rst/introduction.html>`_

    including the Goals and History of reStructuredText


-  `reStructuredText Markup Specification <http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html>`_

   *Note:*
   This document is a detailed technical specification; it is not a tutorial or a primer.
   If this is your first exposure to reStructuredText, please read
   A ReStructuredText Primer and the Quick reStructuredText user reference first.


-  `reStructuredText Directives <http://docutils.sourceforge.net/docs/ref/rst/directives.html>`_

   *Note:* This document describes the directives implemented in the reference reStructuredText parser.


-  `reStructuredText Interpreted Text Roles <http://docutils.sourceforge.net/docs/ref/rst/roles.html>`_

   *Note:* This document describes the interpreted text roles implemented in the reference reStructuredText parser.


Developer Documentation
-----------------------

-  `A Record of reStructuredText Syntax Alternatives <http://docutils.sourceforge.net/docs/dev/rst/alternatives.html>`_
-  `Problems With StructuredText <http://docutils.sourceforge.net/docs/dev/rst/problems.html>`_

How-To's
--------

-  `Creating reStructuredText Directives <http://docutils.sourceforge.net/docs/howto/rst-directives.html>`_
-  `Creating reStructuredText Interpreted Text Roles <http://docutils.sourceforge.net/docs/howto/rst-roles.html>`_






Hyperlinks
==========

The complete, anonymous form
----------------------------

This markup will always work. It has a `linktext`, the complete url in `<...>`,
and **two** underscores at the end. **Two** mean that it's an anonymous link. This
means that the `linktext` is NOT added to the internal table of known link definitions::

   `linktext <https://the/complete/url/>`__

Example::

   See `buildinfo <https://docs.typo3.org/typo3cms/drafts/github/T3DocumentationStarter/Public-Info-001/_buildinfo/>`__

Result:

See `buildinfo <https://docs.typo3.org/typo3cms/drafts/github/T3DocumentationStarter/Public-Info-001/_buildinfo/>`__




A named link
------------

Define the linktext `buildinfo` and the url somewhere in the document::

   .. _buildinfo: https://docs.typo3.org/typo3cms/drafts/github/T3DocumentationStarter/Public-Info-001/_buildinfo/

Use the defined link as often as you like::

   See the buildinfo_. See the buildinfo_. See the buildinfo_.

Result:

See the buildinfo_. See the buildinfo_. See the buildinfo_.

.. _buildinfo: https://docs.typo3.org/typo3cms/drafts/github/T3DocumentationStarter/Public-Info-001/_buildinfo/

tip::

   The url may even be relative::

      .. _buildinfo: _buildinfo



Another way to create a named link
----------------------------------

((to be written))




Anonymous hyperlinks
--------------------

These may come in very handy especially when you are copying and pasting very long, unhandy links.
Here we use some nice links for demonstration.
Create a list with anonymous target urls. To do so, start the line with **two** underscores and
a blank and then paste the link. Afterwards in your text you can use - and consume - one
link after the other in exactly the order you listed them. Example::

   __ https://typo3.org/
   __ https://typo3.org/extensions/repository/
   __ https://docs.typo3.org/

   Go here__ first, then look at `the extensions`__ and don't forget to visit
   the documentation__.

Result:

__ https://typo3.org/
__ https://typo3.org/extensions/repository/
__ https://docs.typo3.org/

Go here__ first, then look at `the extensions`__ and don't forget to visit
the documentation__.





Introduction
============

This is some text for introduction.


Main Contents
=============

Here we go.

