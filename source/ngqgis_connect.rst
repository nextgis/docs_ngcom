.. _ngcom_ngqgis_connect:

Как управлять данными с помощью настольного приложения QGIS
===================================================================

Загружать, редактировать и совершать другие операции с геоданными в :ref:`Веб ГИС <ngcom_description>` можно не только через административный :ref:`веб-интерфейс <ngw_admin_interface>`, но и с помощью настольного приложения QGIS. 

.. note::
   Также вы можете использовать `NextGIS QGIS <http://nextgis.ru/nextgis-qgis/>`_.

Для удобного управления вашей Веб ГИС мы создали модуль расширения `NextGIS Connect <https://plugins.qgis.org/plugins/nextgis_connect/>`_. Обновить модуль можно через меню **Модули** -> **Управление модулями** -> **NextGIS Connect**.

NextGIS Connect позволяет обмениваться данными с множеством Веб ГИС из настольного приложения. Для этого необходимо создать к ним соответствующие подключения.


.. _ngcom_ngqgis_connect_connection:

Подключение к Веб ГИС
---------------------

После успешной установки модуля в правой части экрана появится панель :guilabel:`NextGIS Connect`.

Для начала работы **создайте подключение** к своей Веб ГИС:

* Откройте диалог **Настройки** (шестренка) на панели управления NextGIS Connect;

.. figure:: _static/NGConnection_main_ru.png
   :name: NGconnection_main_pic
   :align: center
   :width: 20cm
   
   Вызов настроек из панели NextGIS Connect

* Нажмите кнопку **Новое**;

