.. _ngcom_embed_webmap:

How to embed a Web Map on your website
======================================

All Web Maps created on nextgis.com can be easily embedded into your website.

.. note:: 
	This functionality is available only to nextgis.com `Mini and Premium users <https://nextgis.com/pricing-base/>`_.

For this:

* Open Web Map
* Click on the "Share" tab on the left sidebar
* Customize your desired map width and height
* Copy the code
* Paste this code on your site

.. figure:: _static/embed_webmap.png
   :name: svg_qgis_style
   :align: center
   :width: 20cm

   Options for embedding a Web Map on a site
   
   
.. figure:: _static/webmap_on_site.png
   :name: svg_qgis_style
   :align: center
   :width: 20cm

   Embedded Web Map example
   
   
There are also additional options:

* Link to the main map - to go from the site to the map page in Web GIS
* Generate events - for integration and programmatic interaction with the iframe
* Preview - to preview the embedded Web Map before publishing it

To embed a Web Map with all the panels available remove ``/tiny`` part from the Web GIS link in iframe code. This will allow users, for instance, to enable and disable particular layers.

If you are a developer check out the `code.nextgis.com <https://code.nextgis.com/>`_ library suite
and the `NGW API <https://docs.nextgis.com/docs_ngweb_dev/doc/toc.html>`_.
