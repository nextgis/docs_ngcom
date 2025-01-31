.. _ngcom_help:

Toubleshooting
===============

Styles compatibility between QGIS and NextGIS Web
---------------------------------------------------

Since original QGIS libraries do render layers in this extension, most styling and rendering options work well. However, there is a big difference between QGIS and NextGIS Web in how they compose layers. QGIS renders layers together and places labels on top of all layers. NextGIS Web, on the other hand, renders layers one-by-one (or even tile-by-tile) and stacks them together on a client side. That's why NextGIS Web rendering of QGIS styles may differ in the following ways:

* Blending options don't work;
* Labels from diffenent layers may overlap;
* Expression-driven SVG markers don't work;
* Masking doesn't work at all, as it part of a project, not of a layer.

To check what version of QGIS is currently used for rendering in the Web GIS, see the `System information <https://docs.nextgis.com/docs_ngweb/source/infowebgis.html#ngw-system-info>`_ section of the `Control panel <https://docs.nextgis.com/docs_ngweb/source/admin_interface.html#ngw-control-panel>`_.

How to get help or send a bug report
---------------------------------------

If you haven't found an answer to your question in this tutorial try `full documentation <http://docs.nextgis.com/docs_ngweb/source/toc.html>`_.

You can send bug-reports to info@nextgis.com. 

Direct support and more functionality are available under Premium plan (`details <http://nextgis.com/nextgis-com/plans>`_).

Informal support and discussions regarding the service are available in the public channel `NextGIS <https://t.me/nextgis_talks>`_