* В открывшемся диалоговом окне заполните поля **URL** (веб-адрес вашей Веб ГИС, например, - https://examples.nextgis.com) и **Название** (будет отображаться в списке доступных подключений). 

.. figure:: _static/create_connection_ru.png
   :name: NGconnection_create_pic
   :align: center
   :width: 20cm
   
   Создание нового подключения

.. note:: 
   Создавать и удалять ресурсы Веб ГИС может ее владелец и пользователи, добавленные в `команду <https://docs.nextgis.ru/docs_ngcom/source/create.html#ngcom-team-management>`_.

* Чтобы получить возможность создавать и удалять ресурсы, в разделе *Аутентификация* в выпадающем меню выберите конфигурацию аутентификации (в списке отражается название соединения и имя пользователя, а также тип аутентификации) или создайте новую.

Для того, чтобы добавить новую конфигурацию, нажмите кнопку с зеленым плюсом. Откроется диалоговое окно «Аутентификация».

.. figure:: _static/auth_config_create_ru.png
   :align: center
   :width: 12cm
   :name: auth_config_create_pic
   :alt: Добавление конфигурации аутентификации
   
   Добавление конфигурации аутентификации

1. Введите произвольное название конфигурации в поле *Имя*;
2. Выберите Basic-аутентификацию в выпадающем меню ниже;
3. Заполните поля *Пользователь* и *Пароль* данными вашего NextGIS ID;
4. Нажмите **Сохранить**.

Убедитесь, что выбрана нужная конфигурация. Если хотите проверить правильность введенных данных, нажмите "Проверка подключения". 

* Затем нажмите **Сохранить** в окне "Создание подключения". 

   
* Нажмите кнопку :guilabel:`Ок` и закройте диалоговое окно `Настройки`. В окне модуля появится дерево ресурсов вашей Веб ГИС.


   
.. figure:: _static/NGConnection_result_ru.png
   :name: NGconnection_result_pic
   :align: center
   :width: 20cm
   
   Дерево ресурсов подключенной Веб ГИС в окне NextGIS Connect


.. _ngcom_ngqgis_connect_data_upload:

Создание и загрузка данных
------------------------------------------------

Модуль NextGIS Connect позволяет быстро загружать в Веб ГИС растровые и векторные данные, а также целиком проекты QGIS. Это позволит вам легко опубликовать в интернете свои карты и геоданные.

.. _vector_data:

Загрузка векторных данных
~~~~~~~~~~~~~~~~~~~~~~~~~

.. important:: 
   Вы можете избежать :ref:`ограничений по форматам данных <ngcom_vector_layer>` при загрузке векторных данных в Веб ГИС через NextGIS Connect, применив опции "Переименовывать запрещенные поля" и "Исправлять некорректные геометрии" в диалоге :guilabel:`Настройки`.

* Создайте в QGIS "с нуля" или добавьте из файлов векторные слои :term:`ESRI Shape`, :term:`GeoJSON` или :term:`CSV`. Настройте стили их отображения;
* Выберите в дереве ресурсов Веб ГИС в окне модуля NextGIS Connect :ref:`Группу ресурсов <ngcom_resources_group>`, в которую вы хотите загрузить данные (или создайте её с помощью кнопки "Создать новую группу ресурсов");
* Выберите в панели слоев QGIS векторный слой, который вы хотите загрузить в Веб ГИС;
* Нажмите кнопку **Добавить в Веб ГИС** на панели инструментов модуля и кликните **Загрузить выбранное** в меню или нажмите **NextGIS Connect --> Загрузить выбранное** в контекстном меню слоя;
* Если данные загрузились успешно, то в соответствующей Группе ресурсов появится новый :ref:`Векторный слой <ngcom_data_upload>`, внутри которого будет создан :ref:`Стиль QGIS <ngcom_styles>` с заданными настройками стиля.

При загрузке слоя **с несколькими стилями** в Веб ГИС, они загружаются со своими именами. Если название стиля - default (или "по умолчанию"), используется название слоя. 



.. _raster_data:

Загрузка растровых данных
~~~~~~~~~~~~~~~~~~~~~~~~~

* Добавьте в QGIS из файлов растровые слои :term:`GeoTIFF`;
* Выберите в дереве ресурсов Веб ГИС в окне модуля NextGIS Connect Группу ресурсов, в которую вы хотите загрузить данные;
* Выберите в панели слоев QGIS растровый слой, который вы хотите загрузить в Веб ГИС;
* Нажмите кнопку **Добавить в Веб ГИС** на панели инструментов модуля и кликните **Загрузить выбранное** в меню или нажмите **NextGIS Connect --> Загрузить выбранное** в контекстном меню слоя;
* Если данные загрузились успешно, то в соответствующей Группе ресурсов появится новый :ref:`Растровый слой <ngcom_data_upload>`, внутри которого будет создан :ref:`Растровый стиль <ngcom_styles>` с настройками стиля по умолчанию.


.. _basemaps:

Загрузка базовых карт (подложек)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Добавьте в QGIS базовую карту (подложку);
* Выберите в дереве ресурсов Веб ГИС в окне модуля NextGIS Connect Группу ресурсов, в которую вы хотите добавить подложку;
* Выберите в панели слоев QGIS подложку, которую вы хотите загрузить в Веб ГИС;
* Нажмите кнопку **Добавить в Веб ГИС** на панели инструментов модуля и кликните **Загрузить выбранное** в меню или нажмите **NextGIS Connect --> Загрузить выбранное** в контекстном меню слоя;
* Если подложка загрузилась успешно, то она появится в соответствующей Группе ресурсов.

Для работы с подложками ваша Веб ГИС должна быть на плане `Мини или Премиум <https://nextgis.ru/pricing-base/>`_, в противном случае вы не сможете импортировать их в Веб ГИС.


.. _qgis_project:

Загрузка проекта QGIS целиком
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Соберите в QGIS проект из растровых и векторных слоев. Настройте их стили отображения, иерархию, группировку, видимость. Настройте охват карты;
* Выберите в дереве ресурсов Веб ГИС в окне модуля NextGIS Connect Группу ресурсов, в которую вы хотите загрузить проект;
* Нажмите кнопку **Загрузить всё** на панели инструментов модуля;

.. figure:: _static/NGConnect_import_menu_ru_2.png
   :name: NGConnect_import_menu_pic
   :align: center
   :width: 20cm
   
   Импорт текущего проекта
   
* В открывшемся диалоговом окне укажите название новой Группы ресурсов, в которую будет загружен проект;

.. figure:: _static/NGConnect_import_name_ru_2.png
   :name: NGConnect_import_name_pic
   :align: center
   :width: 20cm
   
   Указание имени импортируемого проекта

* Если проект загрузился успешно, то в соответствующей Группе ресурсов появится новая Группа ресурсов с заданным названием, внутри которой будут находиться: 
1) все Растровые и Векторные слои, для которых доступна операция *Добавить в Веб ГИС*, а также их Стили;
2) автоматически созданная :ref:`Веб-карта <ngcom_webmap_create>` с заданным охватом, на которую будут добавлены все импортированные слои с учетом их группировки, иерархии и видимости в панели слоёв QGIS.

