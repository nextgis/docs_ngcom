.. sectionauthor:: Yulia Grigorenko <yulia.grigorenko@nextgis.com>

Teams
======

.. _ngcom_team_view:

Team info
----------



.. _ngcom_ream_management:

Team management
---------------

.. warning::
   This functionality is only available for `Premium <http://nextgis.com/nextgis-com/plans>`_ users.
   
   
According to nextgis.com plans, the Premium account holder has an opportunity to give access to Premium-functions of `NextGIS QGIS <https://nextgis.com/nextgis-qgis#pro>`_, `Mobile <https://nextgis.com/nextgis-mobile#pro>`_ и `Formbuilder <https://nextgis.com/nextgis-formbuilder#pro>`_ to 4 more users who have a NextGIS ID.

Team management allows adding any NextGIS user by username to your team. Team management is available through your personal account at https://my.nextgis.com/teammanage in the Team section (see :numref:`Team_on_panel`).

.. figure:: _static/Team_on_panel_en.png
   :name: Team_on_panel
   :align: center
   :width: 7cm    

   The Team section of the Personal Account
   
By default, the team includes the owner of the Premium subscription (see :numref:`First_administrator`). The owner can add team members by clicking the **Add** button and finding them by using their NextGIS ID username (see :numref:`teamlist_users`). Team members must already be registered on my.nextgis.com. The username can be seen in the `profile <https://my.nextgis.com/>`_. Team member will have Free plan under subscription, it's normal, he/she will also have access Premium-functionality.

If the user has forgotten his username and cannot login, he can `restore <https://docs.nextgis.com/docs_ngcom/source/faq_webgis.html#access-recovery-and-passwords>`_ access.

.. figure:: _static/First_administrator_en.png
   :name: First_administrator
   :align: center
   :width: 16cm    

   Default view (owner only)
   
   
.. figure:: _static/teamlist_users.png
   :name: teamlist_users
   :align: center
   :width: 14cm    

   Adding user to the team
   
Each added team member will appear in the list (see :numref:`all_users`). At any moment, a team member can be removed and/or replaced by another if the limit of the team is reached (see :numref:`limit_users`).

.. figure:: _static/all_users_en.png
   :name: all_users
   :align: center
   :width: 16cm    

   Users added to the team
   
   
.. figure:: _static/limit_users.png
   :name: limit_users
   :align: center
   :width: 12cm    

   Message about exceeding the limit of members in the team


.. _ngcom_auth_id_webgis:

Allow team members to access Web GIS using NextGIS ID
------------------------------------------------------

Users added to the `team <https://docs.nextgis.com/docs_ngcom/source/create.html#ngcom-team-management>`_ do not automatically become users of the Web GIS. To get access to the Web GIS, the user must log in to it.
By default a new Web GIS user has no permissions. Set up permissions for your team before their first login.
It can be done in one of two ways:

* The best way is to set up permissions for a `user group <https://docs.nextgis.com/docs_ngweb/source/users.html#create-new-user-group>`_ with the option "New users" enabled. Users will be included in this group upon their first login to the Web GIS.
* An alternative way is to set up permissions for the principal "Authenticated".
