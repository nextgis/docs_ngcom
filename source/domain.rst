.. sectionauthor:: Maxim Dubinin <maxim.dubinin@nextgis.com>

How to change Web GIS domain
============================

.. note:: 
	This functionality is available only to nextgis.com `Premium users <http://nextgis.com/nextgis-com/plans>`_.

By creating your Web GIS you get a domain at nextgis.com, for example mywebgis.nextgis.com. You can change it to a domain of your organization, for example gis.myorg.com.

To do that, you need to add an A records in your DNS settings, pointing to 95.213.223.211. This is usually preformed by a system administrator of your company who has access to company's domain settings.

.. note::
        Make sure that the changes made effect by using `Dig <https://toolbox.googleapps.com/apps/dig/#A/>`_. ANSWER section should point to IP 95.213.223.211.

When it's done, let us know at support@nextgis.com, we will finish the configuration.
