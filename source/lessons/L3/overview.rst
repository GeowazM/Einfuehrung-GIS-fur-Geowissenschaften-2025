Arbeiten mit Attributtabellen
========================

Das zentrale Merkmal von Vektordatentypen ist die Attributtabelle. In dieser Stecken die Sachdaten, die mit der Geometrie verknüpft sind. 
Beispiel: Der Punkt beschreibt die Position eines Vulkans auf der Erde. In der Attributtabelle befindet sich die Sachdaten wie der Name des Vulkans 
und das Datum der letzten Eruption.

Manuelle Auswahl
----------------

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_attribute_table.mp4">

.. raw:: html

   </video>

-  manuell in der Attributtabelle auswählen durch anklicken

Select by Expression
--------------------

Arithmetische Operatoren (Integer, Float-Felder)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  ``>``, ``<``, ``=``, ``!=``
-  z.B. alle Städte mit mehr als 20 Millionen Einwohnern im Jahr 2015:
   ``"2015" > 20000``

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_expresion_greater.mp4">

.. raw:: html

   </video>

String Operatoren (Text-Felder)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  ``LIKE``
-  z.B. alle Länder in Asien: ``"continent" LIKE 'asia'``

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_expression_like.mp4">

.. raw:: html

   </video>

-  man kann auch ``%`` als *Platzhalter* nutzen und so nach bestimmten
   Teilwörtern selektieren
-  z.B. alle Länder, welche auf ``stan``\ enden: ``"name" LIKE '%stan'``

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_expression_placeholder.mp4">

.. raw:: html

   </video>

Logische Operatoren
~~~~~~~~~~~~~~~~~~~

-  ``AND``, ``OR``
-  können dafür genutzt werden, verschiedene Abfragen oder Kriterien zu
   kombinieren
-  z.B. alle Städte, welche 1950 noch keine Millionenstadt waren, aber
   2015 schon mehr als 10 Millionen Einwohner hatten:
   ``"1950" < 1000 AND "2015" > 10000``

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_by_expression_and.mp4">

.. raw:: html

   </video>


Selektierte Features als neue Datei speichern
---------------------------------------------

-  Layer-Properties –> Export –> Save only selected features

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_select_export.mp4">

.. raw:: html

   </video>



Weitere Informationen findest du in der `QGIS Dokumentation <https://docs.qgis.org/3.40/en/docs/user_manual/working_with_vector/attribute_table.html#introducing-the-attribute-table-interface
>`__
