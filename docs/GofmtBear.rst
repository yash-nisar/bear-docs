`GofmtBear <https://github.com/coala/coala-bears/tree/master/bears/go/GofmtBear.py>`_
=====================================================================================

Suggest better formatting options in Go code. Basic checks like alignment,
indentation, and redundant parentheses are provided.

This is done using the ``gofmt`` utility. For more information visit
<https://golang.org/cmd/gofmt/>.

`Supported Languages <../README.rst>`_
--------------------------------------

* Go

Settings
--------

+---------------+---------------------------------------------------------+
| Setting       |  Meaning                                                |
+===============+=========================================================+
|               |                                                         |
| ``simplify``  | Tries to simplify code (Optional, defaults to 'False'.) +
|               |                                                         |
+---------------+---------------------------------------------------------+


Demo
----

|asciicast|

.. |asciicast| image:: https://asciinema.org/a/94812.png
   :target: https://asciinema.org/a/94812?autoplay=1
   :width: 100%

Dependencies
------------

* ``go`` - ``golang.org/cmd/gofmt``


Can Detect
----------

* Code Simplification
* Formatting

Can Fix
----------

* Code Simplification
* Formatting

License
-------

AGPL-3.0

Authors
-------

* The coala developers (coala-devel@googlegroups.com)
