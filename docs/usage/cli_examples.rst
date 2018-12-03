CLI examples
============

The help
--------

Filabel has a help option. You can trigger it with this command:
::

    $ python3.7 -m filabel --help

The help is brief and will probably help you faster than reading these examples.

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


Advanced usage
--------------

::

	$ python3.7 -m filabel --config-auth CONFIG_AUTH_FILE \
						   --config-labels CONFIG_LABELS_FILE \
						   --state all
						   --base master
						   --delete-old
						   username/repository_name1 \
						   username/repository_name2


This example defines all the options with default values. To see a short description of these options, see help.