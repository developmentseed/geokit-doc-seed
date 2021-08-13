---
title: Line to polygon
date: 2012-09-28
layout: post.html
---

- It changes the type of geometry from LineString to Polygon.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    line2polygon input.geojson > output.geojson
```

#### Return:

**GeoJSON file** - It contains features with Polygon type.

#### Use case:

- Change a line to polygon.

![image](https://user-images.githubusercontent.com/11504548/46221217-1d1bf800-c312-11e8-9b75-5ba975460e1d.png)
