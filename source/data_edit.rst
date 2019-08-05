.. _ngcom_data_edit:

How to edit data
=====================================

:ref:`Web GIS <ngcom_description>` allows to edit objects, attributes and add descriptions and attachments (including photos) of separate features in :ref:`Vector layers <ngcom_vector_layer>` and :ref:`PostGIS layers <ngcom_postgis_layer>`.
	
.. note:: 
	You can use described functionality in Web GIS created in nextgis.com_ service on `Premium plan <http://nextgis.com/pricing/#premium/>`_

.. _ngcom_data_edit_objects:

Edit of object on the Web map
------------------------------

1. Open :ref:`Web map <ngcom_webmap_create>` and select the layer with an object you need to edit.
2. Open dropdown menu pressing "Layer" button (see :numref:`webmap_edit`) and tick the box next to "Editing" option.

.. figure:: _static/webgis_edit_objects_eng.png
   :name: webmap_edit
   :align: center
   :width: 16cm

   "Layer" menu.

3. Editing toolbar will appear on a Web map (see :numref:`webmap_edit_panel`):

.. figure:: _static/webgis_edit_objects_panel_eng.png
   :name: webmap_edit_panel
   :align: center
   :width: 16cm

   Editing toolbar.
   
Create a new object (point, line, polygon)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. On the editing toolbar press "Create features" button (see :numref:`webmap_create_objects`):

.. figure:: _static/webgis_create_new_objects_eng.png
   :name: webmap_create_objects
   :align: center
   :width: 16cm

   "Create features" button on the editing toolbar.

2. A blue circle will appear nearby a mouse pointer, with it you can add new objects. Click on the map, where you can create a new object. You can add several new objects one after another. While creating a line you need to indicate its start and end points by clicking on a map. While creating a polygon each new click on a map will indicate its new vertice, to finish a polygon you need to click on its start point. During vertices adding an adhesion will work.
3. To finish new objects creation press "Layer" button (see :numref:`webmap_edit`) and clear a tick box next to "Editing" option.
4. In opened dialog select "Save", if you want to save changes, select "Don't save", if you do not want to save them or "Cancel", if you want to stay in the editing mode:

.. figure:: _static/webgis_finish_editting_eng.png
   :name: webmap_finish_edit
   :align: center
   :width: 16cm

   Dialog window of finishing edits.
   
Edit of object's attributes
---------------------------

You can do it in 2 ways: 
1) using edit form in :ref:`Feature table <ngw_feature_table>` or
2) using edit form in Web map :ref:`web client <ngw_webmaps_client>` (if the relevant layer is added to :ref:`Web map <ngcom_webmap_create>`).

.. _ngcom_data_edit_table:

Edit using Feature table
-----------------------------------------------

#. Open the Properties page of :ref:`Vector layer <ngcom_vector_layer>` or :ref:`PostGIS layer <ngcom_postgis_layer>`;
#. Select :menuselection:`Vector layer --> Feature table` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog window select a feature you want to edit (if necessary search it by its attributes using :guilabel:`Search` bar) and press :guilabel:`Edit` button;
#. In the opened form edit feature attributes values in :guilabel:`Attributes` tab, add description and attachments in :guilabel:`Description` and :guilabel:`Attachments` tabs;
#. Press :guilabel:`Save` button. If attributes, description and attachments are saved successfully you'll be able to view them by selecting the feature in Feature table and pressing :guilabel:`Open` button.

.. _ngcom_data_edit_webmap:

Edit using Web map
---------------------------------------

#. Open :ref:`Web map <ngcom_webmap_create>` and switch on the visibility of the relevant layer;
#. Find a feature on the Web map (if necessary search it by its attributes using :guilabel:`Search` bar in the Toolbar or in :ref:`Feature table <ngw_feature_table>` which can be opened via :guilabel:`Layer` dropdown menu in the upper left corner of Web map web client. You can quickly find the selected feature on Web map using :guilabel:`Go to` button in Feature table);
#. Click on the feature with :ref:`identify tool <ngw_webmaps_client_tools>`. In the opened dialog window with feature properties press :guilabel:`Edit` button;
#. In the opened form edit feature attributes values in :guilabel:`Attributes` tab, add description and attachments in :guilabel:`Description` and :guilabel:`Attachments` tabs;
#. Press :guilabel:`Save` button. If attributes, description and attachments are saved successfully you'll be able to view them on Web map by clicking on the feature with identify tool, or by selecting the feature in Feature table and pressing :guilabel:`Open` button.

.. note:: 
	Updated attributes in PostGIS layers are saved directly to external :term:`PostGIS` database. Updated attributes in Vector layers, as well as descriptions and attachments in Vector layers and PostGIS layers are saved to your Web GIS.

.. note:: 
	You can also edit **geometries and attributes** of Vector layers features :ref:`with desktop app NextGIS QGIS <ngcom_ngqgis_connect_data_edit>`.

	Read more on data editing :ref:`here <ngw_attributes_edit>`.

How to delete data from Web GIS read :ref:`here <ngcom_resource_delete>`.
