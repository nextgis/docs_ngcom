.. _collector:

.. _nextgis.com: http://nextgis.com/
.. _NextGIS Collector: https://play.google.com/store/apps/details?id=com.nextgis.collector

How to begin data collection in your Web GIS
==============================================

.. note:: 
	You can use described functionality in Web GIS created in nextgis.com_ service on `Premium plan <http://nextgis.com/pricing/#premium/>`_
  
Introduction
------------

You need to collect spatial data to get geographic and attributive information about objects located in some area. Geographic information is described by a set of coordinates. 
Attributive information is a description of object's features.

.. note::
    As an **example** we can describe a task of monitoring of road infrastructure objects' condition.
    A road and operational entity should perform periodic control of roadbed condition monitoring.
    Objects of spatial data collecting in this case are roadbed damages.
    Geographical information in this example consists of such damages' coordinates. Attributive information includes
    damage type, its size, a description of its location within roadbed, a damage's photo.
    The NextGIS Collector was developed to simplify the procedure of such data collection and to give an instrument to do it.

However before a technical description of this system possibilityies we will look at main participants of data collection
for better understanding of system work principles.

There are two roles in a process of spatial data collection:

* An organizer of data collection.
* A participant of data collection.
