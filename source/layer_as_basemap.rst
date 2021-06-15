.. sectionauthor:: Roman Gainullov <roman.gainullov@nextgis.com>

.. _ngcom_layer_as_basemap:

How to use any layer in your Web GIS as a basemap
==================================================

Any layer (style) created in Web GIS can be used as a source of a tile service and connected as a **basemap**.
To do this, you should:

1. Create the required `layer <https://docs.nextgis.com/docs_ngweb/source/layers.html>`_ and `style <https://docs.nextgis.com/docs_ngweb/source/mapstyles.html>`_ (both vector and raster). Inside will be a link **TMS service** - need it on; 
2. Enable `tile caching <https://docs.nextgis.com/docs_ngweb/source/mapstyles.html#tile-cache>`_ (to speed up work on a web map);
3. Create resource "Basemap" with unchecked "Use options from QMS" and the link of the above-created TMS layer.
