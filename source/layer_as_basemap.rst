.. sectionauthor:: Roman Gainullov <roman.gainullov@nextgis.com>

.. _ngcom_layer_as_basemap:

How to use any layer in your Web GIS as a basemap
==================================================

Any layer (style) created in Web GIS can be used as a source of a tile service and connected as a basemap.
To do this, you should:

1.
2.
3.


1. Создать нужный `слой <https://docs.nextgis.ru/docs_ngweb/source/layers.html#ngw-create-layers>`_ и `стиль <https://docs.nextgis.ru/docs_ngweb/source/mapstyles.html#qgis>`_ (как векторный, так и растровый). Внутри будет ссылка TMS сервиса - она понадобится далее;  
2. Включить `тайловое кэширование <https://docs.nextgis.ru/docs_ngweb/source/mapstyles.html#ngw-create-tile-cache>`_ (для ускорения работы на веб-карте);
3. Создать ресурс "Базовая карта" со снятой галочкой "Использовать настройки из QMS" и адресом (ссылкой) вышесозданного TMS слоя.
