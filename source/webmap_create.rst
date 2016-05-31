.. _ngcom_webmap_create:

How to display data on web map
===================================

:ref:`Web GIS <ngcom_description>` allows you to display geodata on Web map and view it through built-in :ref:`web client <ngw_webmaps_client>`.

Create Web map 
----------------------------

.. warning:: 
	Make sure all :ref:`Vector layers <ngcom_vector_layer>`, :ref:`Raster layers <ngcom_raster_layer>` and :ref:`PostGIS layers <ngcom_postgis_layer>` which you want to display on Web map have :ref:`Styles <ngcom_styles>` created for them.

.. note:: 
	If you're using `cloud service <http://nextgis.com/>`_  **nextgis.com** your Web GIS already has one ready-to-use Web map. You can use it for geodata visualization or create an unlimited number of new Web maps.

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create Web map (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> Web map` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab;
#. Set Web map :term:`extent` in :guilabel:`Extent and bookmarks` tab (optional);
#. Go to :guilabel:`Layers` tab and in dialog window :guilabel:`Add layer` select those resources (:ref:`Styles <ngcom_styles>` or :ref:`WMS layers <ngcom_wms_layer>`) which you want to display on your Web map;
#. Press :guilabel:`Create` button. If Web map is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. note:: 
	You can set the content of geodata attributes displayed on Web map in Vector layers and PostGIS layers settings. Read more about this option :ref:`here <ngw_attributes>`.

Read more about Web map creation :ref:`here <ngw_webmaps_admin>`.

Open Web map
--------------------------------------------------

#. Go to the Properties window of Web map from the relevant :ref:`Resource group <ngcom_resources_group>`;
#. Select :menuselection:`Web map --> Display` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`. Web map will open in a web client which allows to view and edit geodata.

Read more about Web map web client :ref:`here <ngw_webmaps_client>`.
