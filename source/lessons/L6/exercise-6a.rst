Exercise 5b
==========

.. note::
   
   Ziel der Übung
      -  Rasterdaten im GIS öffnen und kennenlernen
      - farbliche Darstellung der Rasterwerte anpassen
      - Rasterdaten in Vektordaten umwandeln
      - Globale Rasteroperationen anwenden (z.B. Projektion ändern)
      - Lokale Rasteroperationen anwenden (z.B. NDVI berechnen)

.. note::

   Wiki
      -  `Rasterdaten im GIS öffnen und kennenlernen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/qgis-Layer-Konzept>`__
      -  `Darstellung von Rasterdaten <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/qgis-Rasterdarstellung>`__
      -  `Vektordaten in Rasterdaten umwandeln <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/qgis-Konvertierung>`__
      -  `Globale Rasteroperationen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/qgis-Globale-Funktionen>`__
      -  `Lokale Rasteroperationen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/qgis-Lokale-Funktionen>`__


.. seealso::

   Daten
      Ladet euch vom USB-Stick und speichert sie auf eurem PC. Legt einen lokalen Ordner an und speichert dort die Daten. (.zip Ordner müssen vorher entpackt werden.)
      - Landsat 8 data (Source: Landsat-8 image courtesy of the U.S. Geological Survey; Downloaded via EarthExplorer `EarthExplorer <https://earthexplorer.usgs.gov/>`__ )
      - ASTER Global Digital Elevation Map (GDEM) SRTM DEM (Source: `NASA JPL <https://asterweb.jpl.nasa.gov/GDEM.asp>`__)


Aufgaben
--------

Aufgabe 1: Arbeiten mit Geländemodellen

   - Verbindet die ASTER-Kacheln (ASTGMT2) miteinander (z.B. mit merge).
   - Bringt das ASTER-Höhenmodell in eine metrische Projektion (z.B. WGS84/UTM 37N).
   - Verschafft euch einen Überblick über die Höhenwerte. Was sind die maximalen und minimalen Höhen im Untersuchungsgebiet. Schaut dies in den Layer-Eigenschaften nach.
   - Berechnet aus dem ASTER-Höhenmodell Konturlinien 100 Meter Schritten.
   - Berechnet ein Hillshade (dt. Schummerung).

Aufgabe 2: Arbeiten mit Landsat 8 Daten

   - In dieser Aufgabe arbeiten wir mit Daten des Landsat 8 Satelliten (LC08). Wir nutzen für unsere Analyse die Bänder 2, 3, 4 & 5. Welchen Farben entsprechen diese Bänder?
   - Erstellt ein Raster Komposit (bzw. Virtual Raster) aus den gegebenen Bändern.
   - Visualisiert das Komposit in Falschfarben, sodass Vegetation rot erscheint (siehe Symbology).
   - Berechnet den Normalized Difference Vegetation Index (bspw. mit dem Raster Calculator).
   - Erstellt anschließend NDVI-Klassen (Reclassify by table). Orientiert euch dabei an folgender Einteilung.

+-----------+-----------------------+-----------+
| Kategorie                         | NDVI      |
+===================================+-----------+
| Wasser und Schnee                 |       < 0 | 
+-----------------------------------+-----------+
| Felsen, Sand, Gebäude	            |   0 - 0.2 |
+-----------------------------------+-----------+
| Gras, Sträucher	                  | 0.2 - 0.4 | 
+-----------------------------------+-----------+
| Wald und intensive Landwirtschaft	|     > 0.4 | 
+-----------------------------------+-----------+

   - Stellt die Klassen farblich sinnvoll dar.

Aufgabe 3: 3D Visualisierung erstellen

   - Erstellt ein Polygon (Vektordatei), mit dem ihr die Landsat-8 Daten und das ASTER-Höhenmodell verkleinern (clippen) könnt. Ziel ist es ein Untersuchungsgebiet um den Vesuv zu definieren.
   - Installiert das Plugin Qgis2threejs.
      * Startet den Qgis2threejs Explorer,
      * aktiviert das ASTER Höhenmodell & das Landsat-8 Bild.
      * Tipp: Ändere die Überhöhung (exaggeration) in den Scene Settings zu 2.5.
   - Schaut euch das Modell an, findet eine gute Perspektive und exportiert diese als .png

In den Daten findet ihr eine Landsat 9 Satellitenbildaufnahme, die am 17.07.2023 aufgenommen wurde. Wir wollen herausfinden, wie groß die von Lava überflossene Fläche ist.

   1. Erstellt zwei neue Layer: Einen für (a) die Lavafläche und einen zweiten (b) für Straßen. Fügt zu jedem Layer ein Attribute "Name" hinzu.
   2. Nutze als Kartierungsgrundlage die Landsat 9 Aufnahme in den Daten und eine Hintergrundkarte auf Basis von Satellitendaten (z.B. Bing, OSM). Diese könnt ihr mit Hilfe des Plugins QuickMapServices in QGIS einbinden. Was ist der UNterschied zwischen Bing Satellite und der Landsat-9 Aufnahme?
   3. Digitalisiere die Fläche des Eruptionsereignissen ab. Digitalisiere ebenfalls die Straße von Reykjavik nach Grindavik inkl. deren Kennzeichnung ab.
   4. Füge zu jedem Feature den passenden Namen hinzu.
   5. Berechne die Fläche der von dir digitalisierten Lavafläche. Wie viel km² sind es?
   6. Optional: Füge zur von dir bestimmten Lavafläche einen Hyperlink zu weiteren Informationen (bspw. siehe unten) hinzu.

Für weitere Informationen könnt ihr hier reinschauen: `NASA Earth Observation <https://earthobservatory.nasa.gov/images/151653/lava-and-smoke-blanket-fagradalsfjall>`__
Einige vor Ort Aufnahmen könnt ihr euch hier anschauen: `Volcano at Litlihrutur Iceland <https://youtu.be/tvxbKWxmfXk?si=XYrX663QaoqlOEPo>`__

.. figure:: https://raw.githubusercontent.com/GeowazM/Einfuehrung-GIS-fur-Geowissenschaften/refs/heads/main/exercise_06/qgisthreejs.jpg
   :alt: 3D Model

   Quelle: 3D Model erstellt mit qgisthreejs
