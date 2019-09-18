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
    A road and operational entity should perform monitoring of roadbed condition.
    Objects of spatial data collecting in this case are roadbed damages.
    Geographical information in this example consists of such damages' coordinates. Attributive information includes
    damage type, its size, a description of its location within roadbed, a damage's photo.
    The NextGIS Collector was developed to simplify the procedure of such data collection and to give an instrument to do it.

However before a technical description of this system possibilityies we will look at main participants of data collection
for better understanding of system work principles.

There are two roles in a process of spatial data collection:

* An organizer of data collection.
* A participant of data collection.

.. figure:: _static/ngc-data-collection-team-clt_eng.png
   :name: Abstract roles in the process of data collection
   :align: center

   Abstract roles in the process of data collection
   
An *organizer of data collection* is a subject who organizes a process of data collection, gathers a team of participants, controls a process and verified the data. A group of people or a separate person could be an organizer. In the above-mentioned example a road and operational entity was an organizer.

Below there are some more examples of data collection organizers and their tasks.

.. figure:: _static/ngc-team-lead_eng.png
   :name: Examples of data collection organizers
   :align: center

   Examples of data collection organizers

A *participant of data collection* is a person who collect data in the field. His task is to describe properties of a real object in the field. Before active spreading of mobile devices people collected data using a paper notebook and writing implements. Nowadays mobile devices help to simplify this process and decrease a number of mistakes, so that we suppose, that every participant of data collection has a mobile device.

Principles of work with NextGIS Collector
-----------------------------------------

NextGIS Collector - is a technology created for simplifying of spatial data collection in the field.

NextGIS Collector allows an owner of created on nextgis.com Web GIS  to organize a team of a few people and to begin data collection using mobile devices.

NextGIS Collector is a technologic stack allowing to create a dataflow between an organizer and participants of data collection for effective supervision over the process and for an easement of data collection (a process is described in a previous section.

.. figure:: _static/ngc-data-collection-team-ngc_eng.png
   :name: A place of NextGIS Collector among participants of data collection process
   :align: center

   A place of NextGIS Collector among participants of data collection process

There are the next stages of data collection process in NextGIS Collector:

1. An organizer of data collection registers in nextgis.com_ and creates a Web GIS on `Premium plan <http://nextgis.com/pricing/#premium/>`_.
2. A team of data collection participants registers in nextgis.com_.
3. The organizer of data collection adds a team of data collection participants in his Web GIS and creates a project of data collection.
4. Data collection participants install `NextGIS Collector`_ app and join the project.
5. Data collection participants begin data collection. Data is sent to Web GIS automatically.

These stages of work with NextGIS Collector could be described schematically as follows:

.. raw:: html

   <iframe width="560" height="315" src="https://www.youtube.com/embed/fal_oUeGiLE"
    frameborder="0" allow="accelerometer;
    autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

To sum up, for beginning of data collection:

- A data collection organizer should have a Web GIS on `Premium plan <http://nextgis.com/pricing/#premium/>`_.
- Every data collection participant from a team should have a mobile device with Android OS.
- Every data collection participant from a team should register in nextgis.com_ and know his email and a password from registration.


Organizer of data collection: adding of team participants in Web GIS
----------------------------------------------------------------------

The first stage of work with the system presumes a registration of data collection participants in Web GIS of the data collection organizer. Data collection participants from a team should have a mobile device with Android OS. They need to install a mobile app `NextGIS Collector`_ on each of mobile devices - it will allow to update data and synchronize updates with Web GIS of the data collection organizer.

Besides, each data collection participant from a team should be registered in nextgis.com_. Team participant can do it himself or pass his login to the data collection organizer. A login in nextgis.com_ is an email used for a registration.

When each data collection participant from a team is registered in nextgis.com_, the data collection organizer will have a list of their emails.

To add team participants to Web GIS you need to do the following:

1. Open Web GIS as administrator.

.. important::
    Described below actions demand administrator privilegies

2. The home page of your Web GIS resources will be opened. Open a "Main menu" panel:

.. figure:: _static/ngc-stages-001_eng.png
   :name: ngc-stages-001
   :align: center

   Open main menu

3. In main menu select «Control panel»:

.. figure:: _static/ngc-stages-002_eng.png
   :name: ngc-stages-002
   :align: center

   Select «Control panel»

4. In «Settings» of the control panel select «Collector projects»:

.. figure:: _static/ngc-stages-003_eng.png
   :name: ngc-stages-003
   :align: center

   Select «Collector projects»

5. «NextGIS Collector settings» will be opened:

.. figure:: _static/ngc-stages-004_eng.png
   :name: ngc-stages-004
   :align: center

   «NextGIS Collector settings»

6. To add a team participant to Web GIS press "Create" button. In opened window "New collector"
fill up fields.

.. note::
    We advice to fill up a field "Description" with the name and the surname of a team participant in order to have a data about all 
    NextGIS Collector users in one place. You can always find the participant you need with a search tool in a table of Collector users, which is quite suitable when there are a lot of participants.

.. figure:: _static/ngc-stages-005_eng.png
   :name: ngc-stages-005
   :align: center

   Add a new data collection team participant

7. As a result of this stage all data collection team participants will be registered in your Web GIS.

.. figure:: _static/ngc-stages-006_eng.png
   :name: ngc-stages-006
   :align: center

   An example of a filled table of data collection team participants

Users with a registration in your Web GIS can get data collection projects from your Web GIS and begin data collection after they installed mobile app `NextGIS Collector`_ and successfully authorized there. However you can control over an access of different users in each separate project. It is described in details below.
