Draw Airport Polygon
====================

## Overview

Given an airport location record, provide the polygon surrounding the airport area including terminals, runways, and parking.
Also mark the approximate center of the main airport terminal structure.

## Instructions

* Lookup the given airport record in your mapping tool.
* Draw a polygon around the airport's terminals, runways, and parking.
* This polygon should represent the area that we'd reasonably consider to be "at" the airport. That is, once a person were to enter the polygon, we'd consider them to most likely be visiting the airport.
* Please use your overall best human judgment when identifying airport parking lot and runways.
* Mark the approximate "center" of the main airport terminal structure.
* Once you are satisfied with your polygon and center marker, export your work as a KML file and send it to us.

### Example Airport Record

This is an example business record, representing an airport in Bristol, Great Britain:

```json
{"factual_id":"f51030e5-f824-44bf-96d1-ae0f7b1c26cc",
 "name":"Bristol Airport (BRS)",
 "locality":"Bristol",
 "region":"Bristol",
 "country":"gb",
 "latitude":51.38278,
 "longitude":-2.719167}
```

See the example screenshot below to see an example of a polygon for this airport.

### KML File Requirements

Your KML file should include the polygon and the center marker for the airport, but no other polygons or markers.

It should be named __[FACTUAL_ID].kml__, where FACTUAL_ID is the **factual_id** from the business record. Here is an example file name:
`f51030e5-f824-44bf-96d1-ae0f7b1c26cc.kml`.

The contents of the KML file should include two Placemarks: One that contains your Polygon, including the set of coordinates for the polygon, and one that contains a Point that represents your center marker, including a small set of coordinates for the marker.

This [example KML file](https://raw.github.com/Factual/public-works/master/polygons/examples/airports/f51030e5-f824-44bf-96d1-ae0f7b1c26cc.kml)
was drawn for the example business record above.

## Checking your KML Files

You can double check your KML files by using Google's Maps Engine. Maps Engine allows you to
draw polygons over a satellite map view and export to KML, and so it's also possible to view a
KML file using Maps Engine.

Instructions for importing and viewing a KML file can be found here:
http://www.askdavetaylor.com/how_to_import_xml_kml_data_file_google_maps.html

If you're able to import and view your KML files in this way, you can be reasonably certain that we can as well.

Here is a screenshot taken after importing the KML file from the example above:
![Example Polygon drawing](https://github.com/Factual/public-works/raw/master/polygons/examples/airports/f51030e5-f824-44bf-96d1-ae0f7b1c26cc.png)