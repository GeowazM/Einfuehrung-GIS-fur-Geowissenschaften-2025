Übung 7b
========

Ziel der Übung
--------------

-  Rasterdaten zuschneiden
-  Reliefanalysen durchführen
-  zonale Statistiken berechnen
-  Rasterdaten in Vektordaten umwandeln
-  ein Höhenprofil erstellen

Wiki:
-----

-  `fokale
   Rasteroperationen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Fokale-Funktionen>`__
-  `zonale
   Rasteroperationen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Zonale-Funktionen>`__
-  `weitere
   Rasteroperationen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Weitere-Rasterfunktionen>`__
-  `Rasterdaten in Vektordaten
   umwandeln <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Konvertierung>`__

Daten
-----

Ladet euch die Daten vom USB-Stick und speichert sie auf eurem PC. Legt
einen lokalen Ordner an und speichert dort die obigen Daten. (.zip
Ordner müssen vorher entpackt werden.) \* Linien-Layer: Transect_1 und
Transect_2 (Quelle: Own research) \* Raster-Layer: SRTM Höhendaten
(Quelle: NASA JPL (2013). NASA Shuttle Radar Topography Mission Global 1
arc second. Accessed 2024-03-14 from
https://doi.org/10.5067/MEaSUREs/SRTM/SRTMGL1.003 )

Aufgaben
--------

In dieser Aufgabe schauen wir uns das Nördlinger Ries genauer an.
Verschaffe dir einen ersten Eindruck über den UNESCO Global Geopark Ries
`hier <https://www.geopark-ries.de/geologie/>`__. Ein kleines Video zu
den Besonderheiten des Nördlinger Ries findet ihr
`hier <https://www.youtube.com/watch?v=YPRzwbnE6kI>`__. ### Aufgabe 1:
Vorbereitung des DEM (Digital Elevation Model) \* Verschmelzt die
SRTM-Kacheln (SRTMGL1) miteinander (z.B. via **Merge**). \* Bringt das
Höhenmodell in eine passende **metrische Projektion** (z.B. WGS 84 / UTM
32N). \* Verschafft euch einen Überblick über die Werte. Bei digitalen
Geländemodellen sind dies immer Höhenwerte. Was sind die maximalen und
minimalen Höhen im Untersuchungsgebiet? \* Ladet euch mit Hilfe von
*QuickMapServices* eine *OSM Standard* Hintergrundkarte (**Basemap**) in
euer Projekt. Wo befindet sich unser Untersuchungsgebiet?

Aufgabe 2: Ein Höhenprofil erstellen
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Vorsicht: Plugins können etwas undurchsichtig sein. Achtet auf die
   einzelnen Schritte des Erklärvideos. Kleinigkeiten können hier
   entscheidend sein.
-  Erstellt für den Transect_1-Layer ein Höhenprofil (bspw. Profil_1a).
-  Das Höhenprofil soll auf der x-Achse die Distanz in Meter zeigen &
   auf der y-Achse die Höhe ü.N.
-  Speichert euer Höhenprofil als PNG ab.
-  Glättet jetzt euer Ergebnis in dem ihr pro Pixel den Durchschnitt der
   21x21 Nachbarschaft berechnet (via **r.neighbors**).
-  Erstellt mit Hilfe des Transect_1-Layer nochmals ein Höhenprofil
   (bspw. Profil_1b). Speichert es erneut und vergleicht es mit dem
   ersten Profil. Was für ein Unterschied ist erkennbar?
-  Jetzt erstelle ein Höhenprofil mit dem Transect_2 Layer und
   exportiere dies ebenfalls (bspw. Profil_3).
-  Kreiere eine eigene Linie (**Layer - Create layer**), visualisiere
   damit ein Höhenprofil und speichere dies (Profil 3).

Das Profil des Transect_1-Layer müsste so aussehen: |profile|

Hier eine Übersicht über die Profile, die ihr erstellen könnt. \|
Vektorlayer \| Beispielname \| DEM \| \| — \| — \| — \| \| Transect_1 \|
Profil_1a.png \| DEM \| \| Transect_1 \| Profil_1b.png \| DEM geglättet
\| \| Transect_2 \| Profil_2.png \| DEM geglättet \| \| Eigene Linie \|
Profil_3.png \| DEM geglättet \|

Aufgabe 3: Das Relief analysieren und visualisieren
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Aufgabe 3a: Visualisieren
^^^^^^^^^^^^^^^^^^^^^^^^^

-  Berechnet eine Schummerung (via **Hillshade**) für das Geländemodell.
   Tipp: Nutze die Processing - Toolbox, um Funktionen zu finden.
-  Füge den Wert 0 (schwarze Ränder am Dateirand) den No Data Values
   hinzu (via *Transparency - Additional…*)
-  Schiebe das Höhenmodell-Layer (DEM) über den Hillshade-Layer und
   setze die Transparenz des DEMs auf 70% (**Transparency - Global
   Opacity**).
-  Ermittelt die Hangneigung in ° (via **Slope**). Diese kann eine
   Visualisierung ebenfalls aufwerten.

Aufgabe 3b: Analysieren
^^^^^^^^^^^^^^^^^^^^^^^

-  Selektiert besonders steile Regionen (>20°) (nutzt dazu das
   **Reclassify Tool**)
-  Erstellt Übersichtsstatistiken für die beiden Nationalparks (bspw.
   mit Hilfe von **Zonal Statistics**).

   -  Schaut euch die Werte an. Was zeigen uns die Zahlen?
   -  Was ist die maximale Hangneigung pro Nationalpark?
   -  Wie hoch ist die durchschnittliche Hangneigung pro Nationalpark?

-  Konvertiert die Auswahl ins Vektorformat (**Conversion - Raster to
   Vector**). Anschließend kannst du das **Basic statistic per field**
   nutzen.

.. |profile| image:: profil_noerdlinger_ries.png

