.. _ngcom_resources_list:

Как организовано управление данными
=====================================================================

Управление геоданными в :ref:`Веб ГИС <ngcom_description>` организовано с помощью системы ресурсов. В настоящий момент поддерживаются следующие типы ресурсов:

**Ресурсы, необходимые для управления геоданными из локальных источников**:

* `Растровый слой <https://docs.nextgis.ru/docs_ngweb/source/layers.html#ngw-create-raster-layer>`_ (создается для загрузки и хранения растровых геоданных)
* `Векторный слой <https://docs.nextgis.ru/docs_ngweb/source/layers.html#ngw-create-vector-layer>`_  (создается для загрузки и хранения векторных геоданных)

.. hint::
   Загруженные данные сразу можно `подключать во внешние приложения <https://docs.nextgis.ru/docs_ngweb/source/services.html>`_.

**Ресурсы, необходимые для управления геоданными из внешних источников**:

* `Подложка веб-карты <https://docs.nextgis.ru/docs_ngweb/source/webmaps_admin.html#ngw-create-basemap>`_ (создается для подключения дополнительных базовых карт на `Веб-карту <https://docs.nextgis.ru/docs_ngweb/source/webmaps_admin.html>`_)
* `Соединение PostGIS <https://docs.nextgis.ru/docs_ngweb/source/postgis_details.html#ngw-create-postgis-connection>`_ (создается для подключения к внешней базе данных :term:`PostGIS`)
* `Слой PostGIS <https://docs.nextgis.ru/docs_ngweb/source/postgis_details.html#ngw-create-postgis-layer>`_ (создается для подключения к конкретной таблице с геоданными через существующее Соединение PostGIS)
* `Соединение WMS <https://docs.nextgis.ru/docs_ngweb/source/connections.html#ngw-create-wms-connection>`_ (создается для подключения к внешнему серверу :term:`WMS`)
* `Слой WMS <https://docs.nextgis.ru/docs_ngweb/source/connections.html#ngw-create-layer-wms
>`_ (создается для подключения к конкретным растровым слоям через существующее Соединение WMS)
* `Соединение TMS <https://docs.nextgis.ru/docs_ngweb/source/connections.html#ngw-create-tms-connection>`_ (создается для подключения к внешнему серверу :term:`TMS`)
* `Слой TMS <https://docs.nextgis.ru/docs_ngweb/source/connections.html#ngw-tms-layer>`_ (создается для подключения к конкретным слоям через существующее Соединение TMS)


**Ресурсы, необходимые для просмотра и публикации геоданных**:

* `Стиль <https://docs.nextgis.ru/docs_ngweb/source/mapstyles.html>`_ (особый “служебный” вид ресурса, создается внутри Растровых слоев, Векторных слоев и Слоев PostGIS для их добавления на Веб-карту и публикации по протоколу WMS) 
* `Веб-карта <https://docs.nextgis.ru/docs_ngweb/source/webmaps_admin.html>`_ (создается для просмотра существующих Растровых слоев, Векторных слоев, Слоев PostGIS и Слоев WMS на карте через встроенный веб-клиент) 
* `Сервис WFS <https://docs.nextgis.ru/docs_ngweb/source/services.html#ngw-wfs-service>`_ (создается для публикации существующих Векторных слоев и Слоев PostGIS по протоколу :term:`WFS`) 
* `Сервис WMS <https://docs.nextgis.ru/docs_ngweb/source/services.html#ngw-wms-service>`_ (создается для публикации существующих Растровых слоев, Векторных слоев, Слоев PostGIS и Слоев WMS по протоколу WMS)
* `Сервис OGC API Features <https://docs.nextgis.ru/docs_ngweb/source/services.html#ngw-OGC-API-Features>`_ (Используя эти сервисы, сторонние программы могут изменять векторные данные на сервере).

**Ресурсы, необходимые для организации хранения геоданных**:

* `Группа ресурсов <https://docs.nextgis.ru/docs_ngweb/source/create_resource.html#ngw-resourses-group>`_ (аналог группировки “по папкам”)


