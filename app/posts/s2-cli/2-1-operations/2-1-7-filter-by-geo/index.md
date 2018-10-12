---
title: Filter by geometry
date: 2012-09-28
layout: post.html
---

- Filters features by given geometry and will generate a new geojson file with the filtered features.

#### Return:

**Geojson file** - it contains all filtered features.

#### Command line:

```geokit filterbygeometry input.geojson --geos LineString > output.geojson```

#### Use case:

- From a set of different types of features in a geojson file, filter only LineString type.

![filtergeo](https://user-images.githubusercontent.com/11504548/46836199-27a8a980-cd76-11e8-8ed2-247e0bef7f69.png)
