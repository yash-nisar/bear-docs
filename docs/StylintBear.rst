`StylintBear <https://github.com/coala/coala-bears/tree/master/bears/stylus/StylintBear.py>`_
=============================================================================================

Attempts to catch little mistakes (duplication of rules for instance) and
enforces a code style guide on Stylus (a dynamic stylesheet language
with the ``.styl`` extension that is compiled into CSS) files.

The ``StylintBear`` is able to catch following problems:
- Duplication of rules
- Mixed spaces and tabs
- Unnecessary brackets
- Missing colon between property and value
- Naming conventions
- Trailing whitespace
- Consistent quotation style
- Use of extra spaces inside parenthesis
- Naming convention when declaring classes, ids, and variables
- Unnecessary leading zeroes on decimal points
- Checks if a property is valid CSS or HTML

`Supported Languages <../README.rst>`_
--------------------------------------

* Stylus

Settings
--------

+--------------------------------------+-------------------------------------------------------------+
| Setting                              |  Meaning                                                    |
+======================================+=============================================================+
|                                      |                                                             |
| ``allow_trailing_whitespace``        | If ``True``, ignores trailing whitespace. If ``False``,     |
|                                      | trailing whitespace will throw a warning. (Optional,        |
|                                      | defaults to 'False'.)                                       |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``block_keyword``                    | When ``True`` expect the ``@block`` keyword when defining   |
|                                      | block variables. When ``False``, expect no ``@block``       |
|                                      | keyword when defining block variables. (Optional, defaults  |
|                                      | to 'None'.)                                                 |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``brackets``                         | When ``True``, expect ``{}`` when declaring a selector.     |
|                                      | When ``False``, expect no brackets when declaring a         |
|                                      | selector. (Optional, defaults to 'False'.)                  |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``check_duplicates``                 | Checks if selectors or properties are duplicated            |
|                                      | unnecessarily. (Optional, defaults to 'True'.)              |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``check_no_important_keyword``       | If ``True``, show warning when ``!important`` is found. For |
|                                      | example: If set to ``True``, this will throw a warning::    |
|                                      | div color red !important                                    |
|                                      | (Optional, defaults to 'True'.)                             |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``check_property_validity``          | Check that a property is valid CSS or HTML. (Optional,      |
|                                      | defaults to 'True'.)                                        |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``colons_for_property_declaration``  | When ``True``, expect ``:`` when declaring a property. When |
|                                      | ``False``, expect no ``:`` when declaring a property.       |
|                                      | (Optional, defaults to 'True'.)                             |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``color_variables_for_hex_values``   | When ``True``, enforce variables when defining hex values.  |
|                                      | (Optional, defaults to 'True'.)                             |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``efficient_properties``             | Check for places where properties can be written more       |
|                                      | efficiently. (Optional, defaults to 'True'.)                |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``extend_preference``                | Pass in either ``@extend`` or ``@extends`` and then enforce |
|                                      | that. Both are valid in Stylus. It doesn't really matter    |
|                                      | which one you use. For example: If set to ``@extends``,     |
|                                      | prefer ``@extends $some-var`` instead of ``@extend          |
|                                      | $some-var`` or if set to ``@extend``, prefer ``@extend      |
|                                      | $some-var`` over ``@extends $some-var``. (Optional,         |
|                                      | defaults to 'None'.)                                        |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``indent_size``                      | This works in conjunction with ``max_selector_depth``. If   |
|                                      | you indent with spaces this is the number of spaces you     |
|                                      | indent with. If you use hard tabs, set this value to ``0``. |
|                                      | For example: If set to ``2``, prefer ``/s/smargin: 0`` over |
|                                      | ``/s/s/smargin: 0``. (Optional, defaults to '0'.)           |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``leading_zero``                     | When ``True``, prefer leading zeroes on decimal points.     |
|                                      | When ``False``, disallow leading zeroes on decimal points.  |
|                                      | (Optional, defaults to 'None'.)                             |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``max_errors``                       | Set maximum number of errors. If ``0``, all errors will be  |
|                                      | shown without a limit. (Optional, defaults to '0'.)         |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``max_selector_depth``               | Set the max selector depth. If set to 4, max selector depth |
|                                      | will be 4 indents. Pseudo selectors like ``&:first-child``  |
|                                      | or ``&:hover`` won't count towards the limit. (Optional,    |
|                                      | defaults to 'False'.)                                       |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``max_warnings``                     | Set maximum number of warnings. If ``0``, all errors will   |
|                                      | be shown without a limit. (Optional, defaults to '0'.)      |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``mixed_spaces_and_tabs``            | If a non-negative number is passed to ``indent_size``, soft |
|                                      | tabs (i.e. spaces) are assumed, and if ``0`` is passed to   |
|                                      | ``indent_size``, hard tabs are assumed. For example: If     |
|                                      | ``indent_size = 4`` and ``mixed_spaces_and_tabs = True``,   |
|                                      | prefer ``/s/s/s/smargin 0`` over ``/tmargin 0`` or if       |
|                                      | ``indent_size = 0`` and ``mixed_spaces_and_tabs = True``,   |
|                                      | prefer ``/tmargin 0`` over ``/s/s/s/smargin 0``. (Optional, |
|                                      | defaults to 'False'.)                                       |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``no_css_literals``                  | By default Stylint ignores ``@css`` blocks. If set to       |
|                                      | ``True`` however, warnings are thrown if ``@css`` is used.  |
|                                      | (Optional, defaults to 'False'.)                            |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``none_keyword``                     | If ``True`` check for places where ``none`` used instead of |
|                                      | ``0``. If ``False`` check for places where ``0`` could be   |
|                                      | used instead of ``none``. (Optional, defaults to 'False'.)  |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``placeholder``                      | Enforce extending placeholder vars when using               |
|                                      | ``@extend(s)``. (Optional, defaults to 'True'.)             |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``preferred_quotation``              | Your preferred quotation character, e.g. ``double`` or      |
|                                      | ``single``. (Optional, defaults to 'None'.)                 |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``prefix_vars_with_dollar``          | Enforce use of ``$`` when defining a variable. In Stylus,   |
|                                      | using a ``$`` when defining a variable is optional, but is  |
|                                      | a good idea if you want to prevent ambiguity. Not including |
|                                      | the ``$`` sets up situations where you wonder: "Is this a   |
|                                      | variable or a value?" For instance: ``padding $default`` is |
|                                      | easier to understand than ``padding default``. For example: |
|                                      | If set to ``True``, prefer ``$my-var = 0`` over ``my-var =  |
|                                      | 0`` or if set to ``False``, prefer ``my-var = 0`` over      |
|                                      | ``$my-var = 0``. (Optional, defaults to 'True'.)            |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``semicolons``                       | When ``True``, enforce semicolons. When ``False``, disallow |
|                                      | semicolons. (Optional, defaults to 'False'.)                |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``sort_order``                       | Enforce a particular sort order when declaring properties.  |
|                                      | Throws a warning if you don't follow the order. For         |
|                                      | example: If set to ``alphabetical``, prefer this::          |
|                                      | .some-class display block float left position absolute      |
|                                      | right 10px top 0                                            |
|                                      | over this::                                                 |
|                                      | .some-class position absolute top 0 right 10px display      |
|                                      | block float left                                            |
|                                      | Supported values are ``alphabetical`` and ``grouped``.      |
|                                      | (Optional, defaults to 'alphabetical'.)                     |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``spaces_after_commas``              | Enforce or disallow spaces after commas. (Optional,         |
|                                      | defaults to 'True'.)                                        |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``spaces_after_comments``            | Enforce or disallow spaces after line comments. For         |
|                                      | example: If set to ``True``, prefer ``// comment`` over     |
|                                      | ``//comment``. (Optional, defaults to 'True'.)              |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``spaces_inside_parentheses``        | Enforce or disallow use of extra spaces inside parentheses. |
|                                      | For example: If set to ``True``, prefer ``my-mixin(         |
|                                      | $myParam )`` over ``my-mixin($myParam)`` or if set to       |
|                                      | ``False``, prefer ``my-mixin($myParam)`` over ``my-mixin(   |
|                                      | $myParam )``. (Optional, defaults to 'None'.)               |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``stacked_properties``               | No one-liners. Enforce putting properties on new lines. For |
|                                      | example: If set to ``False``, prefer::                      |
|                                      | .className padding 0                                        |
|                                      | over ``.className { padding 0 }`` (Optional, defaults to    |
|                                      | 'False'.)                                                   |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``strict_naming_convention``         | By default, ``variable_naming_convention`` only looks at    |
|                                      | variable names. If ``strict_naming_convention`` is set to   |
|                                      | ``True``, ``variable_naming_convention`` will also look at  |
|                                      | class and ID names. (Optional, defaults to 'False'.)        |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``stylint_config``                   | The location of the ``.stylintrc`` config file. (Optional,  |
|                                      | defaults to ''.)                                            |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``variable_naming_convention``       | Enforce a particular naming convention when declaring       |
|                                      | variables. Throws a warning if you don't follow the         |
|                                      | convention. Supported values are ``lowercase-dash``,        |
|                                      | ``lowercase_underscore``, ``camelCase`` and ``BEM``.        |
|                                      | (Optional, defaults to 'None'.)                             |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``z_index_normalize_base``           | Enforce some basic z-index sanity. Any number passed in     |
|                                      | will be used as the base for your z-index values. Use ``0`` |
|                                      | to disable this feature. For example: If set to ``5``,      |
|                                      | prefer ``z-index 10`` over ``z-index 9`` or if set to       |
|                                      | ``10``, prefer ``z-index 20`` over ``z-index 15``.          |
|                                      | (Optional, defaults to '0'.)                                |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+
|                                      |                                                             |
| ``zero_units``                       | Looks for instances of ``0px``. You don't need the ``px``.  |
|                                      | Checks all units, not just ``px``. (Optional, defaults to   |
|                                      | 'False'.)                                                   |
|                                      |                                                             |
+--------------------------------------+-------------------------------------------------------------+


Dependencies
------------

* ``npm`` - ``stylint``


Can Detect
----------

* Formatting
* Redundancy
* Syntax

License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
