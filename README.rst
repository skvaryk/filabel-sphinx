Filabel
=======

|license|

Tool for labeling PRs at GitHub by globs.

Installation guide
------------------

Using test PyPi:
::

    $ python3.7 -m pip install --extra-index-url https://testpypi.python.org/pypi/filabel-sphinx


If you do not wish to use test PyPi, then clone the Filabel repository and locate it through command line. 

To initiate the installation, execute **one** of these commands:

Using setup.py directly:
::

    $ python3.7 setup.py install 

Using pip module:
::

    $ python3.7 -m pip install .



Basic usage
-----------

::

	$ python3.7 -m filabel --config-auth CONFIG_AUTH_FILE \
						   --config-labels CONFIG_LABELS_FILE \
						   username/repository_name1 \
						   username/repository_name2

Where ``CONFIG_AUTH_FILENAME`` and ``CONFIG_LABELS_FILE`` are configuration files that can be parsed by `ConfigParser`__. To see how these files are structured, please look at the config directory.

If you are unsure how to setup your GitHub repository's access token, please see `this`__ article.

.. _ConfigParser: https://docs.python.org/3/library/configparser.html
__ ConfigParser_

.. _this: https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/
__ this_



Further documentation
---------------------

If you wish to read the sphinx documentation, you have to install the sphinx module:

::

    $ python3.7 -m pip install sphinx


After installing sphinx, navigate to the docs folder and build the documentation:

::

    $ cd docs
    $ make html

After successful build, open ``docs/_build/html/index.html`` in a web browser of your choice.


The sphinx documentation also contains a few doctests. To run those, navigate again to docs folder and run:

::

    $ cd docs
    $ make doctest

License
-------

The license used is MIT. To read the license, head over to `LICENSE`__.

.. _LICENSE: https://github.com/skvaryk/filabel-sphinx/blob/master/README.rst
__ LICENSE_


.. |license| image:: https://img.shields.io/github/license/cvut/filabel.svg
    :alt: License
    :target: LICENSE
