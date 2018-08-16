.. sectionauthor:: Maxim Dubinin <maxim.dubinin@nextgis.com>

How to change the homepage address
==================================

.. note:: 
    This functionality is available only to nextgis.com `Premium users <http://nextgis.com/nextgis-com/plans>`_ for users with administrative privileges.

By default the starting page of your Web GIS is the main resource page (``/resource/0``). You can change which page will be opened first. If this is a Web map, it might look like this: ``/resource/644/display``.

#. Sign in as the user with administrative privileges and open Control panel, then select :guilabel:`Home path`. 
#. Enter path to the resource page that should be opened first when you Web GIS is accessed.

After making this setting visiting ``http://yourwebgis.nextgis.com`` will open not the main resource contents page, but the page you've set up. To access main resource content page after this setting you will need to go directly to: ``http://yourwebgis.nextgis.com/resource/0``.
