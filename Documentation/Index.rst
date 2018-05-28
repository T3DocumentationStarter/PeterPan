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

==========================
My Public Info Project 001
==========================

:Writing here:    `Martin Bless <martin.bless@mbless.de>`__
:Rendered:        |today|
:Buildinfo:       `buildinfo <_buildinfo>`_ \|
                  `Rebuild! <https://docs.typo3.org/~mbless/github.com/T3DocumentationStarter/Public-Info-001.git.make/request_rebuild.php>`__

:Others:          `Who else has a starter project? <TeachingDocs/StarterManuals/Index.html#who-is-where>`__

See:

-  `999: T3O-Team   <https://docs.typo3.org/typo3cms/Teams/T3oTeam/>`__
-  `054: T3DocTeam  <https://docs.typo3.org/typo3cms/Teams/T3DocTeam/>`__

.. toctree::
   :hidden:

   Sitemap/Index
   Docker/Index
   DocTools/Index
   Hyperlinks/Index
   IncomingNotes/Index
   ManualsInProgress/Index
   MarkupLanguages/Index
   ReSTlings/Index
   reStructuredText/Index
   StyleGuides/Index
   T3DocsGitlab/Index
   T3DocsREST/Index
   TeachingDocs/Index
