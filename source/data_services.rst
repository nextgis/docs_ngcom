.. _ngcom_data_services:

How to publish data using standard protocols
=========================================================

:ref:`Web GIS <ngcom_description>` allows to publish uploaded and connected geodata using standard :term:`WFS` и :term:`WMS` protocols. In this case Web GIS acts like WFS(WFS-T)/WMS server.

.. _ngcom_wms_service:

WMS service
-------------------------

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a service (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> WMS service` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab;
#. Go to :guilabel:`WMS service` tab and select those resources (:ref:`Styles <ngcom_styles>` or :ref:`WMS layers <ngcom_wms_layer>`) which you want to publish using WMS protocol. **You need to specify a keyname for each resource**;
#. Press :guilabel:`Create` button. If WMS service is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. note:: 
	Web GIS supports connection of resources published using WMS protocol via :term:`TMS` service. Read more about it :ref:`here <ngw_create_tms_service>`.

Read more about WMS service creation :ref:`here <ngw_create_wms_service>`.

.. _ngcom_wfs_service:

WFS service
-----------------------

#. Open :ref:`Resource group <ngcom_resources_group>` where you want to create a service (by default from the main page of Web GIS you can access Main resource group);
#. Select :menuselection:`Create resource --> WFS service` on the right side of Web GIS :ref:`admin console <ngw_admin_interface>`;
#. In the opened dialog fill in the field :guilabel:`Display name` in :guilabel:`Resource` tab;
#. Go to :guilabel:`WFS service` tab and select those resources (:ref:`Vector layers <ngcom_vector_layer>` or :ref:`PostGIS layers <ngcom_postgis_layer>`) which you want to publish using WMS protocol. **You need to specify a keyname for each resource**;
#. Press :guilabel:`Create` button. If WFS service is created successfully you'll see its name in :guilabel:`Child resources` pane of the relevant Resource group.

.. note::
        Link that appears after WFS service is created is not meant to be opened with a regular browser. You will need to copy and paste it in the WFS-capable client, such as for example `NextGIS QGIS <http://nextgis.com/nextgis-qgis/>`_.

.. note:: 
	By default WFS service publishes 1000 objects. To increase this number change :guilabel:`Default count of returned features` value in :guilabel:`WFS service` tab.

.. note:: 
	Web GIS supports editing of Vector layers with WFS service. Among other things it allows to edit vector geodata in Web GIS using :ref:`mobile <ngcom_ngmobile_connect>` and :ref:`desktop <ngcom_ngqgis_connect>` applications.

Read more about WFS service creation :ref:`here <ngw_wfs_service>`.
