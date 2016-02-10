# Styles QGIS pour les données OpenStreetMap

Les styles sont à utiliser dans le logiciel QGIS sur des données OpenStreetMap.

Les données OSM doivent contenir des champs définis sur la base des clés des entités.

Le choix des champs/clés retenus est géré grâce à la configuration du pilote OGR à l'aide du fichier **_osmconf.ini_**. L'objectif est d'éviter d'utiliser le champ *other_tag* qui est délicat à manipuler. Il faut donc prendre le temps de paramétrer le fichier osmconf.ini mais les règles de symbologie de QGIS sont ensuite plus simple à créer.

N'hésitez pas à faire savoir quelles clés suplémentaire vous semblent importantes à ajouter à 

Attention, les styles proposés ne peuvent probablement pas s'appliquer aux données shapefile récupérées sur GeoFabrik. De même, les styles proposés par d'autres ne fonctionneront probablement plus du fait de la disparition d'informations dans le champ *other_tag*. Penser donc à sauvegarder la version originale de votre fichier _osmconf.ini_.

sudo gedit /usr/share/gdal/1.11/osmconf.ini

Pour récupérer les styles pensez à utiliser le bouton Download ZIP situé à droite.

In case of problems with labeling, there is a workaround here : https://hub.qgis.org/issues/13667
