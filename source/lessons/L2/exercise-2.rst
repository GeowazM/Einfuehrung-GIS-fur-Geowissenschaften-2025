Exercise 2
==========

Ziel der Übung
--------------

-  Eigene Vektorsignaturen gestalten.
-  Eine Karte gestalten und typische Elemente wie Legenden, Nordpfeile
   und Maßstabsleisten hinzufügen.
-  Eine Karte als PDF-Dokument exportieren.

Wiki:
-----

-  `Vektorsignaturen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Vektorsignaturen>`__
-  `Kartengestaltung <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Kartengestaltung>`__

Daten
-----

Ladet euch `die Daten herunter <exercise_02_data.zip>`__ und speichert
sie auf eurem PC.

-  Punkt-Layer: Bodenschaetze Punkte (Quelle: `Bundesanstalt für
   Geowissenschaften und Rohstoffe
   (BGR) <https://services.bgr.de/atomfeeds/dataset_e2ea5cd4-87f4-4751-980a-3451fe2f5758.xml>`__)
-  Polygon-Layer (Quelle: `Landesamt für Geoinformation und
   Landentwicklung <https://www.lgl-bw.de/Produkte/Open-Data/>`__):

Aufgaben
--------

1. Öffne die oben angegebenen Dateien in QGIS.
2. Wähle für das Punkt-Layer eine passende Symbologie.
3. Ändere das Koordinatenbezugssystem (Projektion) eurer Ansicht auf ein
   für Deutschland passenderes.
4. Erstelle eine neue Druckzusammenstellung. Nutzt das Format A4
   (Querformat) für eure Karte.
5. Stelle einen passenden Maßstab ein (z.B. 1:2000000).
6. Versehe deine Karte mit Nordpfeil und Maßstab (Maßstabsbalken und
   Numerischen Maßstab).
7. Füge abschließend Legende, Autor und Datenquelle(n) hinzu.
8. Speicher deine Karte als PDF.

So (oder ähnlich) sieht’s am Ende aus
-------------------------------------

.. image:: bodenschaetze_bw_map.png

.. admonition:: Start your assignment

    **You can start working on your copy of Exercise 2 by** `accepting the GitHub Classroom assignment <https://classroom.github.com/a/1gVkWpT7>`__.

You can also take a look at the template repository for `Exercise 2 on GitHub <https://github.com/Geo-Python-2024/Exercise-2>`__ (does not require logging in).
Note that you should not try to make changes to this copy of the exercise, but rather only to the copy available via GitHub Classroom.

.. admonition:: Pair programming

    Students attending the course in Helsinki, **note that we are working in pairs on this exercise**.
    We will only grade the repository of the member of your pair that is responsible for this week's exercise (i.e., the driver).
    See more information in Discord and on the course page under `Why are we working in pairs? <https://geo-python-site.readthedocs.io/en/latest/lessons/L2/why-pairs.html>`_

Cloud computing environments
----------------------------

.. image:: https://img.shields.io/badge/launch-binder-red.svg
   :target: https://mybinder.org/v2/gh/Geo-Python-2024/Binder/main?urlpath=lab
   
.. image:: https://img.shields.io/badge/launch-CSC%20Noppe-blue.svg
   :target: https://noppe.csc.fi/ 

Exercise 2 hints
----------------

Here are a few things that may be helpful in completing Exercise 2.

Git
~~~

You can find step-by-step instructions for using Git on the course page titled :doc:`git-basics`.
Remember to commit your changes after each major edit! Also, it's better to push your changes to GitHub frequently, rather than only at the very end of the exercise.

Indentation woes
~~~~~~~~~~~~~~~~

We have not really run into this problem in the lessons, but Python codes are sensitive to how much you indent the start of each line.
This is perhaps easiest to see with an example.

.. code:: python

    name = 'Dave'
        dogs = 0
    print('My name is', name, 'and I own', dogs, 'dogs.')

If you copy and paste this code into a **Jupyter Notebook** cell and run it, you will see that is gives an ``IndentationError``.

.. code:: python

        dogs = 0
        ^
    IndentationError: unexpected indent

We will see examples later of why indentation matters, but for now just be sure you don't indent lines to different levels.
Thus, the fix is simply to remove the spaces on the second line.

.. code:: python

    name = 'Dave'
    dogs = 0
    print('My name is', name, 'and I own', dogs, 'dogs.')

Now, running the code results in the expected output.

.. code:: python

    My name is Dave and I own 0 dogs.
