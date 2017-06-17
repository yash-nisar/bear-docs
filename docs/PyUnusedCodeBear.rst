`PyUnusedCodeBear <https://github.com/coala/coala-bears/tree/master/bears/python/PyUnusedCodeBear.py>`_
=======================================================================================================

Detects unused code. By default this functionality is limited to:
- Unneeded pass statements. - Unneeded builtin imports.

`Supported Languages <../README.rst>`_
--------------------------------------

* Python
* Python 2
* Python 3

Settings
--------

+--------------------------------+-----------------------------------------------------------+
| Setting                        |  Meaning                                                  |
+================================+===========================================================+
|                                |                                                           |
| ``remove_all_unused_imports``  | True removes all unused imports - might have side effects |
|                                | (Optional, defaults to 'False'.)                          |
|                                |                                                           |
+--------------------------------+-----------------------------------------------------------+
|                                |                                                           |
| ``remove_unused_variables``    | True removes unused variables - might have side effects   |
|                                | (Optional, defaults to 'True'.)                           |
|                                |                                                           |
+--------------------------------+-----------------------------------------------------------+


Dependencies
------------

* ``pip`` - ``autoflake``


Can Detect
----------

* Unused Code

License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
