.. sectionauthor:: Roman Gainullov <roman.gainullov@nextgis.com>

How to hide the ability to export data option from the user
==========================================================

.. note:: 
   This option is available only to users with Administrator rights.

To hide the ability to export data from Web GIS from certain categories of users, you need to:

* Go to Control Panel -> Settings -> `Resource export <https://docs.nextgis.com/docs_ngweb/source/admin_tasks.html#resource-export>`_
* Select the type of users that **will be able** to export data (only administrators / users with Data:Read or Data:write permissions)

Users who do not fit the selected list will not see the Export link in the interface.

.. note:: 
   This setting does not in any way affect the ability to receive data through the `REST API <https://docs.nextgis.com/docs_ngweb_dev/doc/developer/toc.html>`_ in accordance
   with the set `permissions <https://docs.nextgis.com/docs_ngweb/source/admin_tasks.html#access-management>`_ to them.
