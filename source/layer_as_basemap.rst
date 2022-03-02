.. sectionauthor:: Roman Gainullov <roman.gainullov@nextgis.com>

.. _ngcom_layer_as_basemap:

How to use any layer in your Web GIS as a basemap
==================================================

Any layer (style) created in Web GIS can be used as a source of a tile service and connected as a **basemap**.
To do this, you should:

1. Create the required `layer <https://docs.nextgis.com/docs_ngweb/source/layers.html>`_ (vector or raster) and a `style <https://docs.nextgis.com/docs_ngweb/source/mapstyles.html>`_ for it. In the style settings there is a link marked **TMS service** - you will need it for step 3;
2. Enable `caching <https://docs.nextgis.com/docs_ngweb/source/mapstyles.html#tile-cache>`_ (to speed up Web Map processing, for `Premium plan <https://nextgis.com/pricing-base/>`_ only);
3. Create "Basemap" resource with unchecked "Use options from QMS" and the URL of the above-created TMS layer.
