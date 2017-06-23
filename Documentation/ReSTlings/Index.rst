
.. include:: ../Includes.txt

============
ReST Tryouts
============

Wanted: Inline code starting with blanks
========================================

See also: `Unicode search for "space" <http://unicode-suche.de/unicode-namesearch.pl?term=space>`__

Using U+0020 SPACE
------------------

Does not work:

- ``:literal:`\ abc``` → :literal:`\ abc` parsing works, but no blank in output
- ```\ abc``` → `\ abc`
- \`\` abc\`\` → ``\ abc``

Using U+00A0 NO-BREAK SPACE
---------------------------

Does not work:

- ``:literal:``` abc` → :literal:` abc`
- ``` abc``` → ` abc`
- \`\` abc\`\` → `` abc``


Using U+2420 SYMBOL FOR SPACE
-----------------------------

Works:

- ``:literal:`␠abc``` → :literal:`␠abc`
- ```␠abc``` → `␠abc`
- \`\`␠abc\`\` → ``␠abc``



Experiment
==========

`<formDefinitionIdentifier>`.element.`<elementIdentifier>`.properties.`<propertyName>`

.. parsed-literal::

   *formDefinitionIdentifier*.element.*elementIdentifier*.properties.*propertyName*
   
