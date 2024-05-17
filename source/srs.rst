.. _ngcom_srs:

Custom coordinate systems
=============================

.. note::
    Custom SRS functionality is available on `Premium <http://nextgis.com/pricing/#premium/>`_ and while using the product `On-premise <https://nextgis.com/pricing/>`_. 

.. note::
    Only users with administrative privileges can add and modify SRS.

You can import Spacial Reference Systems from the catalog or create your own.

.. _ngcom_srs_from_catalog:

Add SRS from catalog
--------------------------------------------

To import SRS from the catalog open “Control panel” in the main menu and press **“Catalog”** in “Spacial reference systems”.  You will be redirected to the catalog page. Start typing the name of the SRS in the search bar. When you find the desired SRS in the search results, press the icon with the arrow next to it. 

.. figure:: _static/new_srs_catalog_en.png
   :name: new_srs_catalog
   :align: center
   :width: 20cm    

   Search results in the catalog
   
You will be redirected to the import page. Here you can modify the name of SRS to be displayed in your Web GIS.

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

.. _ngcom_srs_from_descr:

Create SRS using definition
--------------------------------------------

To create a new SRS open “Control panel” in the main menu and press **“Create”** in “Spacial reference systems”: 

.. figure:: _static/new_srs_eng_2.png
   :name: new_srs_pic
   :align: center
   :width: 20cm    

   Creation of a new SRS
   
You can give an SRS display name and enter its definition in OGC WKT format.  You can also import definitions from common formats as PROJ, MapInfo and EPSG, after the import they will get converted to OGC WKT format.  Then press **“Create”** .

.. _ngcom_srs_additional:

Additional coordinate systems
-------------------------------------------------

To view the list of all added SRS, go to the "Control panel" and select **"List"** in the "Spacial reference systems" section. In this list there are two default SRS: «WGS 84 / Lon-lat (EPSG:4326)» and «WGS 84 / Pseudo-Mercator (EPSG:3857)», which can’t be removed or edited (apart from their names):

.. figure:: _static/list_srs_eng_2.png
   :name: list_srs_pic
   :align: center
   :width: 20cm    

   A list of SRS
   
The added SRS can be used for various purposes:

1. To capture coordinates on Web maps.  If you have set up additional SRS (one or several), you can now conveniently capture coordinates in this SRS by clicking anywhere on the map.

.. figure:: _static/use_of_custom_srs1_eng.png
   :name: use_of_custom_srs1_pic
   :align: center
   :width: 20cm    

   The use of custom SRS
   
2. To export vector layers.  All custom SRS are also available for `data export <https://docs.nextgis.com/docs_ngcom/source/data_export.html>`_.

3. To extend API requests. Support for custom SRS is gradually added to NextGIS Web API too.  For example, this request will return a feature in a required SRS:

/api/resource/{id}/feature/{fid}?srs=990002

To find the custom SRS identifier (990002 in this example) open the edit page for the created SRS, for example:

/srs/990002/edit

.. _ngcom_srs_external_db:

Custom SRS support for external PostGIS Databases
-------------------------------------------------

A common case for Web GIS users is adding an external PostGIS/PostgreSQL database while `creating a PosGIS layer <https://docs.nextgis.com/docs_ngcom/source/data_connect.html#external-postgis-databases>`_. These layers often get incorrectly displayed 
in the Web GIS. It happens when the spacial reference system has incorrect definition in the external 
database. To make the Web GIS-DB complex work efficiently, here's what you need:

1. External database must have a table of SRS descriptions spacial_ref_sys.
2. In the geometry column (usually called "geom") a SRS must be assigned.
3. The ID of the assigned SRS must be included in  spacial_ref_sys.
4. Data in the external DB must actually be in that coordinate system, a.i. the SRS definition must correspond to the data.

If all the above requirements are met, then whatever SRS you use in your database, layers created in Web GIS will be reprojected "on the fly" and displayed correctly along any other data you have in your Web GIS.

To check if everything works correctly use `PostGIS diagnostics <https://docs.nextgis.com/docs_ngweb/source/layers.html#postgis-diagnostics>`_.
