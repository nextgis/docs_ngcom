.. _ngcom_data_export:

How to export data
======================================

:ref:`Web GIS <ngcom_description>` allows to export data from :ref:`Vector layers <ngcom_vector_layer>` and :ref:`PostGIS layer <ngcom_postgis_layer>` in the following formats:

* :term:`GeoJSON`
* :term:`CSV`
* CSV for Microsoft Excel
* :term:`ESRI Shapefile`
* AutoCAD DXF
* Mapinfo TAB
* MapInfo MIF/MID
* :term:`GeoPackage`.

Depending on the format, additional file components are exported making further use of the exported data more convenient. For example CSVT (field structure description) and PRJ (coordinate system description) are added to CSV and CPG (codepage) to ESRI Shapefile.

To export data:

#. Open the Properties page of Vector layer or PostGIS layer from which you want to export data;
#. Select :menuselection:`Vector layer --> Save as` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. Save file in chosen format to your device.

In "Format" field select data format you need: CSV, DXF, ESRI Shapefile, GeoJSON or Mapinfo File:

.. figure:: _static/formats_en_2.png
   :name: newformats_pic
   :align: center
   :width: 20cm    

   "Format" field

In "SRS" field (Spatial reference system) in addition to standart coordinate systems Longitude-Latitude (EPSG: 4326) amd Mercator (EPSG: 3857) you can select custom coordinate systems created earlier (how to add custom SRS see below): 

.. figure:: _static/coordinate_systems_en_2.png
   :name: coordinate_systems_pic
   :align: center
   :width: 20cm    

   "SRS" field

In "Encoding" field you can choose among UTF-8, Windows-1251, Windows-1252 encoding for your data:

.. figure:: _static/encodings_en_2.png
   :name: encodings_pic
   :align: center
   :width: 20cm    

   "Encoding" field

“FID field” is used for setting a field name to be added to a exported data where the object identifiers will be placed (the default is “ngw_id”).

Next you can chose which of the fields of the data to keep in the file. By default, all are selected. To remove a field, click on the cross by its name or untick it in the drop-down menu. To add a field again, tick it in the drop-down menu.

.. figure:: _static/export_fields_en.png
   :name: export_fields_pic
   :align: center
   :width: 20cm    

   Selcting fields

Output in ESRI Shapefile or MapInfo TAB results in a Zip archive with necessary files. For single-file formats (like GeoJSON or CSV) creation of Zip archive is optional.

All export options are available through HTTP API.

For example, this inquiry will get you data in CSV format, EPSG:4326, UTF-8 encoding, zipped:

https://demo.nextgis.com/api/resource/4077/export?format=csv&srs=4326&zipped=true&fid=ngw_id&encoding=UTF-8

Custom coordinate systems
---------------------------------

.. note::
    Custom SRS functionality is available on `Premium <http://nextgis.com/pricing/#premium/>`_ and while using the product `On-premise <https://nextgis.com/pricing/>`_. 

.. note::
    Only users with administrative privileges can add and modify SRS.

You can import a SRS from the catalog or create your own.

To **import SRS from the catalog** open "Control panel" in the main menu and press "Catalog" in "Spacial reference systems". Start typing the name of the SRS in the search bar. When you find the desired SRS in the search results, press the icon with the arrow next to it.

.. figure:: _static/new_srs_catalog_en.png
   :name: new_srs_catalog
   :align: center
   :width: 20cm    

   Search results in the catalog

You will be redirected to the import page. Here you can modify the name of SRS to be displayed in your WebGIS.

.. figure:: _static/new_srs_import_en.png
   :name: new_srs_import
   :align: center
   :width: 20cm    

   Adding SRS from catalog
   
.. figure:: _static/new_srs_import_save_en.png
   :name: new_srs_import_save
   :align: center
   :width: 20cm    

   Completing import

On the next page, press **Save** to complete the import.

To **create a new SRS** open "Control panel" in the main menu and press "Create" in "Spatial reference systems": 

.. figure:: _static/new_srs_eng_2.png
   :name: new_srs_pic
   :align: center
   :width: 20cm    

   Creation of a new SRS
   
You can give an SRS display name and enter its definition in OGC WKT format. You can also import definitions from common formats as PROJ, MapInfo and EPSG, after the import they will get converted to OGC WKT format. Then press "Create" button.

You can find a list of created and available SRS in the "List" of "Spatial reference systems" in "Control panel". In this list there are two SRS by default: «WGS 84 / Lon-lat (EPSG:4326)» and «WGS 84 / Pseudo-Mercator (EPSG:3857)», which can’t be removed or edited (except name):

.. figure:: _static/list_srs_eng_2.png
   :name: list_srs_pic
   :align: center
   :width: 20cm    

   A list of SRS
   
The added SRS can be used for various purposes:

1. To capture coordinates on Web maps. If you have set up additional SRS (one or several), you can now conveniently capture coordinates in this SRS from anywhere on the map:

.. figure:: _static/use_of_custom_srs1_eng.png
   :name: use_of_custom_srs1_pic
   :align: center
   :width: 20cm    

   The use of custom SRS
   
2. To export vector layers. All custom SRS are also available for data export (see above).

3. To extend API requests. Support for custom SRS is gradually added to NextGIS Web API too. For example, this request will return a feature in a required SRS:

    /api/resource/{id}/feature/{fid}?srs=990002

Custom SRS identifier (990002 in this example) can be known by editing a created SRS, for example:

    /srs/990002/edit

.. note:: 
	Geometry and attributes data export is supported. Features' descriptions, metadata and images can't be exported in the described way but can be requested using :ref:`NextGIS API <ngcom_ngapi>`.

.. note:: 
	You can also export data from Vector layers :ref:`with desktop app NextGIS QGIS <ngcom_ngqgis_connect_data_export>`.