.. note:: 
	Быстро перейти к Веб-карте можно, нажав кнопку **Открыть карту в браузере** на панели инструментов модуля или выбрав соответствующую команду в контекстном меню Веб-карты.

.. figure:: _static/NGConnect_import_view_ru_2.png
   :name: NGConnect_import_view_pic
   :align: center
   :width: 20cm
   
   Открытие импортированного проекта в Веб ГИС через контекстное меню

При добавлении группы ресурсов, которая содержит слои **с несколькими стилями**, будут добавлены все стили и выбран в качестве текущего либо одноименный слою, либо первый по алфавиту. Диалог с выбором показан не будет.



.. _ngcom_ngqgis_connect_services:

Создание Сервисов: WFS, WMS, OGC API - Features
---------------------------

Модуль NextGIS Connect позволяет быстро публиковать Векторные слои в Веб ГИС по стандартным протоколам :term:`WFS`, :term:`WMS` и OGC API - Features. 

.. _create_wfs_service:

Создание сервиса WFS
~~~~~~~~~~~~~~~~~~~~~

Для этого в модуле доступна операция быстрого создания :ref:`Сервиса WFS <ngcom_wfs_service>`:

* В настольном приложении (QGIS) в дереве ресурсов Веб ГИС модуля NextGIS Connect выберите **Векторный слой**, который вы хотите опубликовать по протоколу WFS;

.. figure:: _static/NGConnect_wfs_select_ru.png
   :name: NGConnect_wfs_select_pic
   :align: center
   :width: 20cm
   
   Выбор слоя

* Выберите пункт **Создать сервис WFS** в контекстном меню слоя;

.. figure:: _static/NGConnect_wfs_context_ru.png
   :name: NGConnect_wfs_context_pic
   :align: center
   :width: 20cm
   
   Контекстное меню слоя
   
* В открывшемся диалоговом окне укажите число объектов слоя, которое должен публиковать Сервис WFS;

.. figure:: _static/NGConnect_wfs_number_ru.png
   :name: NGConnect_wfs_number_pic
   :align: center
   :width: 20cm
   
   Число публикуемых объектов слоя

* Если Сервис WFS создался успешно, то в соответствующей Группе ресурсов появится новый Сервис WFS, в который уже подключен ваш Векторный слой.


.. figure:: _static/NGConnect_wfs_result_ru.png
   :name: NGConnect_wfs_result_pic
   :align: center
   :width: 20cm
   
   Созданный сервис WFS в дереве ресурсов
   
.. note:: 
	Отредактировать настройки созданного таким образом Сервиса WFS (включая его название, публикуемые слои и их настройки) можно через веб-интерфейс Веб ГИС.

.. _create_ogc_api_feat_service:

Создание сервиса OGC API - Features
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Для этого в модуле доступна операция быстрого создания Сервиса OGC API - Features:

* В настольном приложении (QGIS) в дереве ресурсов Веб ГИС модуля NextGIS Connect выберите **Векторный слой**, который вы хотите опубликовать по протоколу OGC API - Features;

