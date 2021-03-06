.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.


The following example shows how to configure |delivery| to ignore and/or run certain |foodcritic| rules, and to exclude running tests that are located in the specified cookbook directories:

.. code-block:: javascript

   {
     "version": "2",
     "build_cookbook": {
       "name": "delivery-truck",
       "git": "https://github.com/chef-cookbooks/delivery-truck.git"
     },
     "delivery-truck": {
       "lint": {
         "foodcritic": {
           "ignore_rules": ["FC009", "FC057", "FC058"],
           "only_rules": ["FC002"],
           "excludes": ["spec", "test"],
           "fail_tags": ["any"]
         }
       }
     }
   }

where:

* ``ignore_rules`` is set to ignore |foodcritic| rules ``FC009``, ``FC057``, ``FC058``
* ``only_rules`` is set to run only |foodcritic| rule ``FC002``; omit this setting to specify all rules not specified by ``ignore_rules``
* ``excludes`` prevents |foodcritic| rules from running if they are present in a cookbook's ``/spec`` and/or ``/test`` diretories
* ``fail_tags`` states which rules should cause the run to fail; omit this setting to specify ``correctness``
