======
Levmar
======

A Python binding to the levmar library.


Description
===========

The levmar is GPL'ed ANSI C implementation of the Levenberg-Marquardt
(LM) optimization algorithm.  The LM algorithm provides a numerical
solution to the problem of minimizing a function over a parameter space
of a function.  The levmar library provides implementation of both
unconstrained and constrained LM algorithms (box, linear equation, and
linear inequality constraints).


Installation
============

Building Levmar requires the following software installed:

* Python (>=2.6)
* NumPy (>=1.3)
* [optional] nose (>=0.11)

nose is required to execute tests.  Additionally, some of demo scripts
in ``./examples`` require matplotlib (>=0.99) installed.

In order to build Levmar, simply do::

    $ python setup.py build
    $ python setup.py install

Then, verify a successful installation::

    $ python -c "import levmar; levmar.test()"


If you downloaded Levmar from a GitHub repository, you need to have
Cython (>=0.12) installed.

::

    $ cython -v levmar/_core.pyx
    $ python setup.py build
    $ python setup.py install
    $ python -c "import levmar; levmar.test()"

If you just want to try Levmar without installing it, build it
in-place::

    $ (cython -v levmar/_core.pyx)
    $ python setup.py build_ext --inplace -f
    [Set up PYTHONPATH appropriately]
    $ python -c "import levmar; levmar.test()"


Documentation
=============

See docstrings and demo scripts contained in the directory
``./examples``.  Documentation of the levmar library can be found at
http://www.ics.forth.gr/~lourakis/levmar/.


Authors
=======

Takeshi Kanmae <tkanmae@gmail.com>


License
=======

The MIT license applies to all the files except those in
``./levmar-2.5``.  All of the software in ``./levmar-2.5`` and only the
software therein is copyrighted by Manolis Lourakis and is licensed
under the terms and conditions of the GNU General Public License (GPL).
See the file LICENSE.txt.


Resources
=========

* levmar: http://www.ics.forth.gr/~lourakis/levmar/
* Python: http://www.python.org/
* NumPy: http://www.scipy.org/
* nose: http://somethingaboutorange.com/mrl/projects/nose
* Cython: http://www.cython.org/


.. # vim: ft=rst tw=72
