Acetate
=======

Acetate is a set of stylesheets that are designed specifically for geographic data visualization. It includes several layers: topographic basemap, hillshading, roads, placenames. These layers can be used individually in combination in layering with thematic data, or composited together into a single image.

![](https://cloud.githubusercontent.com/assets/1218/22753542/77ec9a3e-ee0a-11e6-96c8-1bc252471f37.png)

Using Acetate
=============

You can use Acetate tile layers by using the following template urls in a web map

- Basemap ([preview](http://acetate.geoiq.com/tiles/acetate-base/preview.html))
 - http://acetate.geoiq.com/tiles/acetate-simple/{Z}/{X}/{Y}.png
- Basemap, Hillshading ([preview](http://acetate.geoiq.com/tiles/terrain/preview.html))
 - http://acetate.geoiq.com/tiles/terrain/preview.html
- Basemap, Hillshading, Placename labels ([preview](http://acetate.geoiq.com/tiles/acetate-hillshading/preview.html))
 - http://acetate.geoiq.com/tiles/acetate-hillshading/{Z}/{X}/{Y}.png
- Roads, Placename labels ([preview](http://acetate.geoiq.com/tiles/acetate-fg/preview.html))
 - http://acetate.geoiq.com/tiles/acetate-fg/{Z}/{X}/{Y}.png
- Roads ([preview](http://acetate.geoiq.com/tiles/acetate-roads/preview.html))
 - http://acetate.geoiq.com/tiles/acetate-roads/{Z}/{X}/{Y}.png
- Placename labels ([preview](http://acetate.geoiq.com/tiles/acetate-labels/preview.html))
 - http://acetate.geoiq.com/tiles/acetate-labels/{Z}/{X}/{Y}.png
- Hillshading ([preview](http://acetate.geoiq.com/tiles/hillshading/preview.html))
 - http://acetate.geoiq.com/tiles/hillshading/{Z}/{X}/{Y}.png

Building Tiles
==============

Acetate is built upon the Tilestache, Mapnik projects and it uses a combination of PostGIS and Shapefiles to store spatial data. The data used is OpenStreetMap, Natural Earth and some custom data sources.  The two custom data sources are created through a process of “simulated annealing.”

Data Needed
-----------

In order to get started with the data install PostGIS and download the OpenStreetMap Planet File.  You’ll need to use OSM2PGSQL to import it.  The process of importing for the whole world can take a while, if you only need a specific country you might want to grab a country specific extract from GeoFabrik.  To get the coastline information you’ll need to get the data from Natural Earth.

The custom data is for place names and simplified motorways.  You can download the place name shapefiles from here.  The simplified motorways is a SQL script that should be run after the OSM Planet is imported.

Software Needed
---------------

To get yourself going install [Tilestache](https://github.com/migurski/TileStache) from Github.  From the README Mapnik is listed as an optional dependency but for our purposes you need it.

At the moment we give you all the pieces to roll your own, though look for a full tutorial in the coming weeks.

Installing Acetate
------------------

This step is about just placing the acetate project into a web accessible place. Drop them the project into a web dir and start making tiles.

License
=======

Acetate is released under a [Creative Commons Attribution-ShareAlike 2.5 Generic (CC BY-SA 2.5)](http://creativecommons.org/licenses/by-sa/2.5/) license. It was developed by [FortiusOne](http://www.fortiusone.com/ "FortiusOne Visual Intelligence Solutions | Visual Intelligence, Smarter Decisions") and [Stamen](http://stamen.com/ "stamen design | big ideas worth pursuing").
