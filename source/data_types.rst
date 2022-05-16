.. _ngcom_data_types:

Which data formats and protocols are supported in Web GIS
==========================================================

:ref:`Web GIS <ngcom_description>` allows to :ref:`upload <ngcom_data_upload>` and store geodata from local sources in the following spatial data formats:

* Raster - :term:`GeoTIFF` (with 3 or 4 bands, RGB or RGBA);
* Vector - :term:`ESRI Shape`, :term:`GeoJSON` and :term:`GeoPackage`. 

Use :ref:`NextGIS Connect <ngcom_ngqgis_connect_data_upload>` if you need to upload data in other formats.

Web GIS also allows to :ref:`connect <ngcom_data_connect>` geodata from the following external sources: 

* :term:`TMS` services;
* :term:`PostGIS` databases;
* :term:`WMS` services (WMS server should support :term:`coordinate system` EPSG:3857).

You can add images (including photos) to vector geodata from local and external sources. Image files should be in JPEG or PNG format. Read more `here <https://docs.nextgis.com/docs_ngweb/source/layers_settings.html#ngw-add-photos/>`_.

You can also publish uploaded or connected to your Web GIS geodata using :term:`WFS` (with feature update support) and :term:`WMS` protocols. Read more :ref:`here <ngcom_data_services>`.

Vector geodata from local and external sources can be exported as :term:`GeoJSON` and :term:`CSV` files. Read more :ref:`here <ngcom_data_export>`.