.. figure:: _static/NGConnect_ogc_select_ru.png
   :name: NGConnect_wfs_select_pic
   :align: center
   :width: 20cm
   
   Выбор слоя

* Выберите пункт **Создать сервис OGC API - Features** в контекстном меню слоя;

.. figure:: _static/NGConnect_ogc_context_ru.png
   :name: NGConnect_wfs_context_pic
   :align: center
   :width: 20cm
   
   Контекстное меню слоя
   
* В открывшемся диалоговом окне укажите число объектов слоя, которое должен публиковать Сервис OGC API - Features;

.. figure:: _static/NGConnect_ogc_number_ru.png
   :name: NGConnect_wfs_number_pic
   :align: center
   :width: 20cm
   
   Число публикуемых объектов слоя

* Если Сервис OGC API - Features создался успешно, то в соответствующей Группе ресурсов появится новый Сервис OGC API - Features, в который уже подключен ваш Векторный слой.


.. figure:: _static/NGConnect_ogc_result_ru.png
   :name: NGConnect_wfs_result_pic
   :align: center
   :width: 20cm
   
   Созданный сервис OGC API - Features в дереве ресурсов


.. _create_wms_service:

Создание сервиса WMS
~~~~~~~~~~~~~~~~~~~~~

Для этого в модуле доступна операция быстрого создания :ref:`Сервиса WMS <ngcom_wms_service>`:

* В настольном приложении (QGIS) в дереве ресурсов Веб ГИС модуля NextGIS Connect выберите **Векторный слой**, который вы хотите опубликовать по протоколу WMS;


.. figure:: _static/NGConnect_wfs_select_ru.png
   :name: NGConnect_wfs_select_pic
   :align: center
   :width: 20cm
   
   Выбор слоя
   
* Выберите пункт **Создать WMS сервис** в контекстном меню слоя;

.. figure:: _static/NGConnect_wms_context_ru.png
   :name: NGConnect_wms_context_pic
   :align: center
   :width: 20cm
   
   Контекстное меню слоя
   
* В открывшемся диалоговом выберите стиль слоя для публикация Сервиса WMS;


.. figure:: _static/NGConnect_wms_style_ru.png
   :name: NGConnect_wms_style_pic
   :align: center
   :width: 20cm
   
   Выбор стиля для публикации Сервиса WMS
   
* Если Сервис WMS создался успешно, то в соответствующей Группе ресурсов появится новый Сервис WMS, в который уже подключен ваш Векторный слой.

.. figure:: _static/NGConnect_wms_result_ru.png
   :name: NGConnect_wms_result_pic
   :align: center
   :width: 20cm
   
   Созданный Сервис WMS в дереве ресурсов


.. _ngcom_ngqgis_connect_data_edit:

Редактирование данных
---------------------

Модуль NextGIS Connect позволяет быстро редактировать геометрии и атрибуты объектов в Векторных слоях Веб ГИС. Функция применима только для форматов векторных данных, используемых в QGIS.

.. warning:: 
	Одновременно редактировать слой напрямую может один пользователь.

#. Импортируйте слой из Веб ГИС в QGIS, выделив его в окне NextGIS Connect и нажав "Добавить в QGIS".
#. Перейдите в режим редактирования в контекстном меню слоя или через панель инструментов.
#. Внесите необходимые изменения.
#. Выйдите из режима редактирования. В появившемся диалоговом окне сохраните изменения.
#. Синхронизация произойдет автоматически.

Если со времени последней синхронизации в облаке были сделаны изменения, дальнейшая синхронизация станет невозможна. Нажмите на значок синхронизации рядом со слоем, в открывшемся окне "Статус слоя" в выпадающем меню выберите **Сброс слоя**. Обратите внимание: если  сброс произойдет при наличии локальных изменений, они будут утеряны. 

.. figure:: _static/ngc_check_sync_ru.png
   :align: center
   :alt: Всплывающая подсказка с информацией о синхронизации
   :width: 16cm

   Значок синхронизации слоя

