.. _ngcom_improve_translation:

How to improve translation
=============================

NextGIS Web is an open solution, which can be improved by any user.
The following user interface languages are currently available for NGW:

* Bulgarian
* Czech
* Deutsch
* English
* Spanish
* French
* Italian
* Portuguese
* Russian
* And Chinese


We invite users to contribute to the quality of our translations.
If you are an expert in any of the listed languages, you can improve the current user interface by yourself.


.. figure:: _static/ngw_translation_3.png
   :name: ngw_translation_3
   :align: center
   :width: 20cm    

   NextGIS Web GUI project for user interface translation


Join the project
-----------------

The translation of `NextGIS Web <https://nextgis.ru/nextgis-web/>`_ is carried out on the platform `POEditor <https://poeditor.com/>`_.
First, you need to `sign up <https://poeditor.com/login/>`_. 
After authentication you can join the NextGIS Web GUI project via this `link <https://poeditor.com/join/project?hash=dOVs4gs2WS>`_.
Then select languages and click **Join translation**.
After that, this `page <https://poeditor.com/projects/>`_ will display a list of projects (in our case, NextGIS Web GUI) that have a set of selected languages.


.. figure:: _static/ngw_translation_1.png
   :name: ngw_translation_1
   :align: center
   :width: 10cm    

   Selecting a language for translation


How to translate
----------------

To start translating click on the icon of a specific language in the project.
Row order and filter are customizable. There is also a search.

.. figure:: _static/ngw_translation_2.png
   :name: ngw_translation_2
   :align: center
   :width: 20cm    

   Translator UI window

Strings often contain such parameter names as ‘date_first’ and ‘date_last’ like in the image above. They don't need to be translated.

Russian translation example:

* en. - *'date_first' and 'date_last' are mutually exclusive*.
* ru. - *'date_first' и 'date_last' взаимоисключающие*.

Also you can see these parameters: %s, %d, %f and like these that also don’t require the translation.
When the program is running, they are automatically replaced by string or numeric parameters.

Example 1:

* en. - *User count: %d*.
* ru. - *Количество пользователей: %d*.

Example 2:

* en. - *Field ‘%s(?)’ encoding is broken*.
* ru. - *Кодировка поля ‘%s(?)’ повреждена*.


Parameters are often enclosed in single quotes ', double quotes " or brackets ().
Such diversity does not make much sense and is explained by the lack of agreement among developers on formatting.
Leave it in the translation as in the original raw.
