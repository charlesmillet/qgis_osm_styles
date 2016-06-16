# Styles QGIS pour les données OpenStreetMap

Ce projet propose des styles QGIS généralement adaptés à des données OpenStreetMap. Pour fonctionner correctement les données OSM doivent contenir des champs définis sur la base des clés des entités.

Le choix des champs/clés retenus est géré grâce à la configuration du pilote OGR à l'aide du fichier **_osmconf.ini_**. L'objectif est d'éviter d'utiliser le champ *other_tag* qui est délicat à manipuler. Il faut donc prendre le temps de paramétrer le fichier _osmconf.ini_ mais les règles de symbologie de QGIS sont ensuite plus simple à créer. Pour chaque jeu de styles, un fichier _osmconf.ini_ pré-configuré est fourni.

N'hésitez pas à faire savoir quelles clés suplémentaire vous semblent importantes à ajouter.

Attention, les styles proposés ne peuvent probablement pas s'appliquer aux données shapefile récupérées sur GeoFabrik. De même, les styles proposés par d'autres ne fonctionneront probablement plus du fait de la disparition d'informations dans le champ *other_tag*. Penser donc à sauvegarder la version originale de votre fichier _osmconf.ini_ ou à utiliser un fichier de configuration à part.

Pour modifier le fichier de configuration sous Ubuntu

    sudo gedit /usr/share/gdal/1.11/osmconf.ini

Pour la conversion avec _ogr2ogr_

    ogr2ogr -overwrite -f "SQLite" -dsco SPATIALITE=YES tours.sqlite tours.osm --config OSM_CONFIG_FILE osmconf.ini

Pour récupérer les styles pensez à utiliser le bouton Download ZIP situé à droite.

En cas de problèmes avec les étiquettes (_labels_) il y a une solution ici : https://hub.qgis.org/issues/13667
