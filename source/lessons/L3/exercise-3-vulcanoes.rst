Exercise 3
==========

.. hint::

   Ziel der Übung
      * Nicht-räumliche Abfragen durchführen.
      * Räumliche Abfragen durchführen.
      * Geometrieoperationen nutzen (z.B. die Fläche eines Polygons berechnen).

.. admonition:: Hilfe

   **Support findest du im Wiki**
      *  `Projektionen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Projektionen>`__
      *  `Nicht-Räumliche Abfragen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Nicht-Räumliche-Abfragen>`__
      *  `Räumliche Abfragen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Räumliche-Abfragen>`__
      *  `Geometrieoperationen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Geometrieoperationen>`__

.. seealso::

   Daten
   Lade dir die `Datenfür die Exercise 3 herunter <https://drive.google.com/file/d/1PgPannrjP2JuDgtKvFBathNstQ-WKmvD/view?usp=drive_link>`__ und speichert sie auf eurem PC.

   Beschaffe dir folgende weitere Daten:
      - `Lade dir die Geodaten der Platten- & Plattengrenzen <https://github.com/fraxen/tectonicplates/tree/master/GeoJSON>`__ herunter
      - `Lade dir die World Admin 0 Countries Daten <https://www.naturalearthdata.com/downloads/110m-cultural-vectors/>`__ herunter

   Quellen
      -  Vulkane (`Global Volcanism Program (2024): Volcanoes of the World (v. 5.2.5; 23 Dec 2024). Distributed by Smithsonian Institution, compiled by Venzke, E., DOI: https://doi.org/10.5479/si.GVP.VOTW5-2024.5.2. <https://volcano.si.edu/gvp_votw.cfm>`__)
      -  Platten- & Plattengrenzen (`Hugo Ahlenius, Nordpil and Peter Bird basierend auf doi: 10.1029/2001GC000252 <https://github.com/fraxen/tectonicplates>`__)
      -  World Admin 0 Countries (`Natural Earth Data <https://www.naturalearthdata.com/downloads/110m-cultural-vectors/>`__)
      -  CIESIN - Columbia University. 2018. Gridded Population of the World, Version 4 (GPWv4) - `NASA Socioeconomic Data and Applications Center (SEDAC). https://doi.org/10.7927/H49C6VHW. <https://www.earthdata.nasa.gov/data/catalog/sedac-ciesin-sedac-gpwv4-popcount-r11-4.111>`__

Aufgaben
--------

Von den Geodaten zu den Informationen. Ein EU Forschungsprojekt möchte herausfinden, wie viele Italiener:innen in der Nähe zu aktiven Vulkanen 
leben und international vergleichen. Nutze dafür die Daten des Global Volcanism Program.

1. Öffne die oben angegebenen Dateien in QGIS.
2. Wähle in der Benutzeroberfläche 3 Vulkane deiner Wahl (manuell) aus. Öffne nun die Attributtabelle und lass dir die Informationen für die
   ausgewählten Vulkane (Features) anzeigen. Speichere die ausgewählten Vulkane anschließend in einer neuen Datei.
3. Wähle mit einer Abfrage alle Vulkane aus, in dessen 10km Radius mehr als 80.000 Einwohner beheimaten. Wie viele Vulkane
   gibt es, die diese Bedingung erfüllen? Welcher Vulkan hat in seinem 10km Radius die meisten Einwohner?
4. Führe nun eine kombinierte Abfrage durch. Selektiere zunächst alle Vulkane in Italien. Entferne anschließend Vulkane, deren letzte Eruption vor 1850 stattgefunden hat. 
   Wie viele Vulkane gibt es in Italien, die seit 1850 aktiv waren? Wie viele Einwohner befinden sich dort?
5. Im Pazifik scheint ein Vulkan besonders viel Bevölkerung innerhalb des 10km Radius zu beheimaten. Prüfe auf Plausibiltät!?

.. figure:: img/vulcanoes_italy.png
   :alt: Vulkane in Italien
   :width: 800px

   Vulkane in Italien. Daten von `Global Volcanism Program <https://volcano.si.edu/gvp_votw.cfm>`__ und `DLR - EOC Geoservice <https://geoservice.dlr.de/web/services>`__
 