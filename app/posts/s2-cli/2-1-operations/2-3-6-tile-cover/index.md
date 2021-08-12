---
title: Tile cover
date: 2012-09-28
layout: post.html
---

- Pass a polygon and get the tiles which cover all the polygon at a certain zoom. From: https://github.com/mapbox/tile-cover

#### Return:

**Geojson file** - it contains the tiles which cover all the polygon.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node geokit \
    tilecover input.geojson --zoom=17 > output.geojson
```

#### Use case:

- Gets the tiles which cover all the given polygon.

![Screenshot from 2021-08-12 11-34-23](https://user-images.githubusercontent.com/11504548/129234178-9b66e09a-5e4c-4eaa-9b24-91a27f692f8b.png)
