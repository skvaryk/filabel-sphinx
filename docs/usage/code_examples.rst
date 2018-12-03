Code examples
=============


.. testsetup::

   import os
   username = os.environ.get('GH_USER')
   token = os.environ.get('GH_TOKEN')
   labels_config_path = '../config/labels.example.cfg'


Get pull requests of a GitHub repository
----------------------------------------

.. testcode::

   from filabel.logic import GitHub
   github = GitHub(token)
   repo = 'filabel-testrepo1'
   pr = github.pull_requests(username, repo)
   print(pr[1]['url'])

This prints the url of a the second pull request 


.. testoutput::

   https://api.github.com/repos/skvaryk/filabel-testrepo1/pulls/1


Set labels of a pull request
----------------------------

.. testcode::

   from filabel.logic import GitHub
   github = GitHub(token)
   repo = 'filabel-testrepo1'
   pr_number = 1
   set_labels = github.reset_labels(username, repo, pr_number, ['new label'])
   print(set_labels[0]['name'])

Prints the labels that have been set

.. testoutput::

   new label


Run the whole repository
------------------------

.. testcode::

   from filabel.logic import Filabel
   import configparser
   cfg_labels = configparser.ConfigParser()
   with open(labels_config_path, 'r') as f:
       cfg_labels.read_file(f) 
       filabel = Filabel(token, cfg_labels['labels'])
       repo = 'filabel-testrepo1'
       report = filabel.run_repo(username + "/" + repo)
       print(report.ok)

.. testoutput::
   :hide:

   True


