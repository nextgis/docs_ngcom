.. _ngcom_CSS:

How to change the look of your Web GIS
========================================

.. note:: 
    This functionality is available only to nextgis.com `Premium users <http://nextgis.com/nextgis-com/plans>`_ for users with administrative privileges.

You can customize the look of your Web GIS, including logos, backgrounds, header and buttons colors.

Upload a logo
-------------
You can change the upper-left logo (present on all pages), you can't change the Web map logo (lower right).

To upload a logo choose :guilabel:`Custom logo` on control panel (see item 1 in :numref:`admin_index_pic`) and in opened window upload a file in PNG format with height up to 45 px, width up to 200 px. Then press "Save".



Customize design with CSS
-------------------------------------------

You can modify the look of NextGIS Web using CSS.

From the main menu (see :numref:`ngweb_main_page_administrative_interface_pic`) open the Control Panel (see :numref:`ngweb_main_page_main_menu_pic`).

In the Control Panel (see :numref:`ngweb_control_panel`) select **Custom CSS** in the Settings section.
Here you can enter your own :term:`CSS` rules. They will be used throughout your Web GIS on all its pages. 

Custom CSS examples
-------------------------------------------

Change main Web GIS color 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Affects header, symbols in the header, buttons, field contours, links highlighted on hover etc.

.. code-block:: css

	:root {
  	--primary: red
	}

Change main font color 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Affects menu, name and parameters of displayed resource group etc.

.. code-block:: css

	:root {
  	--text-base: #ff6600
	}

Change additional font color
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Affects paths for the displayed resource, parameters etc.

.. code-block:: css

	:root {
  	--text-secondary: rgb(40 200 40 / .8)
	}
	
