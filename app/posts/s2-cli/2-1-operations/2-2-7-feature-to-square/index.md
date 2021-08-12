---
title: Features to square
date: 2012-09-28
layout: post.html
---

- Creates features' square for a given radius in meters, in case of Polygon and LineString the script takes the centroid to generate the square.

#### Return:

**Geojson file** - it contains squares per each feature of the input file.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node geokit \
    fc2square input.geojson --radius=<number>  > output_square.geojson
```

#### Use case:

- Get a square, according the given radius, of each feature.

![Screenshot from 2021-08-11 15-14-18](https://user-images.githubusercontent.com/11504548/129096854-bd55ed43-8f6a-44c9-aa32-6ede7d31d025.png)