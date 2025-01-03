Basemaps
========

QuickMapServices
----------------

-  Online-Karten (z.B. eines Tile Map Services) in die Kartenansicht
   einbetten
-  QuickMapServices Plugin installieren
-  eine Basemap auswählen und der Kartenansicht hinzufügen
-  (evtl. Projektion der Kartenansicht auf *Web Mercator* setzen)

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/f60155be829c234707f0f4bf5804466c/QuickMapServices.mp4">

.. raw:: html

   </video>

OSM Place Search
----------------

-  Navigation auf zuvor eingebettete Basemaps erleichtern
-  OSM place search Plugin installieren
-  Zielort eingeben und aus Liste passenden Eintrag auswählen

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/75709196b2ee8a45bcca95c4b1619fca/OSM_Place_Search.mp4">

.. raw:: html

   </video>

Digitalisierung
===============

Ein neues Layer erstellen
-------------------------

-  Dateinamen angeben
-  Geometrietyp wählen
-  Koordinatensystem wählen
-  Attributfelder anlegen
-  erstellt zunächst lediglich ein leeres File –> Geometrien und
   Attribute müssen anschließend noch eingetragen werden

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_create_layer.mp4">

.. raw:: html

   </video>

Geometrien zu einem Layer hinzufügen
------------------------------------

-  (evtl. Digitize-Toolbar öffnen)
-  Editiermodus starten
-  Geometrien zeichen und Attributwerte eintragen
-  Edits speichern, Editiermodus beenden

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_digitize_add_feature.mp4">

.. raw:: html

   </video>

-  Ringe hinzufügen (z.B. Innenhof eines Gebäudes kartieren)

-  (evtl. advanced Digitizing-Toolbar öffnen –> unter: ``Ansicht``; ``Werkzeugkästen``; ``Erweiterte Digitalisierungswerkzeugleiste``)

-  Rechtecke können außerdem ‘automatischer’ mit der “Werkzeugleiste für Formen”/ “Shape Digitizing Toolbar” hinzugefügt werden (zu öffnen unter –> ``Ansicht/View``; ``Werkzeugkästen/Toolbars``)

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_digitize_add_ring.mp4">

.. raw:: html

   </video>

Bestehende Geometrien im Layer ändern
-------------------------------------

-  Editiermodus starten
-  Stützpunkte (Vertices) verschieben und neue Stützpunkte hinzufügen
-  Edits speichern, Editiermodus beenden

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_digitize_move_vertices.mp4">

.. raw:: html

   </video>

-  Editiermodus starten
-  Stützpunkte markieren und löschen (``Entf``-Taste drücken)
-  Edits speichern, Editiermodus beenden

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_digitize_delete_vertices.mp4">

.. raw:: html

   </video>

Georeferenzierung
=================

-  *Raster >> Georeferenzierung* (ggfs. Erweiterung GDAL-Georeferenzierung installieren)

Wichtiges zur Georeferenzierung
-------------------------------

Ziel der Georeferenzierung ist es, einen Geodatensatz ohne Realwelt-Koordinaten anhand von Referenzdaten mit Realweltkoordinaten so
zu übersetzten, dass danach ein räumlicher Bezug hergestellt ist. Dabei wird das Koordinatensystem des zu georeferenzierenden Geodatensatzes
anhand von Passpunkten modifiziert: mithilfe von Rotation(Drehung), Translation(Verschiebung) und Skalierung(Dehnung/Stauchung) und ggf. Entzerrung wird der Geodatensatz räumlich verortet.

Wichtig für die Übung sind zwei Methoden: 
   1. Georeferenzieren auf Grundlage einer analogen Karte: 
      * Bedingungen: 
      * KNE muss bekannt sein
      * Mindestens 4 Koordinatenpunkte müssen bekannt sein
      * Pixelwerte müssen auf Meterangaben skaliert werden
      * als Passpunkte werden die Schnittpunkte vom Gitternetz des zugrundeliegenes KNE verwendet
      * Vorteil: Schnittpunkte genau in Karte ablesbar und damit Passpunkte präzise setzbar 
   2. Georeferenzieren auf Grundlage eines Luftbilds: 
      * Passpunkte wählen anhand von gut verortbaren Orten in den beiden Datensätzen Zentral für die Georeferenzierung sind Passpunkte, anhand derer von QGIS
         eine Regression vorgenommen wird. Die Genauigkeit der Georeferenzierung steht und fällt daher mit der Genauigkeit der Passpunkte. 
         Die gewählten Passpunkte sollten daher drei Eigenschaften erfüllen – sie sollten
      * ausreichend viele sein (→ Mindestanzahl der Passpunkte erfüllen → RMS-Fehler bestimmbar)
      * gut verteilt sein (→ je näher zusammen, desto weniger aussagekräftig der RMS-Fehler für Genauigkeit der Georeferenzierung)
      * möglichst gut zu verorten sein (→ exaktere Übereinstimmung der Passpunkte)
   
Je nachdem, wie gut diese Eigenschaften erfüllt sind, wirkt sich dies auf die Genauigkeit der Übersetzung aus. Diese wird von QGIS durch den
RMS-Fehler berechnet – je niedriger dieser ist, desto genauer die Georeferenzierung, sofern die obigen Bedingungen erfüllt sind.

