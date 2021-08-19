---
title: GeoJSON to poly
date: 2012-09-28
layout: post.html
---

- It converts GeoJSON polygons to OpenStreetMap (OSM) poly format file.

#### Return

**poly file** - it contains the polygon in poly format file.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    geojson2poly input.geojson output.poly
```

#### Use case:
- Convert a polygon from GeoJSON to poly format file.

![image](https://user-images.githubusercontent.com/19536044/47043059-4a5e0800-d152-11e8-9cc7-bc17ea7db362.png)
