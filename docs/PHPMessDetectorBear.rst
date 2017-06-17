`PHPMessDetectorBear <https://github.com/coala/coala-bears/tree/master/bears/php/PHPMessDetectorBear.py>`_
==========================================================================================================

The bear takes a given PHP source code base and looks for several
potential problems within that source. These problems can be things like:

- Possible bugs
- Suboptimal code
- Overcomplicated expressions
- Unused parameters, methods, properties

`Supported Languages <../README.rst>`_
--------------------------------------

* PHP

Settings
--------

+---------------------+-------------------------------------------------------------+
| Setting             |  Meaning                                                    |
+=====================+=============================================================+
|                     |                                                             |
| ``phpmd_rulesets``  | A list of rulesets to use for analysis. Available rulesets: |
|                     | cleancode, codesize, controversial, design, naming,         |
|                     | unusedcode.                                                 |
|                     |                                                             |
+---------------------+-------------------------------------------------------------+


Dependencies
------------

* ``any-one-of`` - ``ComposerRequirement(phpmd/phpmd) DistributionRequirement(phpmd)``


Can Detect
----------

* Complexity
* Formatting
* Redundancy
* Unused Code
* Variable Misuse

License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
