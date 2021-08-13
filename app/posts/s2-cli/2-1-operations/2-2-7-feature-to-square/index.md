---
title: Features to square
date: 2012-09-28
layout: post.html
---

- It creates features' square for a given radius in meters, in case of Polygon and LineString the script takes the centroid to generate the square.

#### Return:

**GeoJSON file** - It contains squares per each feature of the input file.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    fc2square input.geojson --radius=<number>  > output_square.geojson
```

#### Use case:

- Get a square, according the given radius, of each feature.

![image](https://user-images.githubusercontent.com/11504548/129096854-bd55ed43-8f6a-44c9-aa32-6ede7d31d025.png)