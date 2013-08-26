Draw Airport Polygons
=====================

## Overview

Given an airport location record, draw polygons indicating the airport's parking lots and
terminal & runway areas.

Also mark the approximate center of the main airport terminal structure.

The main goal is to identify the areas that are "at" the airport. Meaning, if a person is inside
 one of the polygons, we can reasonably consider them to be visiting this airport.

## Instructions

* Lookup the given airport record in your mapping tool.
* Draw one ore more polygons around the airport's terminals and runways (the general airport area excluding parking lots).
Name the polygons "airport".
* Draw one or more polygons around the airport parking areas. Name the polygons "parking".
* Your polygons should represent the areas that we'd reasonably consider to be "at" the airport.
  That is, if a person enters one of the polygons, we'd consider them to likely be visiting the airport.
* Mark the approximate "center" of the main airport terminal structure.
* Do not zoom in so close that your mapping tool stops providing a straight-down view. It's important for accuracy that you have a straight-down view while drawing the polygon.
* Please use your best human judgment when identifying airport terminals, parking lots, and runways.
* Once you are satisfied with your polygon(s) and center marker, export your work as a KML file.
* Please create exactly 1 KML file per airport.

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

Your KML file should include all the polygons you drew for the airport, plus the center marker.
Your KML file should not contain any other polygons or markers.

It should be named __[FACTUAL_ID].kml__, where FACTUAL_ID is the **factual_id** from the business record. Here is an example file name:
`f51030e5-f824-44bf-96d1-ae0f7b1c26cc.kml`.

The contents of the KML file should include multiple Placemarks: One for each polygon, and
one that contains a Point that represents your center marker.

The Placemarks for the airport terminals and runways should contain a name with the value
 set to "airport". E.g.:
```xml
<Placemark>
  <name>airport</name>
```

The Placemarks for the parking lots should each contain a name, with the value set to "parking". E.g.:
```xml
<Placemark>
  <name>parking</name>
```

This should be included for you automatically when you export your work as a KML file.
You should never edit a KML file by hand.

For a detailed illustration, see this [example KML file](https://raw.github.com/Factual/public-works/master/polygons/examples/airports-components/f51030e5-f824-44bf-96d1-ae0f7b1c26cc.kml).
It was created for the example airport record above.

Please do not send us files of any other format, such as KMZ. We only want KML files.

## Checking your KML Files

You can double check your KML files by using Google's Maps Engine. Maps Engine allows you to
draw polygons over a satellite map view and export to KML, and so it's also possible to view a
KML file using Maps Engine.

Instructions for importing and viewing a KML file can be found here:
http://www.askdavetaylor.com/how_to_import_xml_kml_data_file_google_maps.html

If you're able to import and view your KML files in this way, you can be reasonably certain that we can as well.

Here is a screenshot taken after importing the KML file from the example above:
![Example Polygon drawing](https://github.com/Factual/public-works/raw/master/polygons/examples/airports-components/f51030e5-f824-44bf-96d1-ae0f7b1c26cc.png)

## FAQ

**Q:** What should I mark as the center if the airport has multiple terminals?<br>
**A:** Please mark the center of the terminal which is most likely the airport's primary terminal.

**Q:** How should I handle areas that look like airport expansions that were under construction at the time the satellite image was taken?<br>
**A:** Please include those areas. Your polygon should include areas that you're reasonably confident are now, or will soon be, a working part of the airport.
