.. sectionauthor:: Roman Gainullov <roman.gainullov@nextgis.com>

How to enable caching
=====================

Caching is used to speed up data rendering and `optimize <https://docs.nextgis.com/docs_ngcom/source/webmap_optimize.html>`_ the performance of web maps.
It can be applied to `vector <https://docs.nextgis.com/docs_ngweb/source/mapstyles.html>`_ and `raster <https://docs.nextgis.com/docs_ngweb/source/layers.html#raster-style-qgis>`_ layer styles, as well as `WMS <https://docs.nextgis.com/docs_ngweb/source/layers.html#wms-layer>`_ and `TMS <https://docs.nextgis.com/docs_ngweb/source/layers.html#tms-layer>`_ layers.

To enable caching, you need:

* Go to the "Tile Cache" tab in the corresponding resource
* Activate the "Enabled" checkbox
* In accordance with a specific task, set the settings for the maximum zoom level of caching, TTL, and if necessary, flush the cache and allow the use of cached tiles (tiles) when requesting pictures (image)

More information about tile caching is `here <https://docs.nextgis.com/docs_ngweb/source/mapstyles.html#tile-cache>`_.
