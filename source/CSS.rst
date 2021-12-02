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

Custom CSS examples
-------------------

#. Sign in as the user with administrative privileges and open Control panel, then select Custom CSS. 
#. Enter your own CSS rules. They will be used throughout your Web GIS on all its pages.

Change header color
~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

    .header{background-color: #F44336; color: #fff;}

Hide sign in link
~~~~~~~~~~~~~~~~~

This will hide sign in text from Web maps and all other pages. You'll have to type sign in link manually to sign in.

.. code-block:: bash

	.header-nav {
		display: none;
	}

Hide Print, Share buttons from Web maps
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.navigation-menu__item[data-item-value=sharePanel],
        .navigation-menu__item[data-item-value=printMapPanel]{
                display: none;
        }

Hide header of the Web map feature identification popup window
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	div.ngwPopup__content div div.dijitAlignTop,
	div.ngwPopup__features span.ngwWebmapToolIdentify-controller {
	    display: none;
	}

Hide layer icons on Web map
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.dijitIcon.dijitTreeIcon.dijitLeaf {
    	    display: none;
	}
	.dijitIcon.dijitTreeIcon.dijitFolderOpened  {
    	    display: none;
	}

	.dijitIcon.dijitTreeIcon.dijitFolderClosed {
	    display: none;
	}

Advanced example
~~~~~~~~~~~~~~~~

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
