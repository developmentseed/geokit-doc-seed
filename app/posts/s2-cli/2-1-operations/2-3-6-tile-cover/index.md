---
title: Tile cover
date: 2012-09-28
layout: post.html
---

- It pass a polygon and get the tiles which cover all the polygon at a certain zoom level. From: <https://github.com/mapbox/tile-cover>.

#### Return:

**GeoJSON file** - It contains the tiles which cover all the given polygon.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    tilecover input.geojson --zoom=17 > output.geojson
```

#### Use case:

- Get the tiles which cover all the given polygon.

![image](https://user-images.githubusercontent.com/11504548/129234178-9b66e09a-5e4c-4eaa-9b24-91a27f692f8b.png)
