Draw Polygons for Business and Parking
======================================

## Overview

Provide a polygon around the business entity and its official parking lot(s). If a person were to walk into that polygon, it means they are visiting that business.

Also mark the approximate "center" of the primary business building.

## Detailed instructions

* Draw a polygon around the business's physical building and front parking lot.
* Please use your overall best human judgment when identifying the front parking lot.
* Mark the approximate "center" of the business's building. Imagine you're inside the building and you want to stay as far away
  from the outer walls as possible. Where would you stand? Use your mapping tool to set a marker on this spot.
* Once you are satisfied with your polygon and center marker, export your work as a KML file.
* The export should include the polygon and the center marker for the business, but no other polygons or markers.
* The export should be named [FACTUAL_ID].kml, where FACTUAL_ID is the "factual_id" from the business record. Example file name: `21234482-efe6-42e3-902b-cb88378c5ea9.kml`

## KML File Format

The KML file should include two Placemarks. One should contain your Polygon, including the set of coordinates for the polygon.
The other will contain a Point that represents your center marker, including a small set of coordinates for the marker.

[Example KML file](https://raw.github.com/Factual/public-works/master/polygons/building_and_parking/examples/stores/66f9c859-5532-4ee1-85c2-fbbb3b88692d.kml)

## Example Polygon Drawing

![An example Polygon drawing](https://github.com/Factual/public-works/raw/master/polygons/building_and_parking/examples/stores/66f9c859-5532-4ee1-85c2-fbbb3b88692d.png)

The above was drawn for this record:

```json
{"factual_id":"66f9c859-5532-4ee1-85c2-fbbb3b88692d",
  "name":"Walgreens",
  "address":"10407 Santa Monica Blvd",
  "locality":"Los Angeles",
  "region":"CA",
  "latitude":34.057509,
  "longitude":-118.424559}
```

## Checking your KML Files

You can double check your KML files by using Google's Maps Engine. Maps Engine allows people to
draw polygons over a satellite map view and export to KML, and so it's also possible to view a
KML file using Maps Engine.

Instructions for importing and viewing a KML file can be found here:
http://www.askdavetaylor.com/how_to_import_xml_kml_data_file_google_maps.html

If you're able to import and view your KML files in this way, you can be reasonably certain that we can as well.
