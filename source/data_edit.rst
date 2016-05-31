.. _ngcom_data_edit:

How to edit data
=====================================

:ref:`Web GIS <ngcom_description>` allows to edit attributes and add descriptions and images (including photos) of separate objects in :ref:`Vector layers <ngcom_vector_layer>` and :ref:`PostGIS layers <ngcom_postgis_layer>`.

You can do it in 2 ways: 
1) using edit form in :ref:`Feature table <ngw_feature_table>` or
2) using edit form in Web map :ref:`web client <ngw_webmaps_client>` (if the relevant layer is added to :ref:`Web map <ngcom_webmap_create>`).

.. _ngcom_data_edit_table:

Edit using Feature table
-----------------------------------------------

#. Open the Properties page of :ref:`Vector layer <ngcom_vector_layer>` or :ref:`PostGIS layer <ngcom_postgis_layer>`;
#. Select :menuselection:`Vector layer --> Feature table` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog window select an object you want to edit (if necessary search it by its attributes using :guilabel:`Search` bar) and press :guilabel:`Edit` button;
#. In the opened form edit object attributes values in :guilabel:`Attributes` tab, add description and images of the object in :guilabel:`Description` and :guilabel:`Attachments` tabs;
#. Press :guilabel:`Save` button. If attributes, description and images are saved successfully you'll be able to view them by selecting the object in Feature table and pressing :guilabel:`Open` button.

.. _ngcom_data_edit_webmap:

Edit using Web map
---------------------------------------

#. Open :ref:`Web map <ngcom_webmap_create>` and switch on the visibility of the relevant layer;
#. Find an object on the Web map (if necessary search it by its attributes using :guilabel:`Search` bar in the Toolbar or in :ref:`Feature table <ngw_feature_table>` which can be opened via :guilabel:`Layer` dropdown menu in the upper left corner of Web map web client. You can quickly find the selected object on Web map using :guilabel:`Go to` button in Feature table);
#. Click on the object with :ref:`identify tool <ngw_webmaps_client_tools>`. In the opened dialog window with object properties press :guilabel:`Edit` button;
#. In the opened form edit object attributes values in :guilabel:`Attributes` tab, add description and images of the object in :guilabel:`Description` and :guilabel:`Attachments` tabs;
#. Press :guilabel:`Save` button. If attributes, description and images are saved successfully you'll be able to view them on Web map by clicking on the object with identify tool, or by selecting the object in Feature table and pressing :guilabel:`Open` button.

.. warning:: 
	Web GIS supports only JPEG and PNG files upload in :guilabel:`Attachments` tab. GIF format is not supported.

.. note:: 
	Updated attributes of objects from PostGIS layers are saved directly to external :term:`PostGIS` database. Attributes of objects from Vector layers, descriptions and images of objects from Vector layers and PostGIS layers are saved in your Web GIS.

Read more on data editing :ref:`here <ngw_attributes_edit>`.

How to delete data from Web GIS read :ref:`here <ngcom_resource_delete>`.
