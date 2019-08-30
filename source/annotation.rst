.. _ngcom_annotation:

.. _nextgis.com: http://nextgis.com/
.. _WYSIWYG: https://en.wikipedia.org/wiki/WYSIWYG
.. role:: raw-html(raw)
    :format: html

Web map annotations
===================

.. note:: 
	You can use described functionality in Web GIS created in nextgis.com_ service on `Premium plan <http://nextgis.com/pricing/#premium/>`_

Annotation. What is it?
~~~~~~~~~~~~~~~~~~~~~~~~

Annotations are text messages attached to the points, which you can create and display on any :ref:`Web map <ngcom_webmap_create>`. You can create your own set of annotations for each Web map.

Annotation consists of a point and a message attached to this point.

.. figure:: _static/ann_annotation_structure_new_eng.png
   :name: ann_messages_example
   :align: center
   :width: 16cm

   Annotation structure (1 - a text message of annotation, 2 - a point of annotation)

The main aim of annotations is to specify user's data by placing of temporary messages on a Web map.

.. figure:: _static/ann_messages_example_eng.png
   :name: ann_messages_example
   :align: center
   :width: 16cm

   An example of annotation display

At the same time, you can use annotations as a simple tool for creation of point data with text attributes attached to the Web map.

.. figure:: _static/ann_data_example_eng.png
   :name: ann_data_example
   :align: center
   :width: 16cm

   An example of annotation display (as point data)

.. note::
    In contrast to a full vector layer annotation tool does not allow to export data, search for it etc. Therefore, we reccomend you to use :ref:`vector layers <ngcom_vector_layer>` for creation of a great amount of data.

How to plug in Web map annotations?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can enable creation and set display options for annotations in Settings tab of "Create resource" or "Update resource" windows for a certain Web map (see :ref:`Update resource <ngw_update_resource>`). By default annotation tool is inactive.

.. figure:: _static/ann_settings_eng.png
   :name: ann_settings
   :align: center
   :width: 16cm

   Settings tab of a Web map for administration of annotations (annotations are enabled and are shown on a Web map when opened)

There are next options in Settings tab of a Web map:

- **Enable annotations** - enable or forbid work with annotations in an editting Web map.
- **Show annotations by default** - if there is a tick next to *"Enable annotations"*, annotations are shown on a Web map when it opened. Otherwise they will be hidden.

Web map: a panel for work with annotations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If option *"Enable annotations"* is active, the "Annotations" panel appears on a Web map:

.. figure:: _static/ann_panel_eng.png
   :name: ann_panel
   :align: center
   :width: 16cm

   "Annotations" panel on a Web map

"Annotations" panel consists of net options:

- **Show annotations layer** - allows to show or hide points and messages of annotations.
- **Show messages** - allow to show or hide annotation messages, but does not influence on points of annotations.
If *Show annotations layer* is inactive, this option is also inactive.
- **Edit annotations** - activate or inactivate annotation edit mode.

Web map: annotation editting
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can create and edit annotations, if option *Edit annotations* on *"Annotations" panel* is active. When it is active, a mouse pointer looks as a blue point appears near and a pictogram appears above existing annotations:

.. figure:: _static/ann_edit_option_eng.png
   :name: ann_edit_option
   :align: center
   :width: 16cm

   Annotation edit mode

To **create** an annotation you need to click with a left button of a mouse on a Web map. Then a dialog window of annotation creation will be opened:

.. figure:: _static/ann_create_eng.png
   :name: ann_create
   :align: center
   :width: 16cm

   Dialog window of annotation creation

Dialog of annotation creation consists of:

- **Editor of annotation message** - WYSIWYG_ editor of annotation text message.
- **Stroke: width / color** - width and color of annotation point stroke.
- **Fill color** - color of annotation point.
- **Circle size, px** - size (diameter) of annotation point in pixels.

Click *"Save"* button, an annotation will appear on a Web map.

To **edit** annotations you need to activate annotation edit mode, point an annotation and click a pictogram on it with a left button of a mouse. Dialog window of annotation editting looks like a dialog window of annotation creation, but has a *"Delete"* button, which allows to **delete** chosen annotation.

Web map: user's permissions associated with annotations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For fine setting of work with annotations you can use access permissions (you can read more in :ref:`Setting permissions <ngw_access_rights>`of NextGIS Web documentation).

There are two permissions associated with annotations:

- **Web map: View annotations** - allows or forbids annotation view for some users for separate resources. If it sets to Deny value, "Annotations" panel is inactive.
- **Web map: Edit annotations** - allows of forbids editting of annotations for some users for separate resources. If it sets to Deny value, "Edit annotations" option on "Annotations" panel is inactive.

Using above-mentioned permissions you can set annotations as following:

.. list-table::

   * - Settings
     - Result
   * - | Web map: Enable annotations - Yes
       | Web map: Show annotations by default - Yes
       | AnnotationScope.Read - Allowed
       | AnnotationScope.Write - Allowed
     - | "Annotations" panel is active on a Web map
       | There is a tick next to "Show annotations by default"
       | Annotation editting tools are available
       | Annotations are shown on a Web map
   * - | Web map: Enable annotations - Yes
       | Web map: Show annotations by default - Yes
       | AnnotationScope.Read - Allowed
       | AnnotationScope.Write - Deny
     - | "Annotations" panel is active on a Web map
       | There is a tick next to "Show annotations by default"
       | Annotation editting tools are available
       | Annotations are shown on a Web map
   * - | Web map: Enable annotations - Yes
       | Web map: Show annotations by default - Yes
       | AnnotationScope.Read - Deny
       | AnnotationScope.Write - Deny
     - |"Annotations" panel is inactive on a Web map
       | Annotations are not shown on a Web map
   * - | Web map: Enable annotations - No
     - | "Annotations" panel is inactive on a Web map
       | Annotations are not shown on a Web map
   * - | Web map: Enable annotations - Yes
       | Web map: Show annotations by default - No
       | AnnotationScope.Read - Allowed
       | AnnotationScope.Write - Allowed
     - | "Annotations" panel is active on a Web map
       | There is no tick next to "Show annotations by default"
       | Annotation editting tools are not available
       | Annotations are not shown on a Web map