.. figure:: _static/ngc_layer_status_ru.png
   :align: center
   :width: 14cm

   Диалоговое окно статуса слоя. Для сброса слоя нужно нажать на стрелочку вниз рядом с кнопкой "Синхронизация" и выбрать "Сброс слоя"

.. _ngcom_connect_data_edit_wfs:

Редактирование через WFS
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Также редактирование векторного слоя возможно при использовании стандартного протокола :term:`WFS` (с поддержкой редактирования):

* :ref:`Опубликуйте по протоколу WFS <ngcom_ngqgis_connect_wfs_service>` Векторный слой, объекты которого вы хотите отредактировать (как это сделать, см выше);
* Выберите в дереве ресурсов Веб ГИС в окне модуля NextGIS Connect соответствующий WFS сервис;
* Нажмите кнопку **Добавить в QGIS** на панели инструментов модуля или выберите пункт **Добавить в QGIS** в контекстном меню сервиса;

.. figure:: _static/NGConnect_edit_add_ru.png
   :name: NGConnect_edit_add_pic
   :align: center
   :width: 20cm
   
   Добавление слоя в QGIS через панель NextGIS Connect
   
* Если операция прошла успешно, то на панели слоев QGIS появится новая группа слоев WFS, опубликованных с помощью добавленного WFS сервиса;
* Включите режим редактирования (иконка карандаша) и отредактируйте геометрии и атрибуты объектов в добавленном слое WFS с помощью :ref:`стандартных инструментов QGIS <ngqgis_editing>`;

.. figure:: _static/NGConnect_edit_process_ru.png
   :name: NGConnect_edit_process_pic
   :align: center
   :width: 20cm
   
   Редактирование объектов

* Нажмите ещё раз кнопку "Режим редактирования" и подтвердите сохранение изменений.

.. figure:: _static/NGConnect_edit_save_ru.png
   :name: NGConnect_edit_save_pic
   :align: center
   :width: 20cm
   
   Сохранение изменений векторного слоя
   
* Если редактирование объектов прошло успешно, то соответствующие изменения сразу же будут отображены в Веб ГИС в :ref:`Таблице объектов <ngw_feature_table>` и :ref:`веб-клиенте <ngw_webmaps_client>` Веб-карты.



.. _ngcom_ngqgis_connect_data_overwrite:

Обновление данных
-----------------

С помощью NextGIS Connect можно обновить целиком содержимое уже существующего векторного слоя Веб ГИС, заменив входящие в него объекты, но сохранив его стили, псевдонимы атрибутов и другие настройки.

.. warning:: 
   Все данные целевого слоя, включая вложения (фото, документы), будут очищены. Если вам нужно их сохранить - используйте WFS

Для обновления (замены) данных слоя:

* Выберите на панели слоёв QGIS векторный слой, объекты которого вы хотите отправить в векторный слой Веб ГИС;
* Выберите в дереве ресурсов Веб ГИС в окне модуля NextGIS Connect векторный слой, объекты которого вы хотите заменить;
* Щелкните правой кнопкой мыши по выбранному векторному слою в окне NextGIS Connect и выберите **Перезаписать выбранный слой**.

Идентификатор ресурса слоя при этом останется неизменным. Операция подразумевает, что слой-источник и целевой слой имеют одинаковую структуру атрибутов.

   
.. figure:: _static/NGconnect_vector_overwrite_ru_2.png
   :name: connect_vector_overwrite
   :align: center
   :width: 20cm
   
   Перезапись выбранного слоя через контекстное меню

Объекты слоя также можно `редактировать <https://docs.nextgis.ru/docs_ngcom/source/ngqgis_connect.html#ngcom-ngqgis-connect-data-edit>`_ напрямую или через WFS.

.. _ngcom_ngqgis_connect_style_overwrite:

Обновление стиля
-----------------

Стиль можно заменить или добавить к существующему.

