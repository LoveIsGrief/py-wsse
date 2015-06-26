Contributing
============

Thanks for your interest in contributing! The advice below will help you get
your issue fixed / pull request merged.

Please file bugs and send pull requests to the `GitHub repository`_ and `issue
tracker`_.

.. _GitHub repository: https://github.com/orcasgit/py-wsse/
.. _issue tracker: https://github.com/orcasgit/py-wsse/issues



Submitting Issues
-----------------

Issues are easier to reproduce/resolve when they have:

- A pull request with a failing test demonstrating the issue
- A code example that produces the issue consistently
- A traceback (when applicable)


Pull Requests
-------------

When creating a pull request:

- Write tests (see below)
- Note user-facing changes in the `CHANGES`_ file
- Update the documentation as needed
- Add yourself to the `AUTHORS`_ file

.. _AUTHORS: AUTHORS.rst
.. _CHANGES: CHANGES.rst


Testing
-------

Please add tests for any changes you submit. The tests should fail before your
code changes, and pass with your changes. Existing tests should not
break. Coverage (see below) should remain at 100% following a full tox run.

To install all the requirements for running the tests, first you need to ensure
that the OpenSSL, libxml2, and xmlsec1 headers are available on your system. On
Debian/Ubuntu, ``sudo apt-get install libssl-dev libxml2-dev libxmlsec1-dev``
should take care of that. On RedHat-based systems, try ``sudo yum install
openssl-devel libxml2-devel xmlsec1-devel``. Then run::

    pip install -r requirements.txt

To run the tests once::

    py.test

To run tox (which runs the tests across all supported Python and Django
versions) and generate a coverage report in the ``htmlcov/`` directory::

    make test

This requires that you have ``python2.7``, ``python3.3``, ``python3.4``,
``pypy``, and ``pypy3`` binaries on your system's shell path.
