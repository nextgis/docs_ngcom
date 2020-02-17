.. _ngcom_CSS:

Как настроить внешний вид Веб ГИС
=================================

.. note:: 
	Эта функциональность доступна только для пользователей плана `Premium <http://nextgis.ru/nextgis-com/plans>`_ с правами администратора.

:ref:`Веб ГИС <ngcom_description>` поддерживает настройку своего внешнего вида. Внешний вид включает: логотипы, цвета шапки, фона, кнопок и других элементов.

Загрузка логотипа
-----------------

Вы можете поставить свой логотип вместо логотипа NextGIS в верхнем левом углу. Изменить/убрать логотип NextGIS на самой Веб карте - нельзя.

Чтобы загрузить логотип, в панели управления (см. :numref:`ngweb_main_page_administrative_interface_pic`, п.1) необходимо выбрать пункт :guilabel:`Логотип` и в открывшемся окне загрузить файл в формате PNG, высотой до 45 px, ширина до 200 px. После этого требуется нажать на кнопку "Сохранить".


Изменение стиля элементов интерфейса
------------------------------------

#. Войдите в свою Веб ГИС с правами администратора, откройте раздел :guilabel:`Панель управления` и выберите пункт :guilabel:`Пользовательские стили CSS`. 
#. В открывшейся вкладке можно задать собственные стили CSS. Они будут использованы для оформления всех страниц вашей Веб ГИС. 


Изменить цвет шапки
~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.header{background-color: #F44336; color: #fff;}

Скрыть пункт Войти
~~~~~~~~~~~~~~~~~~

Пункт будет скрыт с Веб-карт и со всех остальных страниц.

.. code-block:: bash

	.header-nav {
		display: none;
	}

	.dynamic-panel__title {
		display: none;
	}

Скрыть кнопки Поделиться, Печать с Веб-карт
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.navigation-menu__item[data-item-value=sharePanel],
        .navigation-menu__item[data-item-value=printMapPanel]{
                display: none;
        }

Скрыть заголовок окна идентификации объекта на веб-карте
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	div.ngwPopup__content div div.dijitAlignTop,
	div.ngwPopup__features span.ngwWebmapToolIdentify-controller {
	    display: none;
	}

Скрыть иконки у слоёв на веб-карте
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

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

Расширенный пример настройки внешнего вида Веб ГИС
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Этот пример показывает, как настроить большинство изменяемых элементов внешнего вида вашей Веб ГИС. 
Вы можете использовать фрагменты приведенных ниже стилей в своей Веб ГИС как есть или с нужными вам изменениями. Увидеть эти стили в действии можно `тут <http://nastya.nextgis.com>`_.

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
