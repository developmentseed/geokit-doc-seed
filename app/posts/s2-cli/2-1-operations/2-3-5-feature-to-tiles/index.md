---
title: Feature to tiles
date: 2012-09-28
layout: post.html
---

- Pass a geojson with points and get the nearest tiles to this point in a geojson file.

#### Return:

**Geojson file** - it contains the nearest tiles to the points

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node geokit \
    point2tile input.geojson --zoom=17 --buffer=0.2 --copyattrs=true > output.geojson
```

#### Use case:

- Gets the nearest tiles to the points.

![Screenshot from 2021-08-12 11-01-55](https://user-images.githubusercontent.com/11504548/129229601-6d4c2f13-acaa-434b-8cc0-acfb6c2c2549.png)