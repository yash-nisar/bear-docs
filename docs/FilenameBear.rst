`FilenameBear <https://github.com/coala/coala-bears/tree/master/bears/general/FilenameBear.py>`_
================================================================================================

Checks whether the filename follows a certain naming-convention.

`Supported Languages <../README.rst>`_
--------------------------------------

* All

Settings
--------

+---------------------------------+------------------------------------------------------------+
| Setting                         |  Meaning                                                   |
+=================================+============================================================+
|                                 |                                                            |
| ``file_naming_convention``      | The naming-convention. Supported values are: - ``auto`` to |
|                                 | guess the correct convention. Defaults to ``snake`` if the |
|                                 | correct convention cannot be guessed. - ``camel``          |
|                                 | (``thisIsCamelCase``) - ``kebab`` (``this-is-kebab-case``) |
|                                 | - ``pascal`` (``ThisIsPascalCase``) - ``snake``            |
|                                 | (``this_is_snake_case``) - ``space`` (``This Is Space      |
|                                 | Case``) (Optional, defaults to 'None'.)                    |
|                                 |                                                            |
+---------------------------------+------------------------------------------------------------+
|                                 |                                                            |
| ``ignore_uppercase_filenames``  | Whether or not to ignore fully uppercase filenames         |
|                                 | completely, e.g. COPYING, LICENSE etc. (Optional, defaults |
|                                 | to 'True'.)                                                |
|                                 |                                                            |
+---------------------------------+------------------------------------------------------------+


License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
