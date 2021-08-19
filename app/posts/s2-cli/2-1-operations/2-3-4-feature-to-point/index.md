---
title: Feature to point
date: 2012-09-28
layout: post.html
---

- It gets the centroid for each feature in a GeoJSON file.

#### Return:

**GeoJSON file** - It contains the centroid of each feature.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    centroid input.geojson > output.geojson
```

#### Use case:

- Get the centroid of each feature of the input file.

![image](https://user-images.githubusercontent.com/11504548/129109435-509a8456-1cf0-4d83-b385-c3543472ab95.png)