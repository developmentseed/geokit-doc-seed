---
title: Filter by property
date: 2012-09-28
layout: post.html
---

- Filters features by given property and will generate a new geojson file with the filtered features.

#### Return:

**Geojson file** - it contains all filtered features.

#### Command line:

```geokit filterbyprop input.geojson --prop building=* > output.geojson```

#### Use case:

- From a set of different features in a geojson file, filter only buildings.

![14](https://user-images.githubusercontent.com/11504548/46221600-63be2200-c313-11e8-9f23-e6d3d86767dd.png)
