---
title: Area
date: 2012-09-28
layout: post.html
---

- It gets the total area in km² of Polygon and MultiPolygon features that there are in a GeoJSON file.

#### Return:

**Number** - total area in km².

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    area input.geojson
```

### Use Case:

- Get the total area in km² of the all polygons.

![image](https://user-images.githubusercontent.com/19536044/46107317-a57a8b80-c1a0-11e8-8e5a-0509ec7ad8ed.png)