..
        SPDX-License-Identifier: CC-BY-SA-4.0 or-later

Antispam
========

Reset the password
------------------

If you have forgotten the initial password or just want to set a new password
you can do that with the following commands:

.. code-block::

	PASSWORD="YourNewPassword"
	NEWPASS=$(printf 'password = "%s";\n' $(rspamadm pw -p "${PASSWORD}"))
	sed -i -n -e '/^password/!p;$a \'"$NEWPASS" /etc/grommunio-antispam/local.d/worker-controller.inc

.. meta::
   :description: grommunio Knowledge Database
   :keywords: grommunio Knowledge Database
   :author: grommunio GmbH
   :publisher: grommunio GmbH
   :copyright: grommunio GmbH, 2022
   :page-topic: software
   :page-type: documentation
   :robots: index, follow
