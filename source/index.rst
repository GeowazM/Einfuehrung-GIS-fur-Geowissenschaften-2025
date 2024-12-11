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

+-----------------------------------+-----------------------------------+
| Übung                             | Thema                             |
+===================================+===================================+
| 0                                 | `Ei                               |
|                                   | nführung <https://github.com/Geow |
|                                   | azM/Einfuehrung-GIS-fur-Geowissen |
|                                   | schaften/tree/main/exercise_0>`__ |
+-----------------------------------+-----------------------------------+
| 1                                 | `Layerkonzept,                    |
|                                   | Attrib                            |
|                                   | utdaten <https://github.com/Geowa |
|                                   | zM/Einfuehrung-GIS-fur-Geowissens |
|                                   | chaften/tree/main/exercise_01>`__ |
+-----------------------------------+-----------------------------------+
| 2                                 | `Eine Karte                       |
|                                   | er                                |
|                                   | stellen <https://github.com/Geowa |
|                                   | zM/Einfuehrung-GIS-fur-Geowissens |
|                                   | chaften/tree/main/exercise_02>`__ |
+-----------------------------------+-----------------------------------+
| 3                                 | `Vektor - Mit Attributtabellen    |
|                                   | a                                 |
|                                   | rbeiten <https://github.com/Geowa |
|                                   | zM/Einfuehrung-GIS-fur-Geowissens |
|                                   | chaften/tree/main/exercise_03>`__ |
+-----------------------------------+-----------------------------------+
| 4                                 | `Vektor - Räumliche Abfrage       |
|                                   | nutzen <https://github.com/Geowa  |
|                                   | zM/Einfuehrung-GIS-fur-Geowissens |
|                                   | chaften/tree/main/exercise_04>`__ |
+-----------------------------------+-----------------------------------+
| 5a                                | `Digitali                         |
|                                   | sieren <https://github.com/Geowaz |
|                                   | M/Einfuehrung-GIS-fur-Geowissensc |
|                                   | haften/tree/main/exercise_05a>`__ |
+-----------------------------------+-----------------------------------+
| 5a                                | `Georeferen                       |
|                                   | zieren <https://github.com/Geowaz |
|                                   | M/Einfuehrung-GIS-fur-Geowissensc |
|                                   | haften/tree/main/exercise_05b>`__ |
+-----------------------------------+-----------------------------------+
| 6                                 | `Raster - Klassifizierung von     |
|                                   | Sentinel-2 Daten & 3D             |
|                                   | Visualisi                         |
|                                   | erungen <https://github.com/Geowa |
|                                   | zM/Einfuehrung-GIS-fur-Geowissens |
|                                   | chaften/tree/main/exercise_06>`__ |
+-----------------------------------+-----------------------------------+
| 7                                 | `Raster - Digitale Geländemodelle |
|                                   | nutzen <https://github.com/Geowa  |
|                                   | zM/Einfuehrung-GIS-fur-Geowissens |
|                                   | chaften/tree/main/exercise_07>`__ |
+-----------------------------------+-----------------------------------+
| 8                                 | `Räumliche Interpolation          |
|                                   | durc                              |
|                                   | hführen <https://github.com/Geowa |
|                                   | zM/Einfuehrung-GIS-fur-Geowissens |
|                                   | chaften/tree/main/exercise_08>`__ |
+-----------------------------------+-----------------------------------+
| 9                                 | `Prozesse                         |
|                                   | automat                           |
|                                   | isieren <https://github.com/Geowa |
|                                   | zM/Einfuehrung-GIS-fur-Geowissens |
|                                   | chaften/tree/main/exercise_09>`__ |
+-----------------------------------+-----------------------------------+
|                                   | Vorbereitung Abschlussprojekt     |
+-----------------------------------+-----------------------------------+

--------------


.. admonition:: Abschlussprojekt

**WICHTIG:** \* Die Abgabe des Abschlussprojekts erfolgt ausschließlich
per Mail. Achtet darauf, dass ein anderer Nutzer dein QGIS Projekt mit
allen Layern öffnen kann. \* Die aus der Gesamt-Punktzahl resultierende
Note wird dem Prüfungssekretariat gemeldet.

Links: \* https://www.geotis.de/geotisapp/geotis.php \*
https://www.nlog.nl/southern-permian-basin-atlas \*
https://nibis.lbeg.de/cardomap3/



The **Geo-Python** course teaches you the basic concepts of programming and scientific data analysis using the Python programming language in a format that is easy to learn and understand (no previous programming experience required).
Each lesson is a tutorial with specific topic(s) where the aim is to gain skills and understanding how to solve common data-related tasks using Python.
Geo-Python is jointly organized by the `Master's Program in Geography <https://www.helsinki.fi/en/degree-programmes/geography-masters-programme>`_ and the `Bachelor's Program in Geoscience <https://www.helsinki.fi/fi/koulutusohjelmat/geotieteiden-kandiohjelma>`_ at the University of Helsinki.




Geo-Python covers the essential skills needed to continue to more advanced courses such as `Automating GIS processes <https://autogis.github.io>`_ and/or `Introduction to Quantitative Geology <https://introqg.github.io>`_.

.. admonition:: Open Access!

    The course is **open for everyone to follow online**.
    The aim of this course is to share the knowledge and help people to get started with their journey towards doing science more efficiently and in a reproducible manner using Python programming.

.. admonition:: University of Helsinki students

    The Geo-Python course is run under two course codes in teaching period I at the University of Helsinki.
    Please sign up using only one of these course codes (not both)!

    - GEOG-329-1 for geography students
    - GEOK3001 for geology students

Course format
-------------

The majority of this course will be spent in front of a computer learning to program in the Python language.
The course consists of interactive lectures and weekly exercises.
The exercises will focus on developing basic programming skills using Python and applying those skills to various analytical problems.
Typical exercises will involve a brief introduction followed by topical computer-based tasks.
For each exercise, you may be asked to submit the Python codes you have written, output figures and answers to related questions.
You are encouraged to discuss and work together with other students while working on the weekly exercises.
However, the exercises you submit must must clearly reflect your own work (in short, don't copy/paste from other students).

.. admonition:: On-site teaching

    Please note that the course is organized completely on site during the 2023 autumn semester.
    Online support for University of Helsinki and Aalto University students will be available in the discussion channels in Discord.

.. toctree::
    :maxdepth: 2
    :caption: Kursinhalte

    course-info/course-info
    course-info/learning-goals
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
    :caption: Lesson 2

    lessons/L2/overview
    lessons/L2/intro-to-GitHub
    lessons/L2/log-in-GitHub
    lessons/L2/Github-classroom
    lessons/L2/why-pairs
    lessons/L2/exercise-2

.. toctree::
    :maxdepth: 2
    :caption: Lesson 7

    lessons/L1/motivation
    lessons/L1/overview
    lessons/L1/course-environment-components
    lessons/L1/discord-usage
    notebooks/L1/a-taste-of-python.ipynb
    notebooks/L1/gcp-1-variable-naming.ipynb
    lessons/L1/exercise-1