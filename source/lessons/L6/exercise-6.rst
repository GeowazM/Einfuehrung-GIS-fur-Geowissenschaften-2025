Exercise 6
==========

.. note::

    Please complete this exercise by **the start of the next lesson**.


Exercise 6 hints
-----------------

Data format for problems 1-3
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The first 5 rows of the data file look like the following:

.. code:: python

    STATION           ELEVATION  LATITUDE   LONGITUDE  DATE     PRCP     TAVG     TMAX     TMIN     
    ----------------- ---------- ---------- ---------- -------- -------- -------- -------- -------- 
    GHCND:FIE00142080         51    60.3269    24.9603 19520101 0.31     37       39       34       
    GHCND:FIE00142080         51    60.3269    24.9603 19520102 -9999    35       37       34       
    GHCND:FIE00142080         51    60.3269    24.9603 19520103 0.14     33       36       -9999    

As you can see, we have rainfall data (``PRCP``) in inches, and temperature data (``TAVG``, ``TMAX``, and ``TMIN``) in degrees Fahrenheit.
Dates of the observations are given in the format YYYYMMDD.
No-data values are indicated with ``-9999``.

Reading in fixed-width text files
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Rather than having separation by commas, our data file this week has a variable number of spaces between values.
Previously, we read in comma-separated values using the option ``sep=','`` for the Pandas ``read_csv()`` function.
For a variable number of spaces we can either use the ``sep`` or ``delim_whitespace parameter``; ``sep='\s+'`` or ``delim_whitespace=True`` will work, but not both.
In this case, we suggest using ``delim_whitespace``.

Skipping the second row of a file
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The ``skiprows=n`` option of the Pandas ``read_csv()`` function is an easy way to skip the first *n* rows of a file when reading it.
If we wanted to skip the first two rows of our data file, we could thus use ``skiprows=2``.
The value for ``n``, however, need not be a single value, but can also be given in the form of a list.
In this way, one can skip reading the second row of a file using a list with an index value for the second row.
In other words, you can use ``skiprows=[1]``.

Joining data from one DataFrame to another
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

One quite useful functionality in Pandas is the ability to conduct a **table join**
where data from one DataFrame is merged with another DataFrame based on a common **key**.
Hence, making a table join requires that you have at least one common variable in both
of the DataFrames that can be used to combine the data together.

Consider a following example. Let's first create some test data to our DataFrames.

.. ipython:: python
    :suppress:

        import pandas as pd

.. ipython:: python

    data1 = pd.DataFrame(data=[['20170101', 'Pluto'], ['20170102', 'Panda'], ['20170103', 'Snoopy']], columns=['Time', 'Favourite_dog'])
    data2 = pd.DataFrame(data=[['20170101', 1], ['20170101', 2], ['20170102', 3], ['20170104', 3], ['20170104', 8]], columns=['Time', 'Value'])
    data1
    data2

As we can see here, there different number of rows in the DataFrames. Important thing to notice is that there seems to be a common column called ``Time`` that we can use to
join these DataFrames together. In Pandas we can conduct a table join with ``merge`` -function. Consider following example where we join the data **from** ``data2`` DataFrame **to** ``data1`` DataFrame.

.. ipython:: python

    join1 = data1.merge(data2, on='Time')
    join1

Ahaa! Now we can see that we managed to get the ``Value`` column from ``data2`` in our ``data1`` DataFrame (here we just assigned those values to a new variable ``join1``).
Notice also that the ``Pluto`` is two times in the joined DataFrame although, it was only once in the original one. Hence, Pandas automatically duplicates the values in such
columns where there are more matching values in one DataFrame compared to the other.

However, it is important to notice that there were more values in the ``data2`` DataFrame than in ``data1``. The result ``join1``, does not contain the values ``3 and 8`` that were from day ``20170104`` and they were omitted.
This might be okey, but in some cases it is useful to also bring **all** values from another DataFrame even though there would not be a matching value in the column that used for making the join (i.e. the ``key``).

We can bring all the values from another DataFrame by specifyin parameter ``how='outer'``, i.e. we will make an **outer** join.
Let's consider another example with the outer join.

.. ipython:: python

    join2 = data1.merge(data2, on='Time', how='outer')
    join2

