# TMS Tiles to XYZ
Use TMS tiles generated from *gdal2tiles.py* to XYZ tiles (default tiles for OSM and other services).

- d[2] is zoom level
- d[0] is sublevel
- 1 << d[2]) - d[1] - 1 is tile name.

Which gives : 

`.attr("xlink:href", function(d) {return "pathToTiles/" + d[2] + "/" + d[0] + "/" +   ((1 << d[2]) - d[1] - 1) + ".png";}`)
