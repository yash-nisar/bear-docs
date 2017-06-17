`TextLintBear <https://github.com/coala/coala-bears/tree/master/bears/general/TextLintBear.py>`_
================================================================================================

The pluggable linting tool for text and Markdown. It is similar to ESLint,
but covers natural language instead.

`Supported Languages <../README.rst>`_
--------------------------------------

* HTML
* Markdown
* reStructuredText

Settings
--------

+---------------------------------------------+-------------------------------------------------------------+
| Setting                                     |  Meaning                                                    |
+=============================================+=============================================================+
|                                             |                                                             |
| ``allow_adverbs``                           | Allows adverbs that can weaken the meaning, such as:        |
|                                             | ``really``, ``very``, ``extremely``, etc. (Optional,        |
|                                             | defaults to 'True'.)                                        |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``allow_ambiguous_words``                   | Allows "weasel words", for example "often" or "probably".   |
|                                             | (Optional, defaults to 'True'.)                             |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``allow_cliche_phrases``                    | Allows common cliche phrases in the sentence. For example:  |
|                                             | In the sentence "Writing specs puts me at loose ends.", "at |
|                                             | loose ends" is a cliche. (Optional, defaults to 'True'.)    |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``allow_extra_words``                       | Allows wordy phrases and unnecessary words. (Optional,      |
|                                             | defaults to 'True'.)                                        |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``allow_passive_voice``                     | Allows passive voice. (Optional, defaults to 'True'.)       +
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``allow_repeated_words``                    | Allows lexical illusions, i.e. cases where a word is        |
|                                             | repeated. (Optional, defaults to 'True'.)                   |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``allow_so_beginning``                      | Allows ``So`` at the beginning of a sentence. (Optional,    |
|                                             | defaults to 'True'.)                                        |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``allow_there_is``                          | Allows ``There is`` or ``There are`` at the beginning of a  |
|                                             | sentence. (Optional, defaults to 'True'.)                   |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``base_uri``                                | The base URI to be used for resolving relative URIs.        |
|                                             | (Optional, defaults to ''.)                                 |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``check_common_misspellings``               | This rule helps to find common misspellings from            |
|                                             | Wikipedia's list of common misspellings. (Optional,         |
|                                             | defaults to 'True'.)                                        |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``check_date_weekday_mismatch``             | This rule finds a mismatch between a date and the           |
|                                             | corresponding weekday. (Optional, defaults to 'True'.)      |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``check_grammar``                           | This rule checks your English grammar with Ginger           |
|                                             | Proofreading. (Optional, defaults to 'True'.)               |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``check_relative_links``                    | This rule enables dead link checks against relative URIs.   |
|                                             | Note that you also have to specify the ``base_uri`` to make |
|                                             | this option work. (Optional, defaults to 'False'.)          |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``check_todos``                             | This rule checks for occurrences of ``- [ ]`` (so called    |
|                                             | task lists). (Optional, defaults to 'None'.)                |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``check_with_alex``                         | This rule helps you find gender favouring, polarising, race |
|                                             | related, religion inconsiderate, or other unequal phrasing  |
|                                             | and checks for: - Gendered work-titles, for example warning |
|                                             | about ``garbageman`` and suggesting ``garbage collector``   |
|                                             | instead - Gendered proverbs, such as warning about ``like a |
|                                             | man`` and suggesting ``bravely`` instead, or warning about  |
|                                             | ``ladylike`` and suggesting ``courteous`` - Blunt phrases,  |
|                                             | such as warning about ``cripple`` and suggesting ``person   |
|                                             | with a limp`` instead - Intolerant phrasing, such as        |
|                                             | warning about using ``master`` and ``slave`` together, and  |
|                                             | suggesting ``primary`` and ``replica`` instead (Optional,   |
|                                             | defaults to 'True'.)                                        |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``check_with_rousseau``                     | This rule checks English writing using Rousseau, which is a |
|                                             | lightweight proofreader written in JavaScript. It can       |
|                                             | check: - Passive voice - Lexical illusions – cases where a  |
|                                             | word is repeated - 'So' at the beginning of the sentence -  |
|                                             | Adverbs that can weaken meaning: really, very, extremely,   |
|                                             | etc. - Readability of sentences - Simpler expressions -     |
|                                             | Weasel words - If a sentence is preceded by a space - If    |
|                                             | there is no space between a sentence and its ending         |
|                                             | punctuation - If sentences are starting with uppercase      |
|                                             | letter (Optional, defaults to 'True'.)                      |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``dont_start_with_duplicated_conjunction``  | This rule checks whether your sentence starts with a        |
|                                             | duplicated conjunction. (Optional, defaults to 'True'.)     |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``ignore_acronyms``                         | A list that contains the acronyms to ignore. (Optional,     |
|                                             | defaults to '[]'.)                                          |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``link_ignore_list``                        | A list of URIs to be ignored, i.e. skipped from             |
|                                             | availability checks. (Optional, defaults to '[]'.)          |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``max_comma_per_sentence``                  | Number of commas allowed per sentence. (Optional, defaults  |
|                                             | to '4'.)                                                    |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``max_lines_per_file``                      | Number of lines allowed per file. (Optional, defaults to    |
|                                             | '300'.)                                                     |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``maximum_acronym_length``                  | Maximum length for unexpanded acronyms. (Optional, defaults |
|                                             | to '5'.)                                                    |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``minimum_acronym_length``                  | Minimum length for unexpanded acronyms. (Optional, defaults |
|                                             | to '3'.)                                                    |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``no_empty_section``                        | This rule does not allow to create an empty section. For    |
|                                             | example, there is an empty section ``# Header A`` below::   |
|                                             | # Header A                                                  |
|                                             | # Header B Text.                                            |
|                                             | (Optional, defaults to 'True'.)                             |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``no_good_words``                           | Set of NG (No Good) words to check for. (Optional, defaults |
|                                             | to '[]'.)                                                   |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``period_in_list_item``                     | Checks whether a sentence in a list item ends with a        |
|                                             | period. (Optional, defaults to 'True'.)                     |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+
|                                             |                                                             |
| ``textlint_config``                         | The location of the ``.textlintrc`` config file. (Optional, |
|                                             | defaults to ''.)                                            |
|                                             |                                                             |
+---------------------------------------------+-------------------------------------------------------------+


Dependencies
------------

* ``npm`` - ``textlint-plugin-asciidoc-loose``
* ``npm`` - ``textlint-plugin-html``
* ``npm`` - ``textlint-plugin-review``
* ``npm`` - ``textlint-plugin-rst``
* ``npm`` - ``textlint-rule-alex``
* ``npm`` - ``textlint-rule-common-misspellings``
* ``npm`` - ``textlint-rule-date-weekday-mismatch``
* ``npm`` - ``textlint-rule-ginger``
* ``npm`` - ``textlint-rule-max-comma``
* ``npm`` - ``textlint-rule-max-number-of-lines``
* ``npm`` - ``textlint-rule-ng-word``
* ``npm`` - ``textlint-rule-no-dead-link``
* ``npm`` - ``textlint-rule-no-empty-section``
* ``npm`` - ``textlint-rule-no-start-duplicated-conjunction``
* ``npm`` - ``textlint-rule-no-todo``
* ``npm`` - ``textlint-rule-period-in-list-item``
* ``npm`` - ``textlint-rule-rousseau``
* ``npm`` - ``textlint-rule-unexpanded-acronym``
* ``npm`` - ``textlint-rule-write-good``
* ``npm`` - ``textlint``
* ``pip`` - ``docutils-ast-writer``


Can Detect
----------

* Formatting
* Grammar
* Spelling

License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
