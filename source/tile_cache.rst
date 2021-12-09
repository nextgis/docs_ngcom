.. sectionauthor:: Роман Гайнуллов <roman.gainullov@nextgis.ru>

Как включить кэширование
=========================

Кэширование используется для ускорения отрисовки данных и `оптимизации <https://docs.nextgis.ru/docs_ngcom/source/webmap_optimize.html>`_ работы веб-карт.
Оно может быть применимо для стилей `векторных <https://docs.nextgis.ru/docs_ngweb/source/mapstyles.html>`_ и `растровых <https://docs.nextgis.ru/docs_ngweb/source/layers.html#qgis>`_ слоев, а также для слоев `WMS <https://docs.nextgis.ru/docs_ngweb/source/layers.html#c-wms>`_ и `TMS <https://docs.nextgis.ru/docs_ngweb/source/layers.html#tms>`_.

Чтобы включить кэширование, нужно:

* Перейти на вкладку "Тайловый кэш" в соответствующем ресурсе
* Активировать чекбокс "Включен"
* В соответствии с конкретной задачей выставить настройки максимального масштабного уровня кэширования, TTL, а при необходимости очистки кэша и разрешения использования закешированных тайлов (tile) при запросе картинок (image)

Подробнее про кэширование написано `здесь <https://docs.nextgis.ru/docs_ngweb/source/mapstyles.html#ngw-create-tile-cache>`_.
