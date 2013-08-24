Draw Business Polygon
=====================

## Overview

Given a business location record, provide the polygon surrounding the business location and its front parking lot. Also mark the approximate center of the business buidling.

## Instructions

* Lookup the given business record in your mapping tool.
* Draw a polygon around the business's physical building and front parking lot.
* This polygon should represent the area that we'd reasonably consider to be "at" the business. That is, once a person were to walk into the polygon, we'd consider them to most likely be visiting the place of business.
* Please use your overall best human judgment when identifying the front parking lot.
* Mark the approximate "center" of the business's building. Imagine you're inside the building and you want to stay as far away
  from the outer walls as possible. Where would you stand? Use your mapping tool to set a marker on this spot.
* Once you are satisfied with your polygon and center marker, export your work as a KML file and send it to us.

### Example Business Record

This is an example business record, representing a Walgreens drug store in Century City, CA:

```json
{"factual_id":"66f9c859-5532-4ee1-85c2-fbbb3b88692d",
 "name":"Walgreens",
 "address":"10407 Santa Monica Blvd",
 "locality":"Los Angeles",
 "region":"CA",
 "latitude":34.057509,
 "longitude":-118.424559}
```

See the example screenshot below to see an example of a polygon for this business.

### KML File Requirements

Your KML file should include the polygon and the center marker for the business, but no other polygons or markers.

It should be named __[FACTUAL_ID].kml__, where FACTUAL_ID is the **factual_id** from the business record. Here is an example file name:
`66f9c859-5532-4ee1-85c2-fbbb3b88692d.kml`.

The contents of the KML file should include two Placemarks: One that contains your Polygon, including the set of coordinates for the polygon, and one that contains a Point that represents your center marker, including a small set of coordinates for the marker.

This [example KML file](https://raw.github.com/Factual/public-works/master/polygons/examples/stores/66f9c859-5532-4ee1-85c2-fbbb3b88692d.kml)
was drawn for the example business record above.

## Checking your KML Files

You can double check your KML files by using Google's Maps Engine. Maps Engine allows you to
draw polygons over a satellite map view and export to KML, and so it's also possible to view a
KML file using Maps Engine.

Instructions for importing and viewing a KML file can be found here:
http://www.askdavetaylor.com/how_to_import_xml_kml_data_file_google_maps.html

If you're able to import and view your KML files in this way, you can be reasonably certain that we can as well.

Here is a screenshot taken after importing the KML file from the example above:
![Example Polygon drawing](https://github.com/Factual/public-works/raw/master/polygons/examples/stores/66f9c859-5532-4ee1-85c2-fbbb3b88692d.png)
