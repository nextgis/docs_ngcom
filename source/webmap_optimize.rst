.. _ngcom_webmap_optimize:

How to optimize web map performance
====================================

Web-maps show data rendered by the server. The more of this data you have the more server resources needed to render and more time it takes. There are several things to think about and technologies to use to improve your map experience.

**Don't show everything at once**

This is a universal recommendation. Does your user need to see everything once he/she opens the Web map for the first time? Typically this is not informative. On the broad scales (smaller zooms) it is advisable to show limited amount of data to get started.

**Scale range**

Set a range of `scale levels <https://docs.nextgis.com/docs_ngweb/source/webmaps_admin.html#admin-webmap-create-layers>`_ for displaying data on a web map.
This will allow you not to request data outside this range and as a result won't show excess data where it is not essential.

**Сaching**

Set up `caching <https://docs.nextgis.com/docs_ngweb/source/layers.html#tms-layer>`_ for your layer styles.
In this case, already rendered data will not be re-requested.