Для того, чтобы внести изменения и заменить старый стиль на новый:

* Добавьте слой в QGIS через Connect.
* Измените стиль вашего слоя (цвет, толщина линий и так далее).
* Выделите слой в панели слоев QGIS, а в окне Connect выделите **стиль** нужного ресурса.
* В панели инструментов Connect нажмите кнопку "Добавить в Веб ГИС" и выберите в меню "Обновить стиль слоя". (Или в панели слоев QGIS на редактируемом слое - Правый клик > NextGIS Connect > Обновить стиль слоя)

.. figure:: _static/connect_replace_style_ru.png
   :name: connect_replace_style_pic
   :align: center
   :width: 20cm

   Обновление стиля


.. figure:: _static/connect_replace_style_context_ru.png
   :name: connect_replace_style_context_pic
   :align: center
   :width: 20cm

   Обновление стиля через контекстное меню слоя

После данных операций модуль NextGIS Connect удалит старый стиль вашего слоя из веб ГИС и загрузит новый, оставив при этом нетронутыми данные и вложения.

Также можно добавить изменённый стиль, сохранив старый. Для этого после внесения изменений сделайте следующее:

* Выделите в окне Connect **слой**.
* В панели слоев QGIS в контекстном меню выберите NextGIS Connect > Добавить новый стиль к слою.

.. figure:: _static/connect_add_style_ru.png
   :name: connect_add_style_pic
   :align: center
   :width: 20cm

   Добавление стиля

.. _ngcom_ngqgis_connect_style_copy:

Копирование стиля из Веб ГИС
-----------------------------

Модуль имеет возможность копирования QML-стиля слоя в Веб ГИС для применения его к локальному слою в QGIS.

Разверните нужный вам слой в дереве Connect и кликните правой кнопкой мыши по QML-стилю слоя. Выберите «Копировать стиль» и стандартным способом через контекстное меню слоя на панели слоёв QGIS вставьте его.

.. figure:: _static/connect_copy_style_ru.png
   :name: connect_copy_style_pic
   :align: center
   :width: 8cm

   Копирование стиля

.. figure:: _static/connect_paste_style_ru.png
   :name: connect_paste_style_pic
   :align: center
   :width: 20cm

   Вставить стиль

.. figure:: _static/connect_result_style_ru.png
   :name: connect_result_style_pic
   :align: center
   :width: 20cm

   Скопированный стиль в проекте QGIS

.. _ngcom_ngqgis_connect_data_export:

Экспорт данных
--------------

Модуль NextGIS Connect позволяет быстро экспортировать векторные данные из Веб ГИС в QGIS для их последующей обработки, анализа, выгрузки и иных операций.

Для этого в модуле доступна операция быстрого создания векторных слоев GeoJSON в QGIS с использованием данных Векторных слоев Веб ГИС:

* Выберите в дереве ресурсов Веб ГИС в окне модуля NextGIS Connect Векторный слой, который вы хотите экспортировать в QGIS;
* Нажмите кнопку **Добавить в QGIS** на панели инструментов модуля или выберите пункт **Добавить в QGIS** в контекстном меню слоя;

.. figure:: _static/NGConnect_export_select_ru.png
   :name: NGConnect_export_select_pic
   :align: center
   :width: 20cm
   
   Экспорт векторного слоя из Веб ГИС


* В случае, если слой имеет несколько стилей QGIS, сценарий зависит от того, что выделено для загрузки в окне Connect:

1. При выборе в дереве Connect **слоя с несколькими стилями**, они подгрузятся все, но будет предложено выбрать текущий. Это единственный вариант, при котором появляется диалоговое окно.

.. figure:: _static/NGConnect_export_select_style_ru.png
   :name: NGConnect_export_select_pic
   :align: center
   :width: 20cm
   
   Выбор текущего QGIS-стиля

2. При выборе в дереве Connect **стиля** слоя, добавятся все стили, по умолчанию будет выбранный.

