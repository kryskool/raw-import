.. Raw Pages Import documentation master file, created by
   sphinx-quickstart on Sun Apr  1 22:39:39 2012.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Raw Pages Import's documentation!
============================================

Raw Pages Import
================

``raw-import`` is a fork of ``ghp-import`` to be more generic on branch name

This is what ``ghp-import`` was written for.

.. _GitHub: http://github.com/
.. _`GitHub Pages`: http://pages.github.com/
.. _Sphinx: http://sphinx.pocoo.org/
.. _`github-tools`: http://dinoboff.github.com/github-tools/

Big Fat Warning
---------------

This will **DESTROY** your dedicate branch. If you love it, you'll want to take
backups before playing with this. This script assumes that pages is 100%
derivative. You should never edit files in your gh-pages branch by hand if
you're using this script because you will lose your work.

Usage
-----

.. code-block:: bash

    Usage: raw-import [OPTIONS] DIRECTORY

    Options:
      -m MESG     The commit message to use on the gh-pages branch.
      -p          Push the branch to origin/gh-pages after committing.
      -r REMOTE   The name of the remote to push to. [origin]
      -b BRANCH   The name of the dedicate branch. [pages]
      -h, --help  show this help message and exit

Its pretty simple. Inside your repository just run ``raw-import $DOCS_DIR``
where ``$DOCS_DIR`` is the path to the *built* documentation. This will write a
commit to your ``dedicate`` branch with the current documents in it.

If you specify ``-p`` it will also attempt to push the ``dedicate`` branch to
GitHub. By default it'll just run ``git push origin pages``. You can specify
a different remote using the ``-r`` flag.

License
-------

raw-import is distributed under the same license as ghp-import 
(the Tumbolia Public License. See the LICENSE file for more information).

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

