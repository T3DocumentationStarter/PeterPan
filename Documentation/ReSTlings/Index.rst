
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

Textroles
=========

kbd: :kbd:`Control-x Control-f`

Admonitions
===========

.. admonition:: This one is generic!

   And here we go!

.. note:: There may be a better way.
   We only have to find it.

.. tip:: How to make money now!

   What you should do: ...


Backslash
=========

| use Vendor\\Extkey\\Domain\\Model\\Abc;
| `use Vendor\Extkey\Domain\Model\Abc;`
| :php:`use Vendor\Extkey\Domain\Model\Abc;`
| ``use Vendor\Extkey\Domain\Model\Abc;``

Single backslash in a code-block::

   use Vendor\Extkey\Domain\Model\Abc;
   

Quick try
=========

properties.dateFormat
---------------------

:aspect:`Option path`
     TYPO3.CMS.Form.prototypes.<prototypeIdentifier>.formElementsDefinition.DatePicker.properties.dateFormat

:aspect:`Data type`
     string

:aspect:`Needed by`
     Frontend/ Backend (form editor)

:aspect:`Overwritable within form definition`
     Yes

:aspect:`form editor can write this property into the form definition (for prototype 'standard')`
     Yes

:aspect:`Mandatory`
     Yes

:aspect:`Default value (for prototype 'standard')`
     .. code-block:: yaml
        :linenos:
        :emphasize-lines: 3

        DatePicker:
          properties:
            containerClassAttribute: input
            elementClassAttribute: 'small form-control'
            elementErrorClassAttribute: error
            timeSelectorClassAttribute: mini
            timeSelectorHourLabel: ''
            timeSelectorMinuteLabel: ''
            dateFormat: Y-m-d
            enableDatePicker: true
            displayTimeSelector: false

.. :aspect:`Good to know`
     ToDo

:aspect:`Description`
     The datepicker time format. The following date formats are allowed:
     
     .. highlight:: none

     Day::

        d => Day of the month, 2 digits with leading zeros
        D => A textual representation of a day, three letters
        j => Day of the month without leading zeros
        l => A full textual representation of the day of the week
        
        
     How to write tables: http://docutils.sourceforge.net/docs/user/rst/quickref.html#tables   

     =  ====================================================
     Day
     -------------------------------------------------------
     F  Description
     =  ====================================================
     d  Day of the month, 2 digits with leading zeros
     D  A textual representation of a day, three letters
     j  Day of the month without leading zeros
     l  A full textual representation of the day of the week
     =  ====================================================

     Month::

        F => A full textual representation of a month, such as January or March
        m => Numeric representation of a month, with leading zeros
        M => A short textual representation of a month, three letters
        n => Numeric representation of a month, without leading zeros

     Year::

        Y => A full numeric representation of a year, 4 digits
        y => A two digit representation of a year
        
     .. highlight:: php   