3. При добавлении **группы ресурсов**, которая содержит слои с несколькими стилями, будут добавлены все стили и выбран либо одноименный слою, либо первый по алфавиту. Диалог с выбором показан не будет.

4. При добавлении WFS/OGCF диалога выбора не будет. Стиль будет выбран либо одноименный слою, либо первый по алфавиту.


Выбрать другой стиль для загруженного слоя можно будет в свойствах слоя.


Если слой экспортировался успешно, то в панели слоев QGIS появится новый векторный слой GeoJSON, который можно использовать в текущих проектах или сохранить на устройство в нужном формате.

.. _ngcom_connect_save_to_device:

Экспорт в файл слоя или стиля
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Чтобы сохранить **слой** на устройстве, выберите в главном меню :menuselection:`Слой --> Сохранить как` или в панели слоев вызовите контекстное меню и нажмите :menuselection:`Экспорт --> Сохранить объекты как`.

.. figure:: _static/NGConnect_export_save_ru.png
   :name: NGConnect_export_save_pic
   :align: center
   :width: 20cm
   
   Сохранение векторного слоя в файл

Чтобы сохранить на устройстве **стиль** QGIS векторного слоя, в панели Connect вызовите к нему контекстное меню и выберите **Загрузить как QML**.

.. figure:: _static/NGConnect_export_style_save_ru.png
   :name: NGConnect_export_style_save_pic
   :align: center
   :width: 7cm

   Загрузка стиля слоя как файла QML


.. _ngcom_ngqgis_connect_resource_group:

Создание Групп ресурсов
-------------------------------------------------------------------

Модуль NextGIS Connect позволяет быстро создавать новые Группы ресурсов в Веб ГИС. Для этого:

* Выберите в дереве ресурсов Веб ГИС в окне модуля NextGIS Connect Группу ресурсов, в которой вы хотите создать новую Группу;
* Нажмите кнопку **Создать новую группу ресурсов** на панели инструментов модуля или выберите пункт **Создать новую группу** в контекстном меню;
* В открывшемся диалоговом окне укажите имя новой Группы ресурсов;
* Если Группа ресурсов создалась успешно, то она появится в дереве ресурсов Веб ГИС.


.. _web_map:

Создание веб-карты на основе слоя
----------------------------------

* Выберите в дереве ресурсов Веб ГИС в окне модуля NextGIS Connect векторный или растровый слой, который вы хотите представить на веб-карте;
* В контекстном меню выберите **Создать веб-карту**.

В той же группе ресурсов будет создана веб-карта с именем вида "имя_слоя-map". Для слоя будет создан стиль QGIS и добавлен на веб-карту. Начальный охват карты устанавливается по охвату слоя.

.. _ngcom_connect_resource_double:

Дублирование ресурсов
-----------------------

При помощи модуля можно создать копию слоя в Веб ГИС. Доступно для ресурсов Векторный слой и Растровый слой. 

* Чтобы скопировать слой, выберите его в окне модуля Connect и в контекстном меню нажмите **Дублировать ресурс**.
* Во всплывающем окне подтвердите дублирование.

Копия слоя будет создана в той же папке, стиль слоя также будет скопирован.

.. figure:: _static/NGConnect_double_ru.png
   :name: NGConnect_double_pic
   :align: center
   :width: 8cm

   Дублирование ресурса

.. _ngcom_ngqgis_connect_resource_delete:

Удаление ресурсов
--------------------------------------------------------

Модуль NextGIS Connect позволяет быстро создавать / удалять любые ресурсы из Веб ГИС. Для этого:

* Выберите в дереве ресурсов Веб ГИС в окне модуля NextGIS Connect ресурс, который вы хотите удалить;
* Выберите пункт **Удалить** в контекстном меню;
* Если ресурс удалился успешно, то он исчезнет из дерева ресурсов Веб ГИС.


Больше информации о модуле расширения NextGIS Connect - `здесь <https://docs.nextgis.ru/docs_ngconnect/source/toc.html>`_. 
