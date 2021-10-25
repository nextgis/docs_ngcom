.. sectionauthor:: Maxim Dubinin <maxim.dubinin@nextgis.com>

How to change Web GIS domain
============================

.. note:: 
    This functionality is available only to nextgis.com `Premium users <http://nextgis.com/nextgis-com/plans>`_.

After you created a Web GIS you get a domain at nextgis.com, for example mywebgis.nextgis.com. Afterwards, you can change it to a domain of your organization, for example gis.mycompany.com.

Follow these steps. Typically this done by system administrator of your company who has access to DNS records.

**Step 1. Add DNS record 1 to get HTTPS certificates**

.. code-block:: bash

   _acme-challenge.gis.example.com. CNAME _acme-challenge.nimbo.nextgis.net.
   
change gis.example.com to the needed domain under the domain of your organization, change example.nextgis.com to your Web GIS address at *.nextgis.com

**Check 1**

Your system administrator needs to check that changes took effect. Use `Dig <https://toolbox.googleapps.com/apps/dig/#CNAME/>`_. Enter: _acme-challenge.gis.example.com. Give some time for DNS changes to take an effect.

Expected answer: CNAME (TTL and TARGET).

**Step 2. Внести в DNS Запись 2 для перенаправления запросов к Веб ГИС**

.. code-block:: bash

   gis.example.com. CNAME example.nextgis.com.

change gis.example.com to the needed domain under the domain of your organization, change example.nextgis.com to your Web GIS address at *.nextgis.com

**Check 2**

Your system administrator needs to check that changes took effect. Use `Dig <https://toolbox.googleapps.com/apps/dig/#CNAME/>`_. Enter: gis.example.com. Give some time for DNS changes to take an effect.

Expected answer: CNAME (TTL and TARGET).

When all changes are entered and confirmed, let us know at support@nextgis.com to finalize.
