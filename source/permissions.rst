.. sectionauthor:: Роман Гайнуллов <roman.gainullov@nextgis.ru>

.. _ngcom_permissions_intro:

Managing access rights
================================

This section will help you set up access to your Web GIS for various users. Below you'll find an overview of the permissions system and some common cases of setting up access.


Terms
-------------

.. figure:: _static/resource_permissions_tab_en.png
   :name: resource_permissions_tab_pic
   :align: center
   :width: 20cm

   Permissions tab

There are two base rules:

1. **Resource approach**

Main (root) resource group (0) > Group 1 > Group 2 > Layer.

Permission for the root group > Permission for Group 1 > Permission for Group 2 > Permission for the layer.

.. important::
	! Without permission to read the main resource group user cannot view any files it contains.

.. list-table::


   * - **Resource**
     - Root (0)
     - Folder 1
     - Folder 2
     - Layer
   * - **Permission**
     - Read
     - Read
     - Read
     - Read


You can select a specific resource type that will be affected by the permission.

Other than that, there are two main options to apply a permission:

* This resource only - it will only affect the resource itself.
* This and subresources - it will affect all resources within, subgroups and their contents.

.. figure:: _static/permission_apply_en.png
   :name: permission_apply_pic
   :align: center


   Selecting permission application

2. By default users have NO permissions.

.. important::
	! Everything is forbidden unless explicitly allowed by the administrator.

The only way a user gets access to data is by having access granted by a permission.


Types of principals (users)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Administrator - Web GIS user with administrative rights
* Owner - Web GIS user who has created the particular resource for which the permission is given
* Guest - user that has not logged in
* Authenticated - Web GIS user who's logged in with any existing account (a.k.a. not a guest)
* Everyone - this includes both guests and users logged in with existing account


Types of rules - what can be allowed or denied
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. list-table::

   * - Resource: All permissions
     - Any actions with resources, except resource groups
   * - Resource: Read
     - Read resources
   * - Resource: Create
     - Create resources
   * - Resource: Modify
     - Edit resources
   * - Resource: Delete
     - Delete resources
   * - Resource: Manage subresources
     - Configure included (child) resource
   * - Resource: Configure permissions
     - Edit access permissions for the resources
   * - Metadata: All permissions 
     - Any actions on metadata
   * - Metadata: Read
     - Edit metadata
   * - Metadata: Modify 
     - Read metadata
   * - Data structure: All permissions 
     - Any actions with the data structure
   * - Data structure: Read
     - Read data structure
   * - Data structure: Modify 
     - Edit data structure
   * - Data: All permissions 
     - Any actions with the data
   * - Data: Read
     - Read data
   * - Data: Modify 
     - Edit data
   * - Connection: All permissions
     - Any actions with the connections
   * - Connection: Read
     - Read connection settings
   * - Connection: Configure
     - Edit connections
   * - Connection: Use
     - Use connections (gives to the user access to the layers and data of the connection)
   * - Service: All permissions
     - Any actions with the service
   * - Service: Access
     - Connect to the service
   * - Service: Configure
     - Edit service settings
   * - Web Map: All permissions
     - Any actions with the Web Maps
   * - Web Map: Open
     - View Web Map
   * - Web Map: View annotations
     - View Web Map annotations
   * - Web Map: Draw annotations
     - Add annotations to Web Maps
   * - Web Map: Manage annotations
     - Edit Web Map annotations
   * - Collector: All permissions
     - Any actions with the Collector project 
   * - Collector: Read
     - Read Collector data







