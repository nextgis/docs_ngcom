.. _ngcom_data_connect:

How to connect data from external sources 
=======================================================

:ref:`Web GIS <ngcom_description>` supports connection of basemaps (:term:`TMS` services) from external servers, vector geodata from external :term:`PostGIS` databases and connection of vector and raster geodata from external :term:`WMS` services. 

.. _ngcom_basemap_layer:

Basemaps
------------


Add a Basemap resource
~~~~~~~~~~~~~~~~~~~~~~

#. Navigate to a :ref:`Resource group <ngcom_resources_group>` where you want to create a basemap resource (by default, from the main page of Web GIS you access the Main resource group);
#. Press **Create resource** and select **Basemap**;
#. In the opened dialog, go to :guilabel:`Resource` tab and type a name for the new basemap in the field :guilabel:`Display name`. Then in :guilabel:`Basemap` tab fill in the field :guilabel:`URL` (if you know the correct link to :term:`TMS` service) or start typing the name of the basemap in the field :guilabel:`Search`. If this basemap is found in `QuickMapServices <https://qms.nextgis.com/>`_ catalog, the :guilabel:`URL` field will be filled in automatically and option "Use options from QMS" will be activated;
#. Press **Create** button. If Basemap is created successfully, you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. note:: 
	We recommend creating a separate "Basemaps" :ref:`Resource group <ngcom_resources_group>` to keep the basemaps to add your :ref:`Web maps <ngcom_webmap_create>`.

Find out how to add basemaps you've created to the Web map :ref:`here <ngcom_webmap_create>`.

.. _ngcom_postgis_connect:

External PostGIS databases
--------------------------

.. _ngcom_postgis_connection:

Create a PostGIS connection
~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a connection (by default, from the main page of Web GIS you access the Main resource group);
#. Press **Create resource** and select **PostGIS connection**;
#. In the opened dialog, go to :guilabel:`Resource` tab and type a name for the new connection in the field :guilabel:`Display name`. Then in :guilabel:`PostGIS connection` tab fill in the fields :guilabel:`Host`, :guilabel:`Database`, :guilabel:`User` (if applicable) and :guilabel:`Password` (if applicable);
#. Press **Create** button. If PostGIS connection is created successfully, you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. _ngcom_postgis_layer:

Create a PostGIS layer
~~~~~~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a data layer (by default, from the main page of Web GIS you access the Main resource group);
#. Press **Create resource** and select **PostGIS layer**;
#. In the opened dialog, go to :guilabel:`Resource` tab and type a name for the new layer in the field :guilabel:`Display name`. Then in :guilabel:`PostGIS layer` tab select :ref:`PostGIS connection <ngcom_postgis_connection>` and fill in the fields :guilabel:`Schema`, :guilabel:`Table`, :guilabel:`ID column` and :guilabel:`Geometry column`;
#. Press **Create** button. If PostGIS layer is created successfully, you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

Read more about connecting to external PostGIS databases :ref:`here <ngw_create_postgis_layer>`.

If you plan to display PostGIS layer on :ref:`Web map <ngcom_webmap_create>` or publish it using :term:`WMS` protocol, you need to create a :ref:`Style <ngcom_styles>` for it.

.. _ngcom_wms_connect:

External WMS services
---------------------

.. note:: 
	Currently supported WMS versions 1.1.1 and 1.3.0.

.. _ngcom_wms_connection:

Create a WMS connection
~~~~~~~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a connection (by default, from the main page of Web GIS you access the Main resource group);
#. Press **Create resource** and select **WMS connection**;
#. In the opened dialog, go to :guilabel:`Resource` tab and type a name for the new connection in the field :guilabel:`Display name`. Then in :guilabel:`WMS connection` tab fill in the fields :guilabel:`URL`, :guilabel:`Username` (if applicable) and :guilabel:`Password` (if applicable) to connect to :term:`WMS` server;
#. Press **Create** button. If WMS connection is created successfully, you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. warning:: 
	WMS server to which you connect must support EPSG:3857 :term:`coordinate system`.

.. _ngcom_wms_layer:

Create a WMS layer
~~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a data layer (by default, from the main page of Web GIS you access the Main resource group);
#. Press **Create resource** and select **WMS layer**;
#. In the opened dialog, go to :guilabel:`Resource` tab and type a name for the new layer in the field :guilabel:`Display name`. Then in :guilabel:`WMS layer` tab select :ref:`WMS connection <ngcom_wms_connection>`, image format and WMS layers you want to add to Web GIS;
#. Press **Create** button. If WMS layer is created successfully, you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

Read more about connecting to external WMS servers :ref:`here <ngw_create_wms_layer>`.

.. _ngcom_tms_connect:

External TMS services
---------------------

.. _ngcom_tms_connection:

Create a TMS connection
~~~~~~~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a connection (by default, from the main page of Web GIS you access the Main resource group);
#. Press **Create resource** and select **TMS connection**;
#. In the opened dialog, go to :guilabel:`Resource` tab and type a name for the new connection in the field :guilabel:`Display name`. Then in :guilabel:`TMS connection` tab select the mode for connection with TMS server (Custom or NextGIS GeoServices) and enter URL template, API key parameters and tile scheme;
#. Press **Create** button. If TMS connection is created successfully, you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. _ngcom_tms_layer:

Create a TMS layer
~~~~~~~~~~~~~~~~~~

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a data layer (by default, from the main page of Web GIS you access the Main resource group);
#. Press **Create resource** and select **TMS layer**;
#. In the opened dialog, go to :guilabel:`Resource` tab and type a name for the new layer in the field :guilabel:`Display name`. Then in the :guilabel:`Tile cache` tab choose cache settings, and in the :guilabel:`TMS layer` tab select the required TMS connection and set up display parameters;
#. Press **Create** button. If TMS layer is created successfully, you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

Read more about connecting to external TMS services :ref:`here <ngw_create_tms_layer>`.