Cool! Nowe we have all the values included from both DataFrames and if Pandas did not find a common value in the ``key`` column, it still kept them and inserted ``NaN`` values into ``Favourite_dog`` column and ``Value`` column.
Overall, knowing how to conduct a table join can be really handy in many different situations.
See more examples and documentation from `official documentation of Pandas <https://pandas.pydata.org/pandas-docs/stable/merging.html>`__.

Breaking loops after a certain number of iterations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We had a question during the lesson about breaking out of a loop after a certain number of iterations.
As you may recall, the ``break`` can be used to exit a loop.
We provided examples of how to break out of a ``for`` loop after a single iteration, but what if you want to loop 5 times and then break?
This can be done by creating a counter variable (``count`` in this case) and using that to break after a certain number of iterations as follows:

.. ipython:: python

    # Initialize counter variable
    count = 0
    # Create a list of months
    months = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']
    # Loop over months and print them
    for month in months:
        print('The current month is', month)
        # Increment counter variable
        count = count + 1
        # Exit if the month counter equals 5
        if count == 5:
            break

As you can see, here our code will exit the loop when the month counter is equal to 5.
This can be a handy way to break after a fixed number of iterations.

Übung 7
=======

Ziel der Übung
--------------

-  Rasterdaten zuschneiden
-  Reliefanalysen durchführen
-  zonale Statistiken berechnen
-  Rasterdaten in Vektordaten umwandeln
-  ein Höhenprofil erstellen

Wiki:
-----

-  `Rasterdaten in Vektordaten
   umwandeln <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Konvertierung>`__
-  `fokale
   Rasteroperationen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Fokale-Funktionen>`__
-  `zonale
   Rasteroperationen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Zonale-Funktionen>`__
-  `weitere
   Rasteroperationen <https://courses.gistools.geog.uni-heidelberg.de/giscience/gis-einfuehrung/wikis/qgis-Weitere-Rasterfunktionen>`__

Daten
-----

Ladet euch die Daten vom USB-Stick und speichert sie auf eurem PC. Legt
einen lokalen Ordner an und speichert dort die obigen Daten. (.zip
Ordner müssen vorher entpackt werden.) \* Linien-Layer: trails (Quelle:
OpenRouteService, OpenStreetMap and Contributors) \* Polygon-Layer:
national_parks (Quelle: OpenStreetMap and Contributors) \* Raster-Layer:
ASTER Höhendaten (Quelle: METI/NASA)

Aufgaben
--------

Aufgabe 1: Vorbereitung
~~~~~~~~~~~~~~~~~~~~~~~

-  Bringt die Höhendaten in eine passende metrische Projektion (z.B. WGS
   84 / UTM 37N).
-  Schneidet (**Clip**) den Raster-Datensatz auf die Ausdehnung des
   Nationalpark-Layers zu.

Aufgabe 2: Reliefanalysen
~~~~~~~~~~~~~~~~~~~~~~~~~

-  Berechnet zunächst einen **Hillshade** für das Geländemodell. Tipp:
   Nutze die Processing - Toolbox, um Funktionen zu finden.
-  Ermittelt die Hangneigung in ° (via **Slope**).
-  Erstellt Übersichtsstatistiken für die beiden Nationalparks (bspw.
   mit Hilfe von **Zonal Statistics**).

   -  Was ist die maximale Hangneigung pro Nationalpark?
   -  Wie hoch ist die durchschnittliche Hangneigung pro Nationalpark?

-  Glättet euer Ergebnis in dem ihr pro Pixel den Durchschnitt der 11x11
   Nachbarschaft berechnet (via **r.neighbors**).
-  Selektiert besonders steile Regionen (>30°) (nutzt dazu zunächst den
   Raster Calculator oder das **Reclassify Tool**)
-  Konvertiert die Auswahl ins Vektorformat (**Conversion - Raster to
   Vector**). Anschließend kannst du das **Basic statistic per field**
   nutzen.

Aufgabe 3: Höhenprofil
~~~~~~~~~~~~~~~~~~~~~~

-  Erstellt für die Sirimon-Route im trails-Layer ein Höhenprofil.
-  Das Höhenprofil soll auf der x-Achse die Distanz in Meter zeigen &
   auf der y-Achse die Höhe ü.N.
-  Tipp: Achtet auf die einzelnen Schritte des Erklärvideos für das
   Plugin, was ihr hierfür nutzt. Kleinigkeiten können hier entscheidend
   sein.

Das könnte dann ungefähr so aussehen: |profile|

.. |profile| image:: sirimon_route_profile.png