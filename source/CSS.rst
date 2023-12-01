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

	.ngw-pyramid-layout-header{
  background-color: blue !important;
}

.. code-block:: bash

.ngw-pyramid-layout-header > .text {
  color: gold !important;
}

Скрыть пункт Войти
~~~~~~~~~~~~~~~~~~

Пункт будет скрыт с Веб-карт и со всех остальных страниц.

.. code-block:: bash

	.header-nav {
		display: none;
	}

Скрыть кнопки Поделиться, Печать с Веб-карт
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.navigation-menu__item[data-item-value=sharePanel],
        .navigation-menu__item[data-item-value=printMapPanel]{
                display: none;
        }
	
	
Скрыть кнопки Увеличения и Уменьшения зума, кнопки Домой
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.control-pane.control-pane--top.control-pane--left {
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

Сделать фон веб карты другим цветом
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

	.ol-viewport {
		background-color: #000;
	}
	

