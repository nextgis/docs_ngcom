.. _ngcom_data_export:

How to export data
======================================

:ref:`Web GIS <ngcom_description>` allows to export data from :ref:`Vector layers <ngcom_vector_layer>` and :ref:`PostGIS layer <ngcom_postgis_layer>` in :term:`GeoJSON`, :term:`CSV`, ESRI Shape, AutoCAD DXF and Mapinfo TAB formats. To do this:

#. Open the Properties page of Vector layer or PostGIS layer from which you want to export data;
#. Select :menuselection:`Vector layer --> Save as` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. Save file in chosen format to your device.

.. note:: 
	Geometry and attributes data export is supported. Features' descriptions, metadata and images can't be exported in the described way but can be requested using :ref:`NextGIS API <ngcom_ngapi>`.

.. note:: 
	You can also export data from Vector layers :ref:`with desktop app NextGIS QGIS <ngcom_ngqgis_connect_data_export>`.