Vorgehen in QGIS
----------------

Reihenfolge in der Regel: 1. `nicht-georeferenziertes Bild öffnen </content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#bild-oeffnen-und-zielprojektion-festlegen>`__
2. `Zielprojektion festlegen </content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#bild-oeffnen-und-zielprojektion-festlegen>`__
3. `Transformationseinstellungen wählen </content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#transformationseinstellungen>`__
4. `Passpunkte setzen </content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#passpunkte-setzen-und-speichern>`__
5. `Passpunkte speichern </content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#passpunkte-setzen-und-speichern>`__
6. `Georeferenziertes Bild speichern </content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#georeferenziertes-bild-speichern>`__
7. Georeferenzierung überprüfen

-  `Weitere Ressourcen </content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#weitere-ressourcen>`__
-  `Allgemeine Fehlerhinweise </content/gis/06_georef-digitalize/qgis-Georeferenzierung.md#allgemeine-fehlerhinweise>`__

Bild öffnen und Zielprojektion festlegen
-----------------------------------------

-  Raster einladen und auf Nachfrage die Zielprojektion festlegen

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_georeference_set_projection.mp4">

.. raw:: html

   </video>

**Hinweis:** Wenn das Programm die Zielprojektion nicht von alleine
abfragt, müssen die Einstellungen zu den KBS geändert werden. Das
funktioniert unter *Einstellungen/Settings* in den Toolbars,
*Optionen/Options* und dann unter dem Reiter *KBS/CRS*. In diesem muss
unter *KBS für neue Layer/CRS for new layers* die Option *KBS
abfragen/Prompt for CRS* gewählt werden.

|Einstellungen_KBS-abfragen|\ |Einstellungen_KBS-abfragen_01|

Transformationseinstellungen
----------------------------

-  Koordinatentransformation wählen
-  Resampling Methode wählen
-  Output-Pfad wählen

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_georeference_transformation_settings.mp4">

.. raw:: html

   </video>

**Praktische Hinweise:** 
   * wenn das Raster nur gedreht, skaliert und verschoben werden muss *Polynom 1. Grades*
   * wenn das Raster gekrümmt oder gebeugt werden muss *Polynom 2. oder 3. Grades*
   * Für die Zahl der Passpunkte gilt: 
      * Min. Zahl Passpunkte 𝑚=(((𝑡+1)(𝑡+2)))/2 (t = Grad d. Transformation)
      * Das mathematisch „beste“ Modell wird erreicht, wenn exakt die erforderliche Zahl m verwendet wird (RMS-Fehler = 0)
      * Geographisch bessere Ergebnisse werden erzielt, wenn leicht mehr Punkte gesetzt werden (Grund: Punkte werden nicht perfekt gesetzt).

Passpunkte setzen und speichern
-------------------------------

-  Passpunkte sollten gleichmäßig verteilt sein, da sonst eine lokal    fehlerhafte Transformation droht
-  Passpunkte sollten so präzise wie möglich platziert werden
-  Lieber mäßig viele gute Punkte, als viele schlecht platzierte!

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_georeference_set_points_grid.mp4">

.. raw:: html

   </video>

-  Passpunktkoordinaten im Kartengrid ablesen und eintragen

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_georeference_set_points_from_layer.mp4">

.. raw:: html

   </video>

-  Passpunktkoordinaten anhand eines anderen Layers wählen

Georeferenziertes Bild speichern
--------------------------------

-  Bild speichern
-  Datei öffnen und Georeferenzierung überprüfen
-  in unserem Beispiel zeigt das Ergebnis eine unterschiedliche Güte für
   verschiedene Regionen (z.B. relativ gut im zentralen Teil, weniger
   gut in Nord- und Südamerika)

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/QGIS/videos/qgis_georeference_save.mp4">

.. raw:: html

   </video>

Weitere Ressourcen:
-------------------

-  `Digital Geography Tutorial: wie georeferenziere ich eine gescannte
   Karte in
   QGIS? <http://de.digital-geography.com/QGIS-tutorial-teil-1-wie-georeferenziere-ich-eine-gescannte-karte-mit-QGIS/>`__

Allgemeine Fehlerhinweise
-------------------------

Fehler können unter anderem zu Stande kommen durch:
   * fehlerhaftes Ablesen der Koordinaten (beim Ablesen von Passpunktkoordinaten im Kartengrid) 
   * eine fehlende Übereinstimmung zwischen Projekt-KBS, KBS des georeferenzierten Layers und übrigen Layern vor Beginn des Georeferenzieren

.. |Einstellungen_KBS-abfragen| image:: https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/d5872200508a16e8cd9f0a8f678566fc/Einstellungen_KBS-abfragen.png
.. |Einstellungen_KBS-abfragen_01| image:: https://courses.gistools.geog.uni-heidelberg.de/giscience/qgis-book/-/raw/main/uploads/bf065093109e2512911bfa9d77e3f77a/Einstellungen_KBS-abfragen_01.png
