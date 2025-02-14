Übung 8
=======

.. note::
   
   Ziel der Übung
      - Räumliche Interpolation anwenden
      - Rasterfunktionen vertiefen

.. hint::

      -  `Räumliche Interpolationsverfahren <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Räumliche-Interpolationsverfahren>`__
      -  `lokale Rasterfunktionen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Konvertierung>`__

.. seealso::

   Daten
      - Ladet euch die `Daten herunter <https://drive.google.com/file/d/1dlhFX5jOUJlZ0bNdei4iQWQ6xCXnkDTh/view?usp=drive_link>`__ und speichert sie auf eurem PC (.zip Ordner nach dem Download entzippen).
      - Landsat 8 data (Source: Landsat-8 image courtesy of the U.S. Geological Survey; Downloaded via `EarthExplorer <https://earthexplorer.usgs.gov/>`__)
      - ASTER Global Digital Elevation Map (GDEM) SRTM DEM (Source: `NASA JPL <https://asterweb.jpl.nasa.gov/GDEM.asp>`__)

Daten
-----

Lade dir `die Daten herunter <exercise_08_data_new.zip>`__ und speichert sie auf eurem PC. Lege einen lokalen Ordner an und speichere dort die obigen Daten. (.zip Ordner müssen vorher entpackt werden.) 
* Höhenmodell: germany_dem.tif (Quelle: `GTOPO30 USGS <https://www.usgs.gov/centers/eros/science/usgs-eros-archive-digital-elevation-global-30-arc-second-elevation-gtopo30?qt-science_center_objects=0#qt-science_center_objects>`__)
* Messstationen: `DWD <%5Bhttps://www.geo.fu-berlin.de/en/v/soga/Geodata-analysis/geostatistics/Data-sets-used/DWD-weather-data-Germany/index.html%5D(https://www.dwd.de/DE/leistungen/cdc/climate-data-center.html;jsessionid=19070115479E2AED22A5D5D622F8CA58.live31083?nn=17626)>`__

Aufgaben
--------

Aufgabe 1: Von der Textdatei zu Geodaten
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Bringe die Daten in ein geeignetes Koordinatensystem (z.B. WGS84/UTM 32N).
-  Importiere die Tabelle in QGIS. Hinweis: Achte auf die Formatierung (engl. vs. dt.)

Aufgabe 2: Temperaturwerte interpolieren.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Schaue dir nach dem erfolgreichen importieren der Daten die Attributtabelle an und notiere dir den Spaltennamen für die Jahresdurchschnittstemperatur.
-  Inpterpoliere anhand der gewonnenen Werte die Durchschnittstemperaturen in Deutschland.

   * Nutze dazu Inverse Distanz Gewichtung (IDW)
   * und einen Power-Wert von 2

-  Style das Ergebnis, sodass Temperaturunterschiede deutlich erkennbar werden.

.. figure:: https://raw.githubusercontent.com/GeowazM/Einfuehrung-GIS-fur-Geowissenschaften/refs/heads/main/exercise_08/temperatur_idw_pow2.PNG
   :alt: 3D Model

   Quelle: Daten vom Deutschen Wetter Dienst (`SWS - CDC (Climate Data Center) <https://www.dwd.de/DE/leistungen/cdc_portal/cdc_portal.html;jsessionid=C122F15176D4A325829CC896BBAAE9B9.live31093?nn=17626>`__)
