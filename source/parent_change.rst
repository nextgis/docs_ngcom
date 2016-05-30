.. _ngcom_parent_change:

How to transfer resources inside Web GIS
=========================================

:ref:`Web GIS <ngcom_description>` resourses (data layers, connections, services, groups) can be transferred from one :ref:`Resource group <ngcom_resources_group>` to another after their creation. To do that:

#. Open the Properties page of a resource you want to transfer;
#. Select :menuselection:`Action --> Update` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog window in the field :guilabel:`Parent` in :guilabel:`Resource` tab select Resource group you want to transfer your resource to;
#. Press :guilabel:`Save` button. If a resource is transferred successfully its name will appear in the new Resource group and disappear from the previous Resource group.

In the same way you can transfer :ref:`Styles <ngcom_styles>` between parent resources (:ref:`Vector layers <ngcom_vector_layer>`, :ref:`Raster layers <ngcom_raster_layer>`, :ref:`PostGIS layers <ngcom_postgis_layer>`).
