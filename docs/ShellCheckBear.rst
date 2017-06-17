`ShellCheckBear <https://github.com/coala/coala-bears/tree/master/bears/shell/ShellCheckBear.py>`_
==================================================================================================

Check bash/shell scripts for syntactical problems (with understandable
messages), semantical problems as well as subtle caveats and pitfalls.

A gallery of bad code that can be detected is available at
<https://github.com/koalaman/shellcheck/blob/master/README.md>.

`Supported Languages <../README.rst>`_
--------------------------------------

* bash
* dash
* ksh
* sh

Settings
--------

+------------------------+----------------------------------------------------------+
| Setting                |  Meaning                                                 |
+========================+==========================================================+
|                        |                                                          |
| ``shell``              | Target shell being used. (Optional, defaults to 'sh'.)   +
|                        |                                                          |
+------------------------+----------------------------------------------------------+
|                        |                                                          |
| ``shellcheck_ignore``  | List of linting rules that should be ignored. (Optional, |
|                        | defaults to 'None'.)                                     |
|                        |                                                          |
+------------------------+----------------------------------------------------------+


Dependencies
------------

* ``any-one-of`` - ``CabalRequirement(shellcheck 0.4.1) DistributionRequirement(shellcheck)``


Can Detect
----------

* Security
* Syntax
* Undefined Element
* Unused Code

License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
