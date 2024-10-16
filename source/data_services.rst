.. _ngcom_data_services:

Как публиковать данные с помощью стандартных протоколов
=======================================================

:ref:`Веб ГИС <ngcom_description>` позволяет публиковать загруженные и подключенные в нее геоданные по стандартным протоколам :term:`WFS` и :term:`WMS`. Веб ГИС в этом случае выступает как сервер WFS(WFS-T)/сервер WMS.

.. _ngcom_wms_service:

Сервис WMS
----------

#. Откройте :ref:`Группу ресурсов <ngcom_resources_group>`, в которой вы хотите создать сервис (на главной странице Веб ГИС по умолчанию открыта Основная группа ресурсов);
#. Нажмите кнопку **Создать ресурс** и выберите во всплывающем окне тип ресурса "Сервис WMS";
#. В открывшемся окне заполните поле :guilabel:`Наименование` на вкладке :guilabel:`Ресурс`;
#. Перейдите на вкладку :guilabel:`Сервис WMS` и выберите те ресурсы (:ref:`Стили <ngcom_styles>` или :ref:`Слои WMS <ngcom_wms_layer>`), которые вы хотите опубликовать по протоколу WMS. Для каждого ресурса нужно указать уникальный ключ;
#. Нажмите кнопку **Создать**. Если Сервис WMS создался успешно, то информация о нем появится в блоке :guilabel:`Дочерние ресурсы` соответствующей Группы ресурсов.

Больше информации о создании Сервиса WMS - :ref:`здесь <ngw_create_wms_service>`.

.. _ngcom_wfs_service:

Сервис WFS
----------

С помощью сервиса WFS можно публиковать векторные данные и редактировать их через :ref:`настольные <ngcom_ngqgis_connect_data_edit>` приложения.

#. Откройте :ref:`Группу ресурсов <ngcom_resources_group>`, в которой вы хотите создать сервис (на главной странице Веб ГИС по умолчанию открыта Основная группа ресурсов);
#. Нажмите кнопку **Создать ресурс** и выберите во всплывающем окне тип ресурса "Сервис WFS";
#. В открывшемся окне заполните поле :guilabel:`Наименование` на вкладке :guilabel:`Ресурс`;
#. Перейдите на вкладку :guilabel:`Сервис WFS` и выберите те ресурсы (:ref:`Векторные слои <ngcom_vector_layer>` или :ref:`Слои PostGIS <ngcom_postgis_layer>`), которые вы хотите опубликовать по протоколу WFS. Для каждого ресурса нужно указать уникальный ключ;
#. Нажмите кнопку **Создать**. Если Сервис WFS создался успешно, то информация о нем появится в блоке :guilabel:`Дочерние ресурсы` соответствующей Группы ресурсов.
	
Ссылка на сервис WFS не предназначена для просмотра в браузере. Её нужно скопировать и вставить в клиент, поддерживающий протокол WFS, например `NextGIS QGIS <http://nextgis.ru/nextgis-qgis/>`_.

По умолчанию при добавлении в клиент сервис WFS отдаёт 1000 объектов. Чтобы увеличить это количество, измените значение поля :guilabel:`Число возвращаемых объектов по умолчанию` на вкладке :guilabel:`Сервис WFS`.

Быстро создавать сервис WFS на основе слоя можно с помощью `NextGIS Connect <https://docs.nextgis.ru/docs_ngcom/source/ngqgis_connect.html#ngcom-ngqgis-connect-services>`_.

Больше информации о создании Сервиса WFS - :ref:`здесь <ngw_wfs_service>`.
