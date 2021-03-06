.. sectionauthor:: Роман Гайнуллов <roman.gainullov@nextgis.ru>

.. _ngcom_layer_as_basemap:

Как использовать любой слой вашей Веб ГИС как базовую карту
==========================================================

Любой слой (стиль), созданный в Веб ГИС, можно использовать как источник тайлового сервиса и подключать его как **базовую карту** (подложку).
Для этого следует:

1. Создать нужный `слой <https://docs.nextgis.ru/docs_ngweb/source/layers.html#ngw-create-layers>`_ и `стиль <https://docs.nextgis.ru/docs_ngweb/source/mapstyles.html#qgis>`_ (как векторный, так и растровый) для него. Внутри будет ссылка **TMS сервиса** - она понадобится далее;  
2. Включить `кэширование <https://docs.nextgis.ru/docs_ngweb/source/mapstyles.html#ngw-create-tile-cache>`_ (для ускорения работы на веб-карте, доступно только на плане `Premium <https://nextgis.ru/pricing-base/>`_);
3. Создать ресурс "Базовая карта" со снятой галочкой "Использовать настройки из QMS" и адресом (ссылкой) вышесозданного TMS слоя.
