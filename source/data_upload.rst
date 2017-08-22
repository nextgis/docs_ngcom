.. _ngcom_data_upload:

How to upload data
================================

Raster and vector geodata are uploaded to :ref:`Web GIS <ngcom_description>` by creation of resources :ref:`Raster layer <ngcom_raster_layer>` and :ref:`Vector layer <ngcom_vector_layer>`.

.. _ngcom_raster_layer:

Raster data
-------------------------------

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a data layer (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> Raster layer` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab and select a file with raster geodata in :guilabel:`Raster layer` tab;
#. Press :guilabel:`Create` button. If Raster layer is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. warning:: 
	Only upload of :term:`GeoTIFF` files with 3 or 4 bands (RGB or RGBA) is supported.

.. figure:: _static/Raster_layer.gif
   :name: Raster_layer
   :align: center
   :width: 850px

Read more about upload of raster geodata to Web GIS :ref:`here <ngw_create_raster_layer>`. 

If you plan to display Raster layer on :ref:`Web map <ngcom_webmap_create>` or publish it using :term:`WMS` protocol you need to create :ref:`Style <ngcom_styles>` for it.

.. _ngcom_vector_layer:

Vector data
-------------------------------

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a data layer (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> Vector layer` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab, then select a file with vector geodata and specify its encoding in :guilabel:`Vector layer` tab;
#. Press :guilabel:`Create` button. If Vector layer is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. warning:: 
	Only upload of :term:`ESRI Shape` files (zip-archived, UTF-8 or Windows-1251) and :term:`GeoJSON` files (UTF-8) is supported. Uploaded files can't inculde mixed or invalid geometries, dates can't have NULL values, attributes' columns can't have the name "id" ("ID"). ESRI Shapefiles can't include multigeometries.

.. figure:: _static/Vector_layer.gif
   :name: Vector_layer
   :align: center
   :width: 850px

Read more about upload of vector geodata to Web GIS :ref:`here <ngw_create_vector_layer>`.

If you plan to display Vector layer on :ref:`Web map <ngcom_webmap_create>` or publish it using :term:`WMS` protocol you need to create :ref:`Style <ngcom_styles>` for it.

.. note:: 
	You can also upload raster and vector geodata to Web GIS :ref:`with desktop app NextGIS QGIS <ngcom_ngqgis_connect_data_upload>`.
