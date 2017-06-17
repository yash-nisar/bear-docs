`YAMLLintBear <https://github.com/coala/coala-bears/tree/master/bears/yaml/YAMLLintBear.py>`_
=============================================================================================

Check yaml code for errors and possible problems.

You can read more about capabilities at
<http://yamllint.readthedocs.org/en/latest/rules.html>.

`Supported Languages <../README.rst>`_
--------------------------------------

* YAML

Settings
--------

+----------------------+-------------------------------------------------------------+
| Setting              |  Meaning                                                    |
+======================+=============================================================+
|                      |                                                             |
| ``document_start``   | Use this rule to require or forbid the use of document      |
|                      | start marker (---). (Optional, defaults to 'None'.)         |
|                      |                                                             |
+----------------------+-------------------------------------------------------------+
|                      |                                                             |
| ``max_line_length``  | Maximum number of characters for a line, the newline        |
|                      | character being excluded. (Optional, defaults to '80'.)     |
|                      |                                                             |
+----------------------+-------------------------------------------------------------+
|                      |                                                             |
| ``yamllint_config``  | Path to a custom configuration file. (Optional, defaults to |
|                      | ''.)                                                        |
|                      |                                                             |
+----------------------+-------------------------------------------------------------+


Dependencies
------------

* ``pip`` - ``yamllint``


Can Detect
----------

* Formatting
* Syntax

License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
