.. _ngcom_resources_list:

How data is managed
======================

Geodata in :ref:`Web GIS <ngcom_description>` is managed with resource system. At the moment there are following types of resources:

**Resources for managing local sources of geodata**:

* :ref:`Raster layer <ngcom_raster_layer>` (created to upload and store raster geodata)
* :ref:`Vector layer <ngcom_vector_layer>`  (created to upload and store vector geodata)

**Resources for managing external sources of geodata**:

* :ref:`PostGIS connection <ngcom_postgis_connection>` (created to connect to external :term:`PostGIS` database)
* :ref:`PostGIS layer <ngcom_postgis_layer>` (create to connect to the specific table with geodata through existing PostGIS connection)
* :ref:`WMS connection <ngcom_wms_connection>` (created to connect to external :term:`WMS` server)
* :ref:`WMS layer <ngcom_wms_layer>` (created to connect to the specific raster layers through existing WMS connection)

**Resources for displaying and publishing of geodata**:

* :ref:`Style <ngcom_styles>` (special type of resource, created inside Raster layers, Vector layers and PostGIS layers to add them to Web map or publish via WMS protocol) 
* :ref:`Web map <ngcom_webmap_create>` (created to display Raster layers, Vector layers, PostGIS layers and WMS layers on the map through built-in web client) 
* :ref:`WFS service <ngcom_wfs_service>` (created to publish Vector layers and PostGIS layers using :term:`WFS` protocol) 
* :ref:`WMS service <ngcom_wms_service>` (created to publish Raster layers, Vector layers, PostGIS layers and WMS layers using WMS protocol)

**Resources for geodata storage management**:

* :ref:`Resource group <ngcom_resources_group>` (create to provide folderlike data structure)
