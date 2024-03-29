.. sectionauthor:: Роман Гайнуллов <roman.gainullov@nextgis.ru>

.. _ngcom_webmap_optimize:

Как оптимизировать работу Веб-карты
===================================

На Веб-карте показываются данные, отрисовываемые сервером. Чем больше этих данных, тем больше ресурсов сервера уходит на их отрисовку и тем медленнее может показываться ваша Веб-карта. Есть ряд моментов, которые можно продумать и настроить, чтобы увеличить производительность.

**Не показывайте всё сразу**

Это общая, универсальная рекомендация. Продумайте, хотите ли вы показывать пользователю вашей Веб-карты все данные сразу по открытии карты. Как правило, визуально это не информативно. На общих зумах лучше показывать небольшое количество данных "для ориентировки".

**Масштабные уровни**

Установите диапазон `масштабных уровней <https://docs.nextgis.ru/docs_ngweb/source/webmaps_admin.html?highlight=%D0%BC%D0%B0%D1%81%D1%88%D1%82%D0%B0%D0%B1#admin-webmap-create-layers>`_ отображения данных на веб-карте.
Это позволит не запрашивать данные вне этого интервала и, как следствие, не показывать много данных на масштабах, где это не нужно.

**Кэширование**

Настройте `кэширование <https://docs.nextgis.ru/docs_ngweb/source/mapstyles.html#ngw-create-tile-cache>`_ для стилей ваших векторных слоев.
Это позволит не запрашивать повторно уже отрисованные данные. Обратите внимание, что несмотря не то, что технически это можно сделать, для растров включать кэширование - не следует.

**Сервисы**

Современная интерактивная карта - часто сложная конструкция и может подключать источники данных, такие как картографические подложки, сервисы WMS, TMS и т.п. из различных внешних источников. В зависимости от скорости работы этих источников они могут сильно замедлять и вашу карту. Удалите подключения внешних сервисов или хотя бы отключите их, чтобы они не показывались по-умолчанию.

**Установите адаптер Изображение**

В настройках Веб-карты на вкладке "Слои" `установите <https://docs.nextgis.ru/docs_ngweb/source/webmaps_admin.html?highlight=%D0%B0%D0%B4%D0%B0%D0%BF%D1%82%D0%B5%D1%80#admin-webmap-create-layers>`_ адаптер **Изображение** для ускорения отрисовки ваших данных. Без особых причин не стоит использовать тайлы - это может сказаться на скорости работы всей Веб ГИС при большом количестве данных.

**Используйте базовые растровые стили вместо стилей QGIS**

Если вы показываете на вашей карте большие растры, то вы сможете немного их ускорить за счет использования простых растровых стилей, вместо стилей QGIS. Зайдите в растровые слои, создайте растровые стили (не QGIS) и добавьте их на карту вместо стилей QGIS.
