.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.

This resource has the following properties:
   
``admin``
   |admin client|
   
``chef_server``
   |chef_server_url|
   
``complete``
   Use to specify if this resource defines a user completely. When ``true``, any property not specified by this resource will be reset to default property values.
   
``email``
   The email address for the user.
   
``external_authentication_uid``
   ...
   
``ignore_failure``
   **Ruby Types:** TrueClass, FalseClass

   |ignore_failure| Default value: ``false``.
   
``name``
   The name of the user.
   
``notifies``
   **Ruby Type:** Symbol, 'Chef::Resource[String]'

   .. include:: ../../includes_resources_common/includes_resources_common_notification_notifies.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_timers.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_notifies_syntax.rst
   
``output_key_format``
   Use to specify the format of a public key. Possible values: ``pem``, ``der``, or ``openssh``. Default value: ``openssh``.
   
``output_key_path``
   Use to specify the path to the location in which a public key will be written.
   
``raw_json``
   The user as |json| data. For example:
       
   .. code-block:: javascript
       
      {
        "name": "Robert Forster"
      }
   
``recovery_authentication_enabled``
   ...
   
``retries``
   **Ruby Type:** Integer

   |retries| Default value: ``0``.
   
``retry_delay``
   **Ruby Type:** Integer

   |retry_delay| Default value: ``2``.
   
``source_key``
   Use to copy a public or private key, but apply a different ``format`` and ``password``. Use in conjunction with ``source_key_pass_phrase``` and ``source_key_path``.
   
``source_key_pass_phrase``
   The pass phrase for the public key. Use in conjunction with ``source_key``` and ``source_key_path``.
   
``source_key_path``
   The path to the public key. Use in conjunction with ``source_key``` and ``source_key_pass_phrase``.
   
``subscribes``
   **Ruby Type:** Symbol, 'Chef::Resource[String]'

   .. include:: ../../includes_resources_common/includes_resources_common_notification_subscribes.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_timers.rst

   .. include:: ../../includes_resources_common/includes_resources_common_notification_subscribes_syntax.rst
