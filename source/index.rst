.. Geo-Python documentation master file, created by
   sphinx-quickstart on Thu Aug 23 14:00:02 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. image:: img/banner/world-map.png
    :class: dark-light

Willkommen zu Einführung in GIS für Geowissenschaften!
===========================


Der GIS-Kurs vermittelt Ihnen die grundlegenden Konzepte der Geoinformationssysteme (GIS) und der wissenschaftlichen Datenanalyse unter Verwendung der 
GIS-Software QGIS (keine Vorkenntnisse erforderlich). Jede Lektion ist ein Tutorial zu spezifischen Themen, bei dem das Ziel darin besteht, Fähigkeiten und Verständnis zu erlangen, wie man gängige raumbezogene Aufgaben mit GIS löst. 
Der Kurs wurde in Kooperation mit der GIS-Station, der Pädagogischen Hochschule Heidelberg für das Geowissenschaftliche Institut der Uni Heidelberg entwickelt. 


Lernziele
---------

-  Übertragung von Konzepten aus der Vorlesung in praktische Abläufe
-  Betrachtung des Workflows von GIS-Analysen (EVAP ohne Erhebung (E))

   -  Datenmanagement (V)
   -  Datenanalyse (A)
   -  Kartenerstellung (P)

-  Einführung in ein Desktop GIS-System: Quantum GIS (open source)

Überblick über den Ablauf und die Inhalte der Übungen
-----------------------------------------------------

Ablauf
~~~~~~

-  Die Übungen werden hier in Github bereitgestellt.
-  Die Inhalte der Übungen sollt ihr euch selbständig erarbeiten. Im
   `Wiki <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/-/wikis/home>`__
   findet ihr alle nötigen Informationen um Übungsaufgaben zu meistern.
   Hier findet ihr Kurzanleitungen, Tipps und Videos. Ein Dankeschön
   geht hier an die Ersteller:innen der Seite, an die GIScience Group
   der Uni Heidelberg & das HeiGIT.
-  Beachtet: Aufgrund technischer Probleme mit dem Gitlab Wiki kann es
   vorkommen, dass einige Links nicht funktionieren.
-  Die Vorlesungsfolien wird euch per Mail zugeschickt.
-  Bei Fragen wendet euch direkt an mich oder schreibt per Mail (siehe
   Folien).

Inhalte
~~~~~~~

Anhand der Übungen lernt ihr,\ **wie** ihr praktisch vorgeht. Ihr
versteht **warum** eure Lösungen funkionieren und erhaltet eine
Übersicht wie **GIS-Systeme** arbeiten. Die Übungen sind als praktische
**Hands-On** Sessions gestaltet.

+-------+--------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Übung | Typ    | Thema                                                                                                                                                          |
+=======+========+================================================================================================================================================================+
| 0     | Vektor | `Einführung <https://github.com/GeowazM/Einfuehrung-GIS-fur-Geowissenschaften/tree/main/exercise_0>`__                                                         |
+-------+--------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 1     | Vektor | `Layer- & Attribute <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/lessons/L1/exercise-1-tectonicplates.html>`__                       |
+-------+--------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 2     | Vektor | `Eine Karte erstellen <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/lessons/L2/exercise-2.html>`__                                    |
+-------+--------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 3     | Vektor | `Mit Attributtabellen arbeiten <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/lessons/L3/exercise-3.html>`__                           |
+-------+--------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 4     | Vektor | `Räumliche Abfrage nutzen <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/lessons/L4/exercise-4.html>`__                                |
+-------+--------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 5     | Raster | `Digitalisieren <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/lessons/L5/exercise-5.html>`__                                          |
+-------+--------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 6     | Raster | `Copernicus Daten & 3D Visualisierungen <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/lessons/L6/exercise-6.html>`__                  |
+-------+--------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 7     | Raster | `Digitale Geländemodelle nutzen <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/lessons/L7/exercise-7b.html>`__                         |
+-------+--------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 8     | Raster | `Räumliche Interpolation durchführen <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/lessons/L8/exercise-8.html8>`__                    |
+-------+--------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 9     | Vektor | `Prozesse automatisieren <https://einfuhrung-gis-fur-geowissenschaften.readthedocs.io/de/latest/lessons/L9/exercise-9.html>`__                                 |
+----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                | Vorbereitung Abschlussprojekt                                                                                                                                  |
+----------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+

--------------


.. admonition:: Abschlussprojekt

    **WICHTIG:** Die Abgabe des Abschlussprojekts erfolgt ausschließlich per Mail. Achtet darauf, dass ein anderer Nutzer dein QGIS Projekt mit allen Layern öffnen kann. Die aus der Gesamt-Punktzahl resultierende Note wird dem Prüfungssekretariat gemeldet.


.. admonition:: Interessante Links

    - https://arcg.is/1vqrur 
    - https://www.geotis.de/geotisapp/geotis.php
    - https://www.nlog.nl/southern-permian-basin-atlas
    - https://nibis.lbeg.de/cardomap3/

.. admonition:: On-site teaching

    Please note that the course is organized completely on site during the 2023 autumn semester.
    Online support for University of Helsinki and Aalto University students will be available in the discussion channels in Discord.

.. toctree::
    :maxdepth: 2
    :caption: Kursinhalte

    course-info/course-info
    course-info/grading
    course-info/resources
    course-info/theteam
    course-info/licensing

.. toctree::
    :maxdepth: 2
    :caption: Erste Schritte in QGIS

    lessons/L0/overview
    lessons/L0/wiki
    lessons/L0/exercise-0


.. toctree::
    :maxdepth: 2
    :caption: Das Layerprinzip

    lessons/L1/overview
    lessons/L1/exercise-1-germany
    lessons/L1/exercise-1-tectonicplates

.. toctree::
    :maxdepth: 2
    :caption: Eine Karte erstellen

    lessons/L2/overview
    lessons/L2/why-pairs
    lessons/L2/exercise-2

.. toctree::
    :maxdepth: 2
    :caption: Mit Attributen arbeiten

    lessons/L3/overview
    lessons/L3/exercise-3

.. toctree::
    :maxdepth: 2
    :caption: Vektorgeometrien verarbeiten

    lessons/L4/overview
    lessons/L4/exercise-4

.. toctree::
    :maxdepth: 2
    :caption: Geodaten erfassen

    lessons/L5/overview
    lessons/L5/exercise-5

.. toctree::
    :maxdepth: 2
    :caption: Rasterdaten verarbeiten

    lessons/L6/overview
    lessons/L6/exercise-6

.. toctree::
    :maxdepth: 2
    :caption: Digitale Geländemodelle nutzen

    lessons/L7/overview
    lessons/L7/exercise-7b

.. toctree::
    :maxdepth: 2
    :caption: Vom Punkt zur Fläche

    lessons/L8/overview
    lessons/L8/exercise-8


.. toctree::
    :maxdepth: 2
    :caption: Prozesse automatisieren

    lessons/L9/overview
    lessons/L9/exercise-9