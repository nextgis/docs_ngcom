.. _ngcom_data_connect:

How to connect data from external sources 
=======================================================

:ref:`Web GIS <ngcom_description>` supports connection of basemaps (:term:`TMS` services) from external servers, vector geodata from external :term:`PostGIS` databases and connection of vector and raster geodata from external :term:`WMS` services. 

.. _ngcom_basemap_layer:

Basemaps
------------
 
.. warning:: 
	Only Mini/Premium users have access to creation of Basemaps.

Create Basemap:
~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a basemap (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> Basemap` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab. Then in :guilabel:`Basemap` tab fill in the field :guilabel:`URL` (if you know the correct link to :term:`TMS` service) or start typing the name of the basemap in the field :guilabel:`Search`. If this basemap will be found in `QuickMapServices <https://qms.nextgis.com/>`_ catalog, then :guilabel:`URL` field will be filled in automatically and option "Use options from QMS" will be activated;
#. Press :guilabel:`Create` button. If Basemap is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. note:: 
	We recommend to create a separate "Basemaps" :ref:`Resource group <ngcom_resources_group>` for storing basemaps which you plan to add to your :ref:`Web maps <ngcom_webmap_create>`.

How to add created basemaps to Web map :ref:`read here <ngcom_webmap_create>`.

.. _ngcom_postgis_connect:

External PostGIS databases
----------------------------------------------

.. _ngcom_postgis_connection:

Create PostGIS connection:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a connection (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> PostGIS connection` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab, then in :guilabel:`PostGIS connection` tab fill in the fields :guilabel:`Host`, :guilabel:`Database`, :guilabel:`User` (if applicable) and :guilabel:`Password` (if applicable);
#. Press :guilabel:`Create` button. If PostGIS connection is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. _ngcom_postgis_layer:

Create PostGIS layer:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a data layer (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> PostGIS layer` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab, then in :guilabel:`PostGIS layer` tab select :ref:`PostGIS connection <ngcom_postgis_connection>` and fill in the fields :guilabel:`Schema`, :guilabel:`Table`, :guilabel:`ID column` and :guilabel:`Geometry column`;
#. Press :guilabel:`Create` button. If PostGIS layer is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

Read more about connection of vector geodata from external PostGIS databases to Web GIS :ref:`here <ngw_create_postgis_layer>`.

If you plan to display PostGIS layer on :ref:`Web map <ngcom_webmap_create>` or publish it using :term:`WMS` protocol you need to create :ref:`Style <ngcom_styles>` for it.

.. _ngcom_wms_connect:

External WMS services
-----------------------------------------------

.. _ngcom_wms_connection:

Create WMS connection:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a connection (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> WMS connection` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab, then in :guilabel:`WMS connection` tab fill in the fields :guilabel:`URL`, :guilabel:`Username` (if applicable) и :guilabel:`Paasword` (if applicable) to connect to :term:`WMS` server;
#. Press :guilabel:`Create` button. If WMS connection is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. warning:: 
	WMS server to which you connect should support :term:`coordinate system` EPSG:3857.

.. _ngcom_wms_layer:

Create WMS layer:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a data layer (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> WMS layer` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab, then in :guilabel:`WMS layer` tab select :ref:`WMS connection <ngcom_wms_connection>`, image format and WMS layers you want to add to Web GIS;
#. Press :guilabel:`Create` button. If WMS layer is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

Read more about connection of geodata from external WMS services to Web GIS :ref:`here <ngw_create_wms_layer>`.
