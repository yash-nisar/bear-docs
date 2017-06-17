`ApertiumLintBear <https://github.com/coala/coala-bears/tree/master/bears/apertium/ApertiumLintBear.py>`_
=========================================================================================================

`Apertium lint` is a python module that lints out irregular yet
acceptable constructs that may creep into files involved in the
transfer process. The lint is designed specifically to handle
4 file types dictionaries, transfer, modes and tagger.

https://github.com/coala/coala-bears/issues/1697 needs to be closed
for extending Windows support for this bear.

Lints the file using
`apertium_lint <https://pypi.python.org/pypi/apertium_lint>`.

`Supported Languages <../README.rst>`_
--------------------------------------

* Apertium

Settings
--------

+------------------------------------+-------------------------------------------------------------+
| Setting                            |  Meaning                                                    |
+====================================+=============================================================+
|                                    |                                                             |
| ``apertiumlint_config``            | Path to a custom configuration file. (Optional, defaults to |
|                                    | ''.)                                                        |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``bidix_transfer_direction``       | This issue is responsible for detecting and reporting       |
|                                    | incorrect transfer directions in bidix files. (Optional,    |
|                                    | defaults to 'False'.)                                       |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``blank_space_detection``          | This issue detects 'extra' blank spaces that might be       |
|                                    | present in the entries in monodix files. (Optional,         |
|                                    | defaults to 'False'.)                                       |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``check_valid_equal_tag``          | Another common error in transfer files is trying to compare |
|                                    | an attribute to a value it cannot take. (Optional, defaults |
|                                    | to 'True'.)                                                 |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``check_valid_part_clip``          | Check that the attribute listed in part='xyz' is defined    |
|                                    | using a `<def­attr>`. The valid parts are defined in        |
|                                    | def­attrs section of the transfer file. (Optional, defaults |
|                                    | to 'True'.)                                                 |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``check_valid_position``           | Every mention of pos='xyz' is checked to make sure that xyz |
|                                    | is less than or equal to the number of elements in pattern  |
|                                    | ­item. (Optional, defaults to 'False'.)                     |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``compare_sdefs``                  | This issue is responsible for detecting and reporting the   |
|                                    | sdefs that may be present in the bidix but are absent in    |
|                                    | the monodixes. (Optional, defaults to 'False'.)             |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``conflicting_cat_item``           | This detects and reports if the same cat­item has been used |
|                                    | in two or more def­cats. (Optional, defaults to 'False'.)   |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``def_label_closed``               | No description given. (Optional, defaults to 'False'.)      +
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``empty_program``                  | Not so much a risk, but this function prompts if a given    |
|                                    | program does not have any file associated with it.          |
|                                    | (Optional, defaults to 'False'.)                            |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``enforce_break_tag``              | This function reports the if the `<b/>` tags are absent     |
|                                    | between two consecutive `<lu>` tags. (Optional, defaults to |
|                                    | 'False'.)                                                   |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``enforce_rules``                  | This function is responsible for enforcing certain rules    |
|                                    | specific to given programs. (Optional, defaults to 'True'.) |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``enforce_side``                   | In `<out>` the side attribute can either take the value of  |
|                                    | 'sl' or 'tl'. With the lint in place, the user can enforce  |
|                                    | the side attribute to be 'tl' in all the `<out>` tags.      |
|                                    | (Optional, defaults to 'False'.)                            |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``install_bool``                   | In modes files, the install attribute can only take one of  |
|                                    | two binary values, ‘yes’ or ‘no’. This function is          |
|                                    | responsible for making sure that no other value is used for |
|                                    | the same. (Optional, defaults to 'False'.)                  |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``install_switch_no``              | If in the definition of a certain mode, the attribute       |
|                                    | install=”no”, the name should have an appropriate suffix    |
|                                    | like ­morph, interchunk, etc. (Optional, defaults to        |
|                                    | 'True'.)                                                    |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``locate_file``                    | This function checks and prompts incase a file defined in a |
|                                    | “program” is missing in the PWD. (Optional, defaults to     |
|                                    | 'False'.)                                                   |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``macro_names``                    | This issue detects multiple def-macro names in transfer     |
|                                    | files. (Optional, defaults to 'False'.)                     |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``monodix_transfer_direction``     | This is issue is responsible for making sure that a valid   |
|                                    | transfer direction is supplied in monodix files. (Optional, |
|                                    | defaults to 'False'.)                                       |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``paradigm_names``                 | This issue is responsible for enforcing certain rules       |
|                                    | associated with naming paradigms in monodix files.          |
|                                    | (Optional, defaults to 'True'.)                             |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``partially_in_lemma``             | This issue is responsible for detecting if the parameter    |
|                                    | definitions that are part of lemma are written twice in     |
|                                    | monodix files. (Optional, defaults to 'False'.)             |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``r_tag_data``                     | This issue is responsible for detecting any inconsistency   |
|                                    | in the data present in the `<r>` tag in the parameter       |
|                                    | definition entries in monodix files. (Optional, defaults to |
|                                    | 'False'.)                                                   |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``redundant_pardef``               | This issue is responsible for detecting redundant paradigms |
|                                    | in monodix files. (Optional, defaults to 'False'.)          |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``repeated_attributes_pardef``     | This issue is responsible for checking any repeated entries |
|                                    | in the attributes associated with an entry in the parameter |
|                                    | definition section n monodix files. (Optional, defaults to  |
|                                    | 'False'.)                                                   |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``repeated_def_label``             | This function detects and reports repeated def-labels in    |
|                                    | tagger files. (Optional, defaults to 'True'.)               |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``repeated_entries_attr_item``     | Again another simple issue that checks for repeated         |
|                                    | attr­items in def­attr. (Optional, defaults to 'False'.)    |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``repeated_entries_cat_item``      | Simple check which iterates over all the `<cat­item>`s in a |
|                                    | `<def­cat>` and detects repeated `<cat­items>` (Optional,   |
|                                    | defaults to 'False'.)                                       |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``repeated_entries_main_section``  | This issue is responsible for detecting repeated entries in |
|                                    | main section in monodix files. (Optional, defaults to       |
|                                    | 'False'.)                                                   |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``repeated_entries_pardef``        | This issue is responsible for detecting repeated entries in |
|                                    | the parameter definition entries for a given paradigm in    |
|                                    | monodix files. (Optional, defaults to 'False'.)             |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``repeated_entries``               | Checks and reports repeated entries in the bidix.           |
|                                    | (Optional, defaults to 'False'.)                            |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``repeated_program``               | Every modes file consits of various programs and there is   |
|                                    | always a chance that a certain program may unintentionally  |
|                                    | get repeated. (Optional, defaults to 'False'.)              |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``repeated_tag_entries``           | Same as `repeated_attributes_pardef`, but include repeated  |
|                                    | entries in the `<s>` and `<par>` tags in the Main Section.  |
|                                    | (Optional, defaults to 'False'.)                            |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``unused_def_cats``                | The lint can now detect and report redundant def­cats that  |
|                                    | maybe present in the transfer rules definition but are      |
|                                    | never actually used. (Optional, defaults to 'False'.)       |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``unused_paradigms``               | This issue is used for detecting unused paradigms in the    |
|                                    | parameter definitions section in monodix files. (Optional,  |
|                                    | defaults to 'False'.)                                       |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``unwanted_tag``                   | This issue detects extra/unwanted `<b/>` tags that might    |
|                                    | creep into entries in monodix files. (Optional, defaults to |
|                                    | 'False'.)                                                   |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``unwanted_white_space``           | This issue detects and reports white spaces that may creep  |
|                                    | into the entries in bidix files. (Optional, defaults to     |
|                                    | 'False'.)                                                   |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``validate_label_sequence``        | This function lints and detects and labels in <forbid> that |
|                                    | are absent in `<tagset>`. (Optional, defaults to 'False'.)  |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``validate_program``               | This function validates every program mentioned in the      |
|                                    | modes file. (Optional, defaults to 'False'.)                |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``verify_invariable_part``         | This issue is responsible for detecting homogeneity in      |
|                                    | definition of the invariable part across the monodix and    |
|                                    | the bidix. (Optional, defaults to 'False'.)                 |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+
|                                    |                                                             |
| ``xsd_validation``                 | XSD Validation for transfer files, takes care of issues     |
|                                    | such as Repeated def­cats, Repeated def­attrs, Repeted      |
|                                    | def­list, Valid side : ‘sl’ or ‘tl’ and Repeated def­macro  |
|                                    | (Optional, defaults to 'True'.)                             |
|                                    |                                                             |
+------------------------------------+-------------------------------------------------------------+


Dependencies
------------

* ``pip`` - ``apertium-lint``
* ``pip`` - ``lxml``


Can Detect
----------

* Duplication
* Formatting
* Redundancy
* Syntax
* Undefined Element
* Unused Code

License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
