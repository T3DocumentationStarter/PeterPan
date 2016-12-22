
.. include:: ../Includes.txt

============
ReST Tryouts
============

Wanted: Inline code starting with blanks
========================================

See also: Unicode search for "space": http://unicode-suche.de/unicode-namesearch.pl?term=space

Using U+0020 SPACE
------------------

- ``:literal:`\ abc``` → :literal:`\ abc`
- ```\ abc``` → `\ abc`
- \`\` abc\`\` → ``\ abc``

**Failure!**

Using U+00A0 NO-BREAK SPACE
---------------------------

- ``:literal:``` abc` → :literal:` abc`
- ``` abc``` → ` abc`
- \`\` abc\`\` → `` abc``

**Failure!**

Using U+2420 SYMBOL FOR SPACE
-----------------------------

- ``:literal:`␠abc``` → :literal:`␠abc`
- ```␠abc``` → `␠abc`
- \`\`␠abc\`\` → ``␠abc``

**Success!**

