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

Hide Zoom In, Zoom Out Buttons, Home Buttons
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.control-pane.control-pane--top.control-pane--left {
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

Change Web map background color
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.ol-viewport {
		background-color: #000;
	}
	

