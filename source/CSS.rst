.. _ngcom_CSS:

Как настроить внешний вид Веб ГИС
===================================

.. note:: 
	Эта функциональность доступна только для пользователей плана `Premium <http://nextgis.ru/nextgis-com/plans>`_ с правами администратора.

:ref:`Веб ГИС <ngcom_description>` поддерживает настройку своего внешнего вида. Внешний вид включает: логотипы, цвета шапки, фона, кнопок и других элементов.

#. Войдите в свою Веб ГИС с правами администратора, откройте раздел :guilabel:`Панель управления` и выберите пункт :guilabel:`Пользовательские стили CSS`. 
#. В открывшейся вкладке можно задать собственные стили CSS. Они будут использованы для оформления всех страниц вашей Веб ГИС. 


Примеры отдельных стилей
-------------------------

Изменить цвет шапки:
~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.header{background-color: #F44336; color: #fff;}

Убрать логотип NextGIS с карты:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.map-logo{display:none;}

.. note:: 
    На данный момент вы не сможете самостоятельно загрузить свой логотип, но его можем добавить мы. Для этого отправьте нам файл с логотипом на support@nextgis.com. Формат: PNG, высота: до 45 px, ширина - любая.

Расширенный пример настройки внешнего вида Веб ГИС:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

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
