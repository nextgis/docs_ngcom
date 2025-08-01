Store, manage and publish your spatial data
============================================

.. note:: Availability: Cloud SaaS (all editions), On premise (all editions), Open Source

NextGIS Web is a data-centric server GIS, allowing you to store, manage and publish spatial data in a flexible and effective way. In this step-by-step tutorial you will learn how to convert your GIS files into shareable Web Maps, tile and OGC services, as well as to create and manage data directly on the server. Register a free cloud account and try it right away!

:download:`Download tutorial data <https://nextgis.com/tutorials/store_manage_publish_geospatial_data.zip>` (source: `Wrocław Spatial Information System <https://geoportal.wroclaw.pl/>`_)

Basic

1. Create Account and Web GIS
2. Create Resource group
3. Upload vector layer and style
4. Upload raster layer
5. Publish Web Map

Advanced

6. Add external WMS layer to Web Map
7. Add basemaps
8. Create vector layer inside Web GIS
9. Edit vector layer on Web Map, add file attachments
10. Publish OGC API — Features service
11. Behind the scenes


1 Create free account and Web GIS
----------------------------------

Go to `my.nextgis.com`, press the **Create Account** button and sign up using your email address. 

After registration your account page would appear. Select the **Web GIS** menu on the left, come up with a name (ngw-quickstart.nextgis.com in this example) and select the nearest Data center location (DE Falkenstein in this example). Then press **Create Web GIS**.

.. figure::

When the creation process is complete, the contents of the page will change. Direct link to your new Web GIS will appear.

.. figure::

2 Access your Web GIS and create resource group
------------------------------------------------

Click on the Web GIS link or type it into your browser.

You'll see the main interface of your Web GIS.

.. figure::

Web GIS has a structure similar to the way files are stored in your computer — in a tree. This tree contains folders (groups), layers, Web Maps, connections to services and databases etc, they are all called *resources*. Let’s create our first resource, a folder or *resource group* named Wroclaw. For that, press the **Create resource** button. 

.. figure::

.. tip:: If you don’t see the “Create resource” button, you should login. Press the “Sign in” button in the top right corner and then press the “Sign in with NextGIS ID” button.

.. figure::

Window appears showing all available options of what could you create in the current context. Select **Resource group**.

.. figure::

The resource creation window consists of several tabs, in this case we need to set only the name “Wroclaw” as the “Resource” tab.

.. figure::

Press **Create** and you'll be redirected to the page of the new resource.

.. figure::

The URL in your browser is the path to the resource, and the numbers at the end of the URL are resource ID. 

Wroclaw group is a child for the Main resource group folder where we created it.

Now you can upload data to this folder.

3 Upload and publish vector layer and style
-------------------------------------------

`Download the sample data <https://nextgis.com/tutorials/store_manage_publish_geospatial_data.zip>`_ and unzip the archive.

Inside the Wroclaw folder, press the “Create resource” button again and select the “Vector layer” type of resource.

.. figure::

You'll see the interface for resource creation with several tabs. 

.. figure::

In the default tab **Vector layer** press **Select a dataset** and select the file called *bicycle_roads.gpkg* from the tutorial dataset (or drag the file to the field).




