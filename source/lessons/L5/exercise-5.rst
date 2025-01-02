Exercise 5
==========

.. note::

    Please complete this exercise by **the start of the next lesson**.

.. admonition:: Start your assignment

    **You can start working on your copy of Exercise 5 by** `accepting the GitHub Classroom assignment <https://classroom.github.com/a/ueF64liU>`__.

You can also take a look at the template repository for `Exercise 5 on GitHub <https://github.com/Geo-Python-2024/Exercise-5>`__ (does not require logging in).
Note that you should not try to make changes to this copy of the exercise, but rather only to the copy available via GitHub Classroom.


Ziel der Übung
--------------

-  web-basierte Hintergrundkarten nutzen
-  Vektordaten händisch erstellen (Digitalisieren)

Wiki:
-----

-  `Basemaps <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Basemaps>`__
-  `Digitalisieren <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Digitalisierung>`__

Daten
-----

Ladet euch `die Daten herunter <exercise_05a_data.zip>`__ und speichert
sie auf eurem PC. Legt einen lokalen Ordner an und speichert dort die
obigen Daten. (.zip Ordner müssen vorher entpackt werden.)

Aufgaben
--------

Häuser und Straßen kartieren
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Erstellt zwei neue Layer für (a) Häuser und (b) Straßen in
   Heidelberg.
2. Fügt zu jedem Layer ein Attribute “Name” hinzu.
3. Nutzt als Kartierungsgrundlage eine Hintergrundkarte auf Basis von
   Satellitendaten (z.B. Bing, OSM)
4. Erstelle mindestens 3 Polygone je Layer. Befülle die von dir
   erstellten Spalten mit Informationen.
5. Füge zu jedem Feature den passenden Namen und einen Hyperlink hinzu.

.. code-block:: python

    august_values = data.loc[data['YR--MODAHRMN'] >= 201708010000]

Here, the value ``201708010000`` corresponds to the first day of August at the hour 00:00.


Übung 5b
========

Ziel der Übung
--------------

-  web-basierte Hintergrundkarten nutzen
-  Ein Bild Georeferenzieren

Wiki:
-----

-  `Basemaps <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Basemaps>`__
-  `Georeferenzieren <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Georeferenzierung>`__

Daten
-----

Ladet euch `die Daten herunter <exercise_05b_data.zip>`__ und speichert
sie auf eurem PC. Legt einen lokalen Ordner an und speichert dort die
obigen Daten. (.zip Ordner müssen vorher entpackt werden.)

Ein Bild georeferenzieren
~~~~~~~~~~~~~~~~~~~~~~~~~

Kontext
^^^^^^^

Du brauchst für dein Projekt eine geologische Karte von Heidelberg. Die
einzig verfügbaren Informationen, die du finden kannst ist eine PDF
Karte der Universität Heidelberg. Um diese geologische Karte mit deinen
weiteren Geodaten zu verknüpfen, müssen wir diese georeferenzieren.

.. figure:: geologische_karte_heidelberg.PNG
   :alt: Geologische Karte von Heidelberg

   Geologische Karte von Heidelberg

.. raw:: html

   <p align="center">

Quelle: UB Heidelberg

.. raw:: html

   </p>

1. Versehe das zur Verfügung gestellte Raster mit WGS 84 / UTM Zone 32N
   Koordinaten (EPSG: 32632).
2. Verwende als Referenz-Layer eine Webkarte deiner Wahl (bspw. OSM
   Standard oder Bing Satellite), welche du in Form einer
   Hintergrundkarte einbinden kannst.
3. Wähle eine geeignete Transformationsvorschrift (bspw. Ploynominal 1,
   2 oder 3) und setzt genügend und ausreichend verteilte Passpunkte.
4. Kontrolliere abschließend deinen Erfolg, indem du die Passgenauigkeit
   des georeferenzierten Bildes mit überlagerten Hintergrundkarte
   vergleichst.

