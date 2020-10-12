.. _ngcom_faq:

Problem Solving (Q&A)
================================

In this section you can find answers to the most frequently asked questions about using Web GIS.

.. _ngcom_change_passwords_webgis:

Access recovery and passwords
-------------------------------

I forgot my account password (NextGIS ID). What to do?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
To recover a password from *NextGIS ID*, follow these steps:

1. Go to `my.nextgis.com <https://my.nextgis.com//>`_
2. Select "Forgot password?"

.. figure:: _static/forgot_pass_ngid_en.png
   :name: forgot_pass_ngid_en
   :align: center
   :width: 16cm    

   Password recovery NextGIS ID



I forgot the password from the user *administrator* of my Web GIS and can not log in. What to do?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
If you have forgotten the password from the administrator of your Web GIS, restore it using the following instructions:

1. Go to `my.nextgis.com <https://my.nextgis.com//>`_
2. Sign in with NextGIS ID
3. Go to Web GIS Settings
4. Click Change Web GIS Password
5. Enter and confirm a new password

Wait for the confirmation message by email. Then you can log in to your Web GIS **administrator** user and specified password.

.. figure:: _static/Web_GIS_change_password_eng.png
   :name: Web_GIS_change_password_eng
   :align: center
   :width: 16cm    

   Changing Web GIS Administrator Password
   
   
   
I forgot the password for Web GIS user created by the administrator
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
If you have forgotten the password for any user who is not a Web GIS administrator, follow these steps: 

1. Go to `my.nextgis.com <https://my.nextgis.com//>`_
2. Log in with NextGIS ID
3. Log in to your Web GIS http://username.nextgis.com/ as user **administrator**
4. Open the main menu in the upper right corner of the interface
5. Go to Control Panel
6. Open the user list
7. Change the password in the user settings (см. :numref:`change_password_user_en`)

.. figure:: _static/change_password_user_en.png
   :name: change_password_user_en
   :align: center
   :width: 16cm    

   Changing Web GIS User Password


.. _ngcom_2_accounts_nextgis:

Two accounts NextGIS. Background
-------------------------------

NextGIS is growing fast and it has several services and products that use authorization, Web GIS is one of them.

As a rule, a typical NextGIS platform user needs 2 accounts: a global and a local one. But, for some specific tasks, it is possible that one of them will be enough.

.. _ngcom_global_account:

Global account
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Most services require a **global** account. This is the usual account that acts uniformly almost everywhere. It gives access to all services, except for **Web GIS**.

This account is created by registration at http://my.nextgis.com. Email or login provided during registration can be used to sign in with services.

Thus, if the user does not need to *enter* the Web GIS, global account is enough and a local one is not needed.

.. _ngcom_local_account:

Local account (your Web GIS account)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Historically, NextGIS' main product is Web GIS. Unlike other services that use central database of users, **each** Web GIS has its **own account system** that operates **locally** within that Web GIS.

For example, each Web GIS has *administrator* user. Its locality lies in the fact that it is impossible to enter a Web GIS with the *administrator* account of another Web GIS. In other words, other services and applications do not know anything about this user, unless it is indicated which Web GIS he is from.

These accounts are created in the Web GIS control panel by a user with appropriate authority (usually administrator). They are not tied to any E-mails.


.. _ngcom_how_to_use:

Which account to use and where
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**NextGIS Web (Web GIS)**

* Creation of Web GIS itself - global account.
* Any actions requiring authorization - a local account created in this Web GIS.

**NextGIS Collector**

* Login and Data Collection - global account.

**NextGIS Mobile**

* Unlocking additional functions of the application - global account.
* Connecting layers from Web GIS (need to unlock first) - a local account of this Web GIS.

**NextGIS QGIS**

* Unlocking additional functions of the application - global account.
* Connecting layers from Web GIS through NextGIS Connect - a local account of this Web GIS.

**NextGIS Formbuilder**

* Unlocking additional functions of the application - global account.
* Sending/receiving forms to/from Web GIS (need to unlock first) - a local account of this Web GIS.

**NextGIS Data**

* Receiving ordered data - global account.

**NextGIS Toolbox**

* Running tools - global account.

**NextGIS QMS**

* Creating services - global account.

**NextGIS Geoservices**

* Getting tiles (OSM /vector, raster/), requests for information on the blocks and areas - global account.
