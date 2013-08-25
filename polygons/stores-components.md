Draw Polygons for Business Areas
================================

## Overview

Given a business location record, draw polygons indicating the business's building(s) and front parking lot. Also mark the approximate center of the business's primary buidling.

## Instructions

* Lookup the given business record in your mapping tool.
* Draw polygons around all business buildings. Name each building polygon "building".
* Draw a polygon around the business's front parking lot. Name the polygon "parking".
* Your polygons should represent the areas that we'd reasonably consider to be "at" the business. That is, if a person enters one of the polygons,
we'd consider them to likely be visiting the business.
* Mark the approximate "center" of the business's primary building. Imagine you're inside the building and you want to stay as far away
  from the outer walls as possible. Where would you stand? Use your mapping tool to set a marker on this spot.
* Do not zoom in so close that your mapping tool stops providing a straight-down view. It's important for accuracy that you have a straight-down view while drawing the polygon.
* Please use your best human judgment when identifying business building(s) and the front parking lot.
* Once you are satisfied with your polygons and center marker, export your work as a KML file and send it to us.
* Please create exactly 1 KML file per business.

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

See the example screenshot below to see an example of polygons drawn for this business.

### KML File Requirements

Your KML file should include the polygons and the center marker for the business, but no other polygons or markers.

It should be named __[FACTUAL_ID].kml__, where FACTUAL_ID is the **factual_id** from the business record. Here is an example file name:
`66f9c859-5532-4ee1-85c2-fbbb3b88692d.kml`.

The contents of the KML file should include multiple Placemarks: One for each polygon, and one that contains a Point that represents your center marker.

The Placemarks for the business building(s) should contain a name with the value set to "building". E.g.:
```xml
<Placemark>
  <name>building</name>
```

The Placemark for the front parking lot should contain a name, with the value set to "parking". E.g.:
```xml
<Placemark>
  <name>parking</name>
```

This should be included for you automatically when you export your work as a KML file. You should never edit a KML file by hand.

For a detailed illustration, see this [example KML file](https://raw.github.com/Factual/public-works/master/polygons/examples/stores-components/66f9c859-5532-4ee1-85c2-fbbb3b88692d.kml).
It was created for the example business record above.

## Checking your KML Files

You can double check your KML files by using Google's Maps Engine. Maps Engine allows you to
draw polygons over a satellite map view and export to KML, and so it's also possible to view a
KML file using Maps Engine.

Instructions for importing and viewing a KML file can be found here:
http://www.askdavetaylor.com/how_to_import_xml_kml_data_file_google_maps.html

If you're able to import and view your KML files in this way, you can be reasonably certain that we can as well.

Here is a screenshot taken after importing the KML file from the example above:
![Example Polygon drawing](https://github.com/Factual/public-works/raw/master/polygons/examples/stores-components/66f9c859-5532-4ee1-85c2-fbbb3b88692d.png)
