.. _usage-reference:

Usage
=====

This section describes how to use the Filabel module. It presumes, that you have successfully installed this module. If you are unsure how to install Filabel, please see :doc:`../installation/index`.

There are two main ways to use Filabel. Either through its command-line interface, or by directly importing the classes you need. Please choose the section that adresses your needs.

.. toctree::
    :maxdepth: 2

    cli_examples
    code_examples


The other option is to deploy Filabel as a web application. To do so, you have to specify the secret webhook key in auth configuration file (see the example in config folder), then you can proceed with the Flask `docs`__.

.. _docs: http://flask.pocoo.org/docs/1.0/tutorial/deploy/
__ docs_