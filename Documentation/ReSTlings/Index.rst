
.. include:: ../Includes.txt

============
ReST Tryouts
============

Inline code with blanks at the beginning
========================================

Search Unicode for "space": http://unicode-suche.de/unicode-namesearch.pl?term=space

Using U+0020 SPACE
------------------

- ``:literal:`\ abc``` → :literal:`\ abc`
- ```\ abc``` → `\ abc`
- \`\` abc\`\` → ``\ abc``

Using U+00A0 NO-BREAK SPACE
---------------------------

- ``:literal:``` abc` → :literal:` abc`
- ``` abc``` → ` abc`
- '' abc'' → `` abc``

Using U+2420 SYMBOL FOR SPACE
-----------------------------

- ``:literal:`␠abc``` → :literal:`␠abc`
- ```␠abc``` → `␠abc`
- \`\`␠abc\`\` → ``␠abc``


