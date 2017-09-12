.. _ngcom_styles:

How to create map styles for data visualization
=================================================

Style is a special type of resource necessary for geodata visualization on :ref:`Web map <ngcom_webmap_create>` or with :ref:`WMS service <ngcom_wms_service>`. When displaying a data layer on Web map of publishing it using :term:`WMS` protocol you actually use its style which describes how geodata is visually presented on a map. 

The only exception are :ref:`WMS layers <ngcom_wms_layer>` which don't need you to create Styles, because the information about their visualization is passed to :ref:`Web GIS <ngcom_description>` from the external WMS server.

For :ref:`Vector <ngcom_vector_layer>` and :ref:`PostGIS <ngcom_postgis_layer>` layers Web GIS supports two types of Styles - :ref:`MapServer style <ngcom_mapserver_style>` and :ref:`QGIS style <ngcom_qgis_style>`. For :ref:`Raster layers <ngcom_raster_layer>` Web GIS allows you to create :ref:`Raster style <ngcom_raster_style>`.

.. _ngcom_mapserver_style:

MapServer style
----------------------------

#. Open the Properties page of :ref:`Vector layer <ngcom_vector_layer>` or :ref:`PostGIS layer <ngcom_postgis_layer>` for which you want to create a style;
#. Select :menuselection:`Create resource --> MapServer style` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab. You can edit style parameters in :guilabel:`MapServer style` tab (optional). Examples of :term:`MapServer` style can be found :ref:`here <ngw_mapserver_templates>`;
#. Press :guilabel:`Create` button. If Style is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Vector layer or PostGIS layer.

.. figure:: _static/Mapserver_style.gif
   :name: Mapserver_style
   :align: center
   :width: 850px

.. _ngcom_qgis_style:

QGIS style
-----------------------

#. Open the Properties page of :ref:`Vector layer <ngcom_vector_layer>` or :ref:`PostGIS layer <ngcom_postgis_layer>` for which you want to create a style;
#. Select :menuselection:`Create resource --> QGIS style` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab;
#. In :guilabel:`QGIS style` tab upload a file in :term:`QML` format created with :term:`QGIS`;
#. Press :guilabel:`Create` button. If Style is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Vector layer or PostGIS layer.

.. note:: 
	For Vector layers uploaded to Web GIS :ref:`with desktop app NextGIS QGIS <ngcom_ngqgis_connect_data_upload>` QGIS style is created automatically.

.. figure:: _static/QGIS_style.gif
   :name: QGIS_style
   :align: center
   :width: 850px

.. _ngcom_raster_style:

Raster style
-----------------------------

#. Open the Properties page of :ref:`Raster layer <ngcom_raster_layer>` for which you want to create a style;
#. Select :menuselection:`Create resource --> Raster style` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab;
#. Press :guilabel:`Create` button. If Style is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Raster layer.

.. note:: 
	For Raster layers uploaded to Web GIS :ref:`with desktop app NextGIS QGIS <ngcom_ngqgis_connect_data_upload>` Raster style is created automatically.

.. figure:: _static/Raster_style.gif
   :name: Raster_style
   :align: center
   :width: 850px

Read more about creation and editing of Styles :ref:`here <ngw_style_create>`.
