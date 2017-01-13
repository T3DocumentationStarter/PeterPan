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


==========================
My Public Info Project 001
==========================


.. The following is 'field list' which is rendered as a horizontal table.
   Think of it as key-value pairs.


:Writing here:    `Martin Bless <martin.bless@mbless.de>`__
:Rendered:        |today|
:Buildinfo:       `buildinfo <_buildinfo>`_
:Others:          `overview <..>`__

`Rebuild! <https://docs.typo3.org/~mbless/github.com/T3DocumentationStarter/Public-Info-001.git.make/request_rebuild.php>`__


**Contents:**

.. rst-class:: compact
.. toctree::

   Sprint-2017-01/Index
   AgendaDocumentation/Index
   T3DocsREST/Index
   T3DocTeam/Index
   TeachingDocs/Index
   StyleGuides/Index
   IncomingNotes/Index
   ManualsInProgress/Index
   ReSTlings/Index
   Hyperlinks/Index
   reStructuredText/Index
