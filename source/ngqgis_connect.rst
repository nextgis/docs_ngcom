.. _ngcom_ngqgis_connect:

How to manage data with desktop app NextGIS QGIS
====================================================================================================

You can upload, edit and perform other operations with geodata in your :ref:`Web GIS <ngcom_description>` not only in :ref:`admin console <ngw_admin_interface>` but also with desktop app `NextGIS QGIS <http://nextgis.ru/nextgis-qgis/>`_.

To make it super-easy we've created `NextGIS Connect <https://plugins.qgis.org/plugins/nextgis_connect/>`_ plugin. After successfull installation you'll see :guilabel:`NextGIS Resources` panel on the right side of the screen.

.. _ngcom_ngqgis_connect_connection:

Establishing Web GIS connection
-----------------------------------

First you need to establish a connection to your Web GIS:

* Open :guilabel:`Settings` dialog from NextGIS Connect control panel;
* Fill in fields :guilabel:`URL` (for example, http://examples.nextgis.com) and :guilabel:`Name` (this name will be used in a list of available connections). In order to be able to create and delete resources uncheck a checkbox :guilabel:`As guest` and fill in fields :guilabel:`User name`and :guilabel:`Password`;
* Press :guilabel:`Ок` button. If the connection is established successfully you'll see your Web GIS resources tree in the plugin window.

.. _ngcom_ngqgis_connect_data_upload:

Creating and uploading data
------------------------------------------------

NextGIS Connect plugin enables a fast upload of raster and vector data and whole QGIS projects to Web GIS. You'll be able to publish your maps and geodata online very quick and easy.

.. warning:: 
	When uploading files using NextGIS Connect the same data format limitations are in place as with uploading using :ref:`admin console <ngcom_data_upload>`.

.. warning:: 
	When creating vector layers in QGIS from scratch for further upload to Web GIS use :term:`coordinate system` EPSG:3857.

1. Creating and uploading vector data to Web GIS:

* Create in QGIS from scratch or upload from files vector layers :term:`ESRI Shape` or :term:`GeoJSON`. Taylor their styles;
* Select in NextGIS Connect Resources panel :ref:`Resource group <ngcom_resources_group>` to which you want to upload your data;
* Select in QGIS Layers panel a vector layer which you want to upload to Web GIS;
* Press :guilabel:`Import selected layer` button on NextGIS Connect control panel or select :menuselection:`NextGIS Connect --> Import selected layer` in layer context menu;
* If data is uploaded successfully you'll see in the relevant Resource group a new :ref:`Vector layer <ngcom_data_upload>` with :ref:`QGIS style <ngcom_styles>` tailored by you.

2. Uploading raster data to Web GIS:

* Upload to QGIS from files raster layers :term:`GeoTIFF`;
* Select in NextGIS Connect Resources panel Resource group to which you want to upload your data;
* Select in QGIS Layers panel a raster layer which you want to upload to Web GIS;
* Press :guilabel:`Import selected layer` button on NextGIS Connect control panel or select :menuselection:`NextGIS Connect --> Import selected layer` in layer context menu;
* If data is uploaded successfully you'll see in the relevant Resource group a new :ref:`Raster layer <ngcom_data_upload>` with default :ref:`Raster style <ngcom_styles>`.

3. Creating and uploading a whole QGIS project to Web GIS:

* Create a QGIS project with raster and vector layers. Tailor their styles, group them, set their hierarchy and visibility settings. Set the map extent;
* Select in NextGIS Connect Resources panel :ref:`Resource group <ngcom_resources_group>` to which you want to upload the project;
* Press :guilabel:`Import current project` button on NextGIS Connect control panel or select :menuselection:`NextGIS Connect --> Import current project` in any layer context menu;
* In the opened dialog window fill in the name of the new Resource group to which the project will be imported;
* If the project is uploaded successfully you'll see in a selected Resource group a newly created group with: 1) all Raster and Vector layers to which :guilabel:`Import selected layer` is applicable, and their Styles; 2) :ref:`Web map <ngcom_webmap_create>` with a set extent, to which all the imported layers are added with groups, hierarchy and visibility settings similar to QGIS.

.. note:: 
	The fastest way to go to the newly created Web map is by pressing :guilabel:`Open map in browser` button on NextGIS Connect control panel or select :guilabel:`Open map in browser` in map's context layer.

.. _ngcom_ngqgis_connect_wfs_service:

Creating WFS services
--------------------------------------------------------------

NextGIS Connect plugin enables a fast publication of Vector layers from your Web GIS using standard :term:`WFS` protocol. 

It's possible due to the quick creation of :ref:`WFS service <ngcom_resources_group>` option in NextGIS Connect:

* Select in NextGIS Connect Resources panel Vector layer which you want to publish using WFS protocol;
* Select :guilabel:`Create WFS service` in layer context menu;
* In the opened dialog window set the number of layer's features to be published via WFS service by changing the value of the field :guilabel:`The number of objects returned by default`;
* If WFS service is created successfully you'll see it in the relevant Resource group. The Vector layer is alreay connected to it.

.. note:: 
	You can edit settings of WFS service (including its name, published layers and their settings) in Web GIS admin console.

.. _ngcom_ngqgis_connect_data_edit:

Editing data
---------------------------------------------------------------

NextGIS Connect plugin enables an easy editing of geometries and attributes of Vector layers features. 

It's possible due to the use of standard :term:`WFS` protocol (with feature edit support):

* :ref:`Publish via WFS protocol <ngcom_ngqgis_connect_wfs_service>` Vector layer which features you're going to edit;
* Select in NextGIS Connect Resources panel the relevant WFS service;
* Press :guilabel:`Add to QGIS` button on NextGIS Connect control panel or select :guilabel:`Add to QGIS` in service context menu;
* If operation is successful you'll see in QGIS Layers panel a new group of WFS layers published via selected WFS service;
* Edit features' geometries and attributes in added WFS layers using standard QGIS tools;
* If editing went successful you'll be able to see the changes at once in Web GIS :ref:`Feature table <ngw_feature_table>` and Web map :ref:`web client <ngw_webmaps_client>`.


.. _ngcom_ngqgis_connect_data_export:

Exporting data
--------------------------------------------------------

NextGIS Connect plugin enables a fast export of vector data from Web GIS to QGIS for further processing, analysis, saving in different formats and other data operations.

It's possible due to the option of fast creation of GeoJSON vector layers in QGIS using vector data from Web GIS:

* Select in NextGIS Connect Resources panel Vector layer which you want to export to QGIS;
* Press :guilabel:`Add to QGIS` button on NextGIS Connect control panel or select :guilabel:`Add to QGIS` in layer context menu;
* If the layer is exported successfully you'll see in QGIS Layers panel a new GeoJSON vector layer which you can use in your projects or save to your device in a required format.

.. note:: 
	Geometry and attributes data export is supported. Styles, descriptions, metadata and images of the objects can't be exported in the described way.

.. _ngcom_ngqgis_connect_resource_group:

Creating Resource groups
-------------------------------------------------------------------

NextGIS Connect plugin enables a fast creation of Resource groups in Web GIS. For that:

* Select in NextGIS Connect Resources panel Resource group where you want to create a new Group;
* Press :guilabel:`Create new group` button on NextGIS Connect control panel or select :guilabel:`Create new group` in group context menu;
* In the opened dialog window fill in the name of the new Resource group;
* If Resource group is created successfully you'll see it in the Web GIS resources tree in the plugin window.

.. _ngcom_ngqgis_connect_resource_delete:

Deleting resources
--------------------------------------------------------

NextGIS Connect plugin enables a fast deletion of any resources from Web GIS. For that:

* Select in NextGIS Connect Resources panel a resource you want to delete;
* Select :guilabel:`Delete` in resource context menu;
* If resource is deleted successfully it will disappear from Web GIS resources tree in the plugin window.
