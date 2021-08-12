---
title: Feature to point
date: 2012-09-28
layout: post.html
---

- Gets the centroid for each features in a geojson file.

#### Return:

**Geojson file** - it contains the centroid of each features.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node geokit \
    centroid input.geojson > output.geojson
```

#### Use case:

- Gets the centroid of each features of the input file.

![Screenshot from 2021-08-11 17-03-11](https://user-images.githubusercontent.com/11504548/129109435-509a8456-1cf0-4d83-b385-c3543472ab95.png)