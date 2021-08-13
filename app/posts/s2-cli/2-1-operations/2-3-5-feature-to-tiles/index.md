---
title: Feature to tiles
date: 2012-09-28
layout: post.html
---

- It pass a GeoJSON file with points and gets the nearest tiles to this points.

#### Return:

**GeoJSON file** - It contains the nearest tiles to the points.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    point2tile input.geojson --zoom=17 --buffer=0.2 --copyattrs=true > output.geojson
```

#### Use case:

- Get the nearest tiles to the points.

![image](https://user-images.githubusercontent.com/11504548/129229601-6d4c2f13-acaa-434b-8cc0-acfb6c2c2549.png)