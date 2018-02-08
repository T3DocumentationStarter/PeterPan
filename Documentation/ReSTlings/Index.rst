
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

Versuch eins
------------

`<formDefinitionIdentifier>`.element.\ `<elementIdentifier>`.properties.\ `<propertyName>`

Versuch zwei (parsed literal)
-----------------------------

.. parsed-literal::

   **formDefinitionIdentifier**.element.\ **elementIdentifier**.properties.\ **propertyName**
   
Versuch drei
------------

`FORM-DEFINITION-IDENTIFIER.element.ELEMENT-IDENTIFIER.properties.PROPERTY-NAME`


Try out table
=============

Abbreviations
   | TER = TYPO3 extension repository
   | *extkey* = extension key
   | *modkey* = backend module key
   

Public extensions
   1. Public extensions are available from the TER.
   
   2. The *extkey* is made up of alphanumeric characters and underscores only
      and should start with a letter.
   
      **Example:** cool\_shop

   3. The *extkey* is valid if the TER accepts it. This makes sure that the
      name follows the rules and is unique.
      
   4. Database tablenames look like 'tx\_' + *extkey* (without underscores) + '\_specification'.
   
      **Examples:** tx\_coolshop\_products, tx\_coolshop\_categories, tx\_coolshop\_more\_categories 

Private extensions
   1. Private extensions are not uploaded to the TER.
   
   2. The *extkey* is made up of alphanumeric characters and underscores only
      and starts with the string 'user\_'.
   
      **Example:** user\_my\_shop

   3. Database tablenames look like *extkey* + '\_specification'.
   
      **Examples:** user\_my\_shop\_products, user\_my\_shop\_categories

Public backend modules
   1. The *modkey* is made up of alphanumeric characters only. It does not
      contain underscores and starts with a letter.
   
      **Example:** coolshop

   2. ((correct?))   
      Database tablenames look like 'tx' (no underscore) + *modkey* + '\_specification'.
   
      **Examples:** txcoolshop\_products, txcoolshop\_categories, txcoolshop\_more\_categories

Private backend modules
   1. The *modkey* is made up of alphanumeric characters only. It does not
      contain underscores and starts with a letter.
  
      **Example:** uMyCoolShop

   2. ((correct?))
      Database tablenames look like 'u' (no underscore) + *modkey* (no underscores) + '\_specification'.
   
      **Examples:** uMyCoolShop\_products, uMyCoolShop\_categories, uMyCoolShop\_more\_categories
