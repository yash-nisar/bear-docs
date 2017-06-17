`LanguageToolBear <https://github.com/coala/coala-bears/tree/master/bears/natural_language/LanguageToolBear.py>`_
=================================================================================================================

Checks the code with LanguageTool.

`Supported Languages <../README.rst>`_
--------------------------------------

* Natural Language

Settings
--------

+---------------------------------+-------------------------------------------------------------+
| Setting                         |  Meaning                                                    |
+=================================+=============================================================+
|                                 |                                                             |
| ``languagetool_disable_rules``  | List of rules to disable checks for. (Optional, defaults to |
|                                 | '()'.)                                                      |
|                                 |                                                             |
+---------------------------------+-------------------------------------------------------------+
|                                 |                                                             |
| ``natural_language``            | A locale representing the language you want to have         |
|                                 | checked. If set to 'auto' the language is guessed. If the   |
|                                 | language cannot be guessed, 'en-US' is used. (Optional,     |
|                                 | defaults to 'auto'.)                                        |
|                                 |                                                             |
+---------------------------------+-------------------------------------------------------------+


Dependencies
------------

* ``pip`` - ``guess-language-spirit``
* ``pip`` - ``language-check``


Can Detect
----------

* Grammar
* Spelling

License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
