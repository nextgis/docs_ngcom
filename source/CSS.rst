.. _ngcom_CSS:

How to change the look of your Web GIS
========================================

.. note:: 
    This functionality is available only to nextgis.com `Premium users <http://nextgis.ru/nextgis-com/plans>`_ for users with administrative privileges.

You can customize the look of your Web GIS, including logos, backgrounds, header and buttons colors etc with a little bit of CSS magic:

#. Sign in as the user with administrative privileges and open Control panel, then select Custom CSS. 
#. Enter your own CSS rules. They will be used throughout your Web GIS on all its pages.


Custom CSS examples
--------------------

Change header color:
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

    .header{background-color: #F44336; color: #fff;}

Remove NextGIS logo from Web map:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

    .map-logo{display:none;}

.. note:: 
    At the moment you can't upload a new logo by yourself, but we can do it for you. If you want us to do it simply send your logo to support@nextgis.com.

Advanced example
~~~~~~~~~~~~~~~~~~

This example shows how to change the look of pretty much all changeable elements of your Web GIS. 
You can try these examples as is or change it to your liking. You can also see them in action `here <http://nastya.nextgis.com>`_.

.. code-block:: bash

	/* Base background */

	body{
	  background-color: #fff;
	  background-image:url("https://nextgis.ru/img/hypnotize_transparent.png");
	}

	/* Header text and background color */

	.header{
	  background-color: #F44336;
	  color: #fff;
	}

	/* Separator color between logo and title */

	.header__title-logo{
	  border-right: 1px solid rgba(255,255,255,.48) !important;
	}

	/* User info color in header */

	.user-avatar__label{
	  background-color: #fff !important;
	  color: #F44336 !important;
	}

	.user-avatar .user-avatar__icon{
	  color: rgba(255,255,255,.82) !important;
	}

	/* Primary button */

	.dijitButton--primary{
	  background-color: #fff !important;
	  color:#f44336 !important;
	  font-weight: bold !important;
	  border: 2px solid #f44336 !important;
	}

	.dijitButton--primary:hover{
	  background-color: #f44336 !important;
	  color: #fff !important;
	}

	/* Default button */

	.dijitButton--default{
	  background-color: #fff !important;
	  color:#999 !important;
	  font-weight: bold !important;
	  border: 2px solid #999 !important;
	}

	.dijitButton--default:hover{
	  background-color: #999 !important;
	  color: #fff !important;
	}

	/* Tabs color */

	.dijitTabContainerTop-tabs .dijitTabChecked{
	  border-top-color: #f44336 !important;
	}

	/* Left navigation panel on the map */

	.navigation-menu{
	  background-color: #fff !important;
	  border-right: 1px solid rgba(0,0,0,.12) !important;
	  color: #000 !important;
	}