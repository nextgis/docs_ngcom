.. _ngcom_resources_list:

How data is managed
======================

Geodata in :ref:`Web GIS <ngcom_description>` is managed with resource system. At the moment there are following types of resources:

**Resources for managing local sources of geodata**:

* :ref:`Raster layer <ngcom_raster_layer>` (created to upload and store raster geodata)
* :ref:`Vector layer <ngcom_vector_layer>`  (created to upload and store vector geodata)

**Resources for managing external sources of geodata**:

* :ref:`Basemap <ngcom_basemap_layer>` (created to add external basemaps to :ref:`Web maps <ngcom_webmap_create>`)
* :ref:`PostGIS connection <ngcom_postgis_connection>` (created to connect to external :term:`PostGIS` database)
* :ref:`PostGIS layer <ngcom_postgis_layer>` (created to connect to the specific table with geodata through existing PostGIS connection)
* :ref:`WMS connection <ngcom_wms_connection>` (created to connect to an external :term:`WMS` server)
* :ref:`WMS layer <ngcom_wms_layer>` (created to connect to the specific raster layers through existing WMS connection)
* :ref:`TMS connection <ngcom_tms_connection>` (created to connect to an external :term:`TMS` server)
* :ref:`TMS layer <ngcom_tms_layer>` (created to connect to the specific layers using an existing TMS connection)
* `OGC API Features <https://docs.nextgis.com/docs_ngweb/source/layers.html#ogc-api-features-service>`_ (Third party software can use these services to edit vector data on server).

**Resources for displaying and publishing geodata**:

* :ref:`Style <ngcom_styles>` (special type of resource, created inside Raster layers, Vector layers and PostGIS layers to add them to Web map or publish using WMS protocol) 
* :ref:`Web map <ngcom_webmap_create>` (created to display Raster layers, Vector layers, PostGIS layers and WMS layers on the map through built-in :ref:`web client <ngw_webmaps_client>`) 
* :ref:`WFS service <ngcom_wfs_service>` (created to publish Vector layers and PostGIS layers using :term:`WFS` protocol) 
* :ref:`WMS service <ngcom_wms_service>` (created to publish Raster layers, Vector layers, PostGIS layers and WMS layers using WMS protocol)

**Resources for geodata storage management**:

* :ref:`Resource group <ngcom_resources_group>` (created to provide folderlike data structure)
