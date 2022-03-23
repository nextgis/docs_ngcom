.. sectionauthor:: Roman Gaunullov <roman.gainullov@nextgis.com>

.. _tracking:

How to enable the monitoring of moving objects (tracking)
========================================================

.. note::
    The number of available trackers depends on the current `plan <https://nextgis.com/pricing-base/>`_. For **Mini** - 1 tracker, for **Premium** - 5 trackers

Introduction
-------------

Monitoring of moving objects function is based on registration of changing user’s geolocation in time
and is necessary to record the history of its movement on the ground.
Tracking can be useful when you need to save a record of the route,
track and further analyze the trajectories of movement of objects in space.


How tracking works
-------------------

A track is a sequence of points in space over time to be displayed on a web map.

Monitoring process looks like this - a person launches tracking in the mobile application, follows the route, stops tracking in the end.
After that, recorded tracks are sent to the Web GIS server and are displayed on the web map (if it's configured).


Creating tracker groups
-----------------------

If you want see tracks on a web map, it’s needed to set up your Web GIS - create special resources groups:

1. Create a resource **Trackers group**. This is a folder which contains trackers (devices that sent data to Web GIS).

.. figure:: _static/group_trackers_en.png
   :name: Create a group of trackers
   :align: center
   
   Creating a group of trackers

2. Create a resource **Tracker** into a trackers group. For sync tracker with a mobile device, it’s needed enter ID (it can be found in NextGIS Mobile/Collector app’s settings (Mobile: Settings -> My tracks -> under Send location to server).

.. figure:: _static/create_tracker_en.png
   :name: Creating a tracker
   :align: center
   
   Creating a tracker

.. figure:: _static/tracker_settings_id_en.png
   :name: Tracker settings
   :align: center
   
   Tracker settings
   

Tracking in NextGIS Mobile, Collector and Tracker
-------------------------------------------------

For now you can track in mobile apps such as
`NextGIS Mobile <https://play.google.com/store/apps/details?id=com.nextgis.mobile>`_,
`NextGIS Collector <https://play.google.com/store/apps/details?id=com.nextgis.collector>`_ и NextGIS Tracker.
An Android smartphone is required for that.


**1. NextGIS Mobile**

It’s the complete mobile `GIS <https://nextgis.com/nextgis-mobile/>`_ that allows create, edit and share geodata both online and offline mode.

First of all you need to install an application and sign in.
Then activate the ‘Send location to server’ option in the ‘My tracks’ section of Settings.

.. figure:: _static/Mobile_settings_en.png
   :name: NextGIS Mobile Settings
   :align: center
   :scale: 70%
   :width: 425.0px
   :height: 685.0px
   
   NextGIS Mobile Settings

Here you can also see the unique identifier (ID) of the device, which must be specified in the tracker settings in Web GIS.

.. figure:: _static/Mobile_send_to_server_en.png
   :name: Send location to server. Device ID
   :align: center
   :scale: 70%
   :width: 425.0px
   :height: 685.0px
   
   Send location to server. Device ID

The process of recording a track is described in details in the `Tracks <https://docs.nextgis.com/docs_ngmobile/source/tracks.html/>`_ section of the documentation for NextGIS Mobile.
