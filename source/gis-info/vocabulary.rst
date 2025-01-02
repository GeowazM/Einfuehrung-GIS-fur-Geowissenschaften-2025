Glossary
========

GIS Vokabular
-----------------

.. todo::

    Falls Sie bestimmte Begriffe hier nicht finden sollten, dann teilen Sie dies dem Dozierenden gerne mit.

Hier finden Sie eine Liste von Begriffen, die im Zusammenhang mit Geodaten und Geographischen Informationssystemen (GIS) immer wieder auftreten.

.. glossary::

  Algorithmus
     Ein Algorithmus im Geodatenbereich ist ein mathematisches Verfahren, das in einer Reihe von Schritten Probleme löst und häufig als Abfolge von Computerbefehlen codiert wird. 
     Diese Algorithmen werden in geografischen Informationssystemen (GIS) verwendet, um verschiedene Aufgaben zu bewältigen, wie z.B. die Umwandlung physischer Adressen in geografische Koordinaten (Geokodierung) oder 
     die Analyse räumlicher Daten.

     *Das Clip tool in QGIS ist hierfür ein Beispiel.*
   
  Datentyp
     An attribute defining the characteristics of a value in a program. For example, type `int` is an integer (whole number).

     *Definition to be given in Finnish.*

  Geodaten
     Geodaten beinhalten räumliche Informationen in Form von Koordinaten wie bspw. die Position einer Stadt auf der Erde.

     *Vektor- oder Rasterdaten.*

  Georeferenzieren
     A number indicating the location of a specific value stored in Python lists or tuples. The first index value of list is always ``0``.

     *Definition to be given in Finnish.*

   Open Geospatial Consortium
      Das Open Geospatial Consortium (OGC) ist eine internationale, freiwillige Konsens-Standardsorganisation, die sich auf die Entwicklung und Pflege von Standards für geospatiale Inhalte und ortsbezogene Dienste spezialisiert hat. 
      Gegründet 1994, fördert das OGC die Interoperabilität zwischen verschiedenen geospatialen Technologien und Systemen.

      *Dateiformate wie Shapefile oder Geojson.*

  Rasterdaten
     Geodaten die flächenhafte Objekte darstellen. Räumlcihe Rasterdateien werden oft als Geotif (``.tif``) gespeichert.

     *Landbedeckung, Temperaturen oder Geländehöhen.*

  Vektordaten
     Geodaten die Punkte, Linien oder Flächen repräsentieren. Räumliche Vektordateien werden oft als Shapefile (``.shp``), Geopackage (``.gpk``) oder Geojson (``.geojson``) gespiechert.

     *Stadt, Fluss oder ein Bundesland.*

- **Datentypen**

   - Integer (int) = Ganze Zahl

   - Float (float) = Dezimalzahl

   - String (str) = Text

   - Boolean (bool) = True / False

   - Date (date) = Datum


Basic vocabulary of Version Control
-----------------------------------

Few basic terms that are used often when discussing about version
control (not exhaustive).

.. glossary::

  Repository
     A location where all the files for a particular project are stored, usually abbreviated to “repo.”
     Each project will have its own repo, which is usually located on a server and can be accessed by a unique URL (a link to GitHub page for example).


-  **Commit** = To commit is to write or merge the changes made in the
   working copy back to the repository. Whe you commit, you are
   basically taking a “snapshot” of your repository at that point in
   time, giving you a checkpoint to which you can reevaluate or restore
   your project to any previous state. The terms 'commit' or 'checkin'
   can also be used as nouns to describe the new revision that is
   created as a result of committing.

-  **Revision / version** = A revision or a version is any change in
   made in any form to a document(s).

-  **Clone** = Cloning means creating a repository containing the
   revisions from another repository. This is equivalent to pushing or
   pulling into an empty (newly initialized) repository. As a noun, two
   repositories can be said to be clones if they are kept synchronized,
   and contain the same revisions.

-  **Pull / push** = Copy revisions from one repository into another.
   Pull is initiated by the receiving repository, while push is
   initiated by the source. Fetch is sometimes used as a synonym for
   pull, or to mean a pull followed by an update.

-  **Merge** = A merge or integration is an operation in which two sets
   of changes are applied to a file or set of files.
