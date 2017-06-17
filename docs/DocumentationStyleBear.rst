`DocumentationStyleBear <https://github.com/coala/coala-bears/tree/master/bears/documentation/DocumentationStyleBear.py>`_
==========================================================================================================================

Checks for certain in-code documentation styles.
It currently checks for the following style: ::
The first line needs to have no indentation. - Following lines can have indentation

`Supported Languages <../README.rst>`_
--------------------------------------

* c
* cpp
* cs
* default
* fortran
* golang
* java
* objective-c
* php
* python
* python3
* tcl
* vhdl

Settings
--------

+------------------------------+-------------------------------------------------------------+
| Setting                      |  Meaning                                                    |
+==============================+=============================================================+
|                              |                                                             |
| ``allow_missing_func_desc``  | When set ``True`` this will allow functions with missing    |
|                              | descriptions, allowing functions to start with params.      |
|                              | (Optional, defaults to 'False'.)                            |
|                              |                                                             |
+------------------------------+-------------------------------------------------------------+
|                              |                                                             |
| ``docstyle``                 | The docstyle to use. For example ``default`` or             |
|                              | ``doxygen``. Docstyles are language dependent, meaning not  |
|                              | every language is supported by a certain docstyle.          |
|                              | (Optional, defaults to 'default'.)                          |
|                              |                                                             |
+------------------------------+-------------------------------------------------------------+
|                              |                                                             |
| ``indent_size``              | Number of spaces per indentation level. (Optional, defaults |
|                              | to '4'.)                                                    |
|                              |                                                             |
+------------------------------+-------------------------------------------------------------+
|                              |                                                             |
| ``language``                 | The programming language of the file(s).                    +
|                              |                                                             |
+------------------------------+-------------------------------------------------------------+


Demo
----

|asciicast|

.. |asciicast| image:: https://asciinema.org/a/7sfk3i9oxs1ixg2ncsu3pym0u.png
   :target: https://asciinema.org/a/7sfk3i9oxs1ixg2ncsu3pym0u?autoplay=1
   :width: 100%

Can Detect
----------

* Documentation

Can Fix
----------

* Documentation

License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
