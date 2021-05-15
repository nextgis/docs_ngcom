.. _ngcom_data_upload:

How to upload data
================================

Raster and vector geodata are uploaded to :ref:`Web GIS <ngcom_description>` by creation of resources :ref:`Raster layer <ngcom_raster_layer>` and :ref:`Vector layer <ngcom_vector_layer>`.

.. note:: 
	The size limit for uploaded files depends on the selected plan. For 'Premium' - 1.0 GB, for 'Free' and 'Mini' - 128 Mb.

.. _ngcom_raster_layer:

Raster data
-----------

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a data layer (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> Raster layer` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab and select a file with raster geodata in :guilabel:`Raster layer` tab;
#. Press :guilabel:`Create` button. If Raster layer is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. warning:: 
	Supported are :term:`GeoTIFF` files with 3 or 4 bands (RGB or RGBA). Inputs must be geographically referenced and have correctly set CRS description as GeoTIFF metadata.

.. figure:: _static/Raster_layer.gif
   :name: Raster_layer
   :align: center
   :width: 850px

Read more about upload of raster geodata to Web GIS :ref:`here <ngw_create_raster_layer>`. 

If you plan to display Raster layer on :ref:`Web map <ngcom_webmap_create>` or publish it using :term:`WMS` protocol you need to create :ref:`Style <ngcom_styles>` for it.

.. _ngcom_vector_layer:

Vector data
-----------

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a data layer (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> Vector layer` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab, then select a file with vector geodata and specify its encoding in :guilabel:`Vector layer` tab;
#. Press :guilabel:`Create` button. If Vector layer is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

Input data requirements
^^^^^^^^^^^^^^^^^^^^^^^

* Supported formats: ESRI Shapefile ((zip-archived, no sub-folders), GeoJSON, GML or KML
* Field names can't be: *id(ID)* or *geom(GEOM)*

Use NextGIS Connect if you need to upload data in other formats.

.. warning:: 
	Avoid using unicode symbols in data field names. While such data can be uploaded, you can experience problems working with it via WFS, in NextGIS Mobile or visualization (especially if styles are using such fields). Use pain latin for field names and set up field aliases to show unicode names.

.. figure:: _static/Vector_layer.gif
   :name: Vector_layer
   :align: center
   :width: 850px

Read more about upload of vector geodata to Web GIS :ref:`here <ngw_create_vector_layer>`.

If you plan to display Vector layer on a :ref:`Web map <ngcom_webmap_create>` or publish it using :term:`WMS` protocol you need to add a :ref:`Style <ngcom_styles>` for it first.

.. note:: 
	You can also upload raster and vector geodata to Web GIS :ref:`with desktop app NextGIS QGIS <ngcom_ngqgis_connect_data_upload>`.
