---
title: Filter by property
date: 2012-09-28
layout: post.html
---

- Filter features by property and will generate a new geojson file with the filtered objects.

#### Return:

**Geojson file** - all filtered objects.

#### Command line:

```geokit filterbyprop input.geojson --prop building=* > output.geojson```

#### Use case:

- From a set of different osm objects in a geojson file, filter only buildings.

![7](https://user-images.githubusercontent.com/11504548/44229508-e3c26b00-a15d-11e8-961a-f38fdf58bc4e.png)

