.. _ngcom_webmap_optimize:

How to optimize Web Map performance
====================================

Web Maps show data rendered by the server. The more of this data you have, the more server resources are needed to render and the more time it takes. There are several techniques you can use to improve your map experience.

**Don't show everything at once**

This is a universal recommendation. Does your user need to see everything after opening the Web Map for the first time? Typically, it is not informative. On broad scales (smaller zooms) it is advisable to show limited amount of data as a start.

**Scale range**

Set a range of `scale levels <https://docs.nextgis.com/docs_ngweb/source/webmaps_admin.html?highlight=scale#admin-webmap-create-layers>`_ for displaying data on a Web Map.
This will allow you to avoid requesting data outside this range and showing excess data where it is not essential.

**Сaching**

Set up `caching <https://docs.nextgis.com/docs_ngweb/source/layers.html#tms-layer>`_ for your layer styles.
In this case, already rendered data will not be re-requested. Note that, while technically it's possible to turn on caching for rasters, this is not recommended.

**Services**

Today's interactive map is often a complex system that might include connections to external services, such as basemaps, WMS, TMS services and more. If you use them on your map, overall speed on it will depend on their performance. Remove them if you don't need them or at least turn them off not to show by default. 
**Select Image as an adapter**

In the Web Map settings, go to the Layers tab and `select <https://docs.nextgis.com/docs_ngweb/source/webmaps_admin.html?highlight=adapter#admin-webmap-create-layers>`_ **Image** as an adapter to allow for faster data processing. We do not recommend using Tiles if it isn't necessary. It slows down the entire Web GIS if large amounts of data are used.

**Raster styles instead of QGIS raster style**
If your map shows big rasters you can add few percents of performance by switching from QGIS raster styles to regular raster styles. Go to your raster, add a raster style (if possible), add them back to your Web map replacing QGIS ones.
