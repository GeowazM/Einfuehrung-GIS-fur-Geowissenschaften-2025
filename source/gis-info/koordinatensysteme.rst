Koordinatensysteme
==================

Jeder Layer sollte ein Koordinatensystem besitzen, d.h. jeder Geodatensatz befindet ich in einem definiertem Koordinatensystem. In
QGIS werden alle Layer eines Projektes in der Kartenansicht im selben Koordinatensystem dargestellt.

Dieses Projekt Koordinatensystem kann unabhängig vom Koordinatensystem der Layer gewählt werden. Falls das Projekt-Koordinatensystem und das
Koordinatensystem der Layer nicht übereinstimmen, werden die Layer on-the-fly umprojiziert. Diese on-the-fly Umprojektion verändert aber
nicht permanent das Koordinatensystem des Datensatzes, sondern nur kurzfristig seine **Darstellung** und ggfs. die Ergebnisse von Längen-,
Fläche- und Winkelberechnungen. Bei der Arbeit in QGIS ist es zu empfehlen die Layer und die darin enthaltenen Daten langfristig umzuprojizieren.

Zur Kommunikation von Koordinatensysteme existieren zwei Formate: PROJ (auch ein Softwareprogramm) & WKT (auch WKT-CRS genannt). Beide sind
durch das OGC anerkannt und alle gängigen Kartographie und GIS Softwares können damit umgehen. 

Beispiel **EPSG:4326**

.. raw:: html

   <details>

.. raw:: html

   <summary>

WKT

.. raw:: html

   </summary>

::

   GEOGCS["WGS 84",
       DATUM["WGS_1984",
           SPHEROID["WGS 84",6378137,298.257223563,
               AUTHORITY["EPSG","7030"]],
           AUTHORITY["EPSG","6326"]],
       PRIMEM["Greenwich",0,
           AUTHORITY["EPSG","8901"]],
       UNIT["degree",0.0174532925199433,
           AUTHORITY["EPSG","9122"]],
       AUTHORITY["EPSG","4326"]]

.. raw:: html

   </details>

.. raw:: html

   <details>

.. raw:: html

   <summary>

PROJ

.. raw:: html

   </summary>

::

   +proj=longlat +datum=WGS84 +no_defs +type=crs

.. raw:: html

   </details>

Beispiel **EPSG:32634**

.. raw:: html

   <details>

.. raw:: html

   <summary>

WKT

.. raw:: html

   </summary>

::

   PROJCS["WGS 84 / UTM zone 34N",
       GEOGCS["WGS 84",
           DATUM["WGS_1984",
               SPHEROID["WGS 84",6378137,298.257223563,
                   AUTHORITY["EPSG","7030"]],
               AUTHORITY["EPSG","6326"]],
           PRIMEM["Greenwich",0,
               AUTHORITY["EPSG","8901"]],
           UNIT["degree",0.0174532925199433,
               AUTHORITY["EPSG","9122"]],
           AUTHORITY["EPSG","4326"]],
       PROJECTION["Transverse_Mercator"],
       PARAMETER["latitude_of_origin",0],
       PARAMETER["central_meridian",21],
       PARAMETER["scale_factor",0.9996],
       PARAMETER["false_easting",500000],
       PARAMETER["false_northing",0],
       UNIT["metre",1,
           AUTHORITY["EPSG","9001"]],
       AXIS["Easting",EAST],
       AXIS["Northing",NORTH],
       AUTHORITY["EPSG","32634"]]

.. raw:: html

   </details>

.. raw:: html

   <details>

.. raw:: html

   <summary>

PROJ

.. raw:: html

   </summary>

::

   +proj=utm +zone=34 +datum=WGS84 +units=m +no_defs +type=crs

.. raw:: html

   </details>

Projektkoordinatensystem
------------------------

Ändern des Projektkoordinatensystem
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/changeProjectProjection.mp4">

.. raw:: html

   </video>

Benutzerdefinierte Projektion
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Man kann auch eigene Koordinatensysteme definieren. I.d.R. auf Basis
existierender Koordinatensysteme, deren Parameter (z.B. Schnittpunkte
oder Schnittkreise so wählen, dass die darzustellende Region möglichst
wenig verzerrt wird).

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/customProjection.mp4">

.. raw:: html

   </video>

Layerkoordinatensystem
----------------------

Welches Koordinatensystem ist im Layer definiert?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Über die Layer Metadaten können sie dessen Koordinatensystem überprüfen.

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/kbs-metadaten.mp4">

.. raw:: html

   </video>

Koordinatensystem eines Layers ändern
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Vektordaten
^^^^^^^^^^^

Liegen die Daten im Vektorformat vor (Punkte, Linien, Polygone), dann
kann man ihr Koordinatensystem über ``Vektor`` >
``Datenmanagement-Werkzeuge`` > ``Layer umprojizieren`` verändern.

Die Daten werden mit diesem Werkzeug umprojiziert und es wird ein neues
Layer mit den veränderten Daten ausgegeben.

.. raw:: html

   <video width="100%" controls src="https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/videos/kbs-vektor.mp4">

.. raw:: html

   </video>

Rasterdaten
^^^^^^^^^^^

Liegen die Daten im Rasterdatenformat vor, dann kann man ihr
Koordinatensystem über ``Raster`` > ``Projektionen`` >
``Transformieren (Reprojizieren)`` verändern.

Projection Wizard
=================

Um ein passendes Koordinatensystem für einen bestimmten Anwendungszweck
und Ausschnitt der Erde zu finden, gibt es den *Projection Wizard* unter
`projectionwizard.org <https://projectionwizard.org/>`__.

Auf dieser Webseite könnt ihr den Ausschnitt in dem sich eure Karte
befindet auswählen und unter *Distortion Property* festlegen ob die
Projektion flächentreu (equal-area), winkeltreu (conformal), längentreu
(equidistant) oder ein Kompromiss aus allen drei (compromise) sein soll.

.. figure:: https://courses.gistools.geog.uni-heidelberg.de/giscience/kartographie_uebung/-/wikis/uploads/img/projwiz-distortion.png
   :alt: projwiz-distortion.png

   projwiz-distortion.png

Die Webseite gibt euch dann Vorschläge, welches Koordinatensystem euren
Anforderungen am besten entspricht und bietet sie sowohl im PROJ und WKT
Format an.

Der Projection Wizard liefert die besten Ergebnisse für große Maßstäbe
und Karten über Ländergrenzen hinweg. Für kleinere Maßstäbe bietet es
sich an, das offizielle Koordinatensystem des jeweiligen Staats zu
benutzen.
