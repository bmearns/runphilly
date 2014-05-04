runphilly
=========

Philadelphia parks, trails, and running site.


workflowy at: https://workflowy.com/#/015cd385-24dc-492d-ba98-2bc3894d0b44

Using the following dependecies on the front end:
leaflet
jquery
handlebars
json2

some backend commands
=========

..\tiles>gdal2tiles ..\runphilly\runphily.mbtiles


..\runphilly>ogr2ogr -f "GeoJSON" -overwrite -sql "SELECT * FROM trails" runphilly.js runphilly.sqlite

// ultimately had to write this, EPSG:3857 was not appearing on map, had to use WGS
..\runphilly>ogr2ogr -s_srs "EPSG:3857" -t_srs "EPSG:4326" -overwrite -f "GeoJSON" -overwrite -sql "SELECT * FROM trails" runphilly2.js runphilly.sqlite
