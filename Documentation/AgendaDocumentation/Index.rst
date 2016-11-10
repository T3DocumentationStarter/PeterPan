.. include:: ../Includes.txt


==============================
Documentation Agenda
==============================

.. contents:: What needs to be done?!
   :depth: 2
   :local:
   :backlinks: top


Tasks to be done regularly
==========================

Handle open issues
------------------

Check whether there are open issues for the official manuals and solve them, like

- https://github.com/TYPO3-Documentation/TYPO3CMS-Reference-TCA/issues
- https://github.com/TYPO3-Documentation/TYPO3CMS-Reference-CoreApi/issues
- https://github.com/TYPO3-Documentation/TYPO3CMS-Reference-FileAbstractionLayer/issues
- ...


Process Pull Requests
---------------------

Are there open pull requests?
Observe https://docs.typo3.org/services/GithubPullRequests/
Become a watcher of the repositories of the official manuals at https://github.com/TYPO3-Documentation




Making Documentation available
==============================

Unsorted tasks
--------------

-  Continue with the "Render Documentation Guide" https://docs.typo3.org/typo3cms/RenderTYPO3DocumentationGuide/
-  Continue with "rst-ing with PhpStorm" https://docs.typo3.org/typo3cms/drafts/github/wmdbsystems/RSTingWithPhpStormGuide/
-  Continue with https://docs.typo3.org/typo3cms/drafts/github/wmdbsystems/TYPO3ComposerGuide/
-  Q: How do I set up PhpStorm for reST? A: See the `answer (with screenshots) at 
   <https://github.com/T3DocumentationStarter/Public-Info-015/issues/1>`__


How to do documentation with Github
-----------------------------------

These Q & A are especially important in the context of working with the
`T3DocumentationStarter projects <https://docs.typo3.org/typo3cms/drafts/github/T3DocumentationStarter/Public-Info-001/TeachingDocs/StarterManuals/Index.html>`__.

#. `How do I create a folder? <https://github.com/T3DocumentationStarter/Public-Info-001/issues/2>`__
#. `How can I rename a folder? <https://github.com/T3DocumentationStarter/Public-Info-001/issues/3>`__
#. `SSH doesn't work with my T3DocumentationStarter project
   <https://github.com/T3DocumentationStarter/Public-Info-015/issues/1>`__
#. `How often will and when are manuals being updated on our docs.typo3.org server?
   <https://github.com/T3DocumentationStarter/Public-Info-001/issues/4>`__

Tools // Server // Installation
===============================

-  Make sure the Javascript list of available extension manuals is correct

   * https://docs.typo3.org/typo3cms/extensions/
   * https://docs.typo3.org/typo3cms/extensions/extensions.js

-  Elastic Search


Cronjobs
--------

-  Add a cronjob that removes the :file:`/tmp/TCT/RenderDocumentation/lockfile.json` if the
   `RenderDocumentation` job had failed to do so. Otherwise it would take **x** seconds for the
   lockfile to become outdated. Currently **x** is set to 3.600 seconds. That means, that in
   case the buildjob dies with an unhandled exception it will take an hour until **any**
   manual will be rendered again.

Missing features
----------------

#. :file:`Ajaxdownloads.php`: this `$knownpath` isn't correctly handled:
   :file:`/typo3cms/drafts/github/*/`. Wildcards aren't handled yet.
   


