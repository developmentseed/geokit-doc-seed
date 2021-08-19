---
title: Merge GeoJSON files
date: 2012-09-28
layout: post.html
---

- It merges multiple GeoJSON files into one FeatureCollection.

#### Return:

**GeoJSON file** - It contains all features.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest \
    geojson-merge input1.geojson input2.geojson > output.geojson
```

#### Use case:

- Merge two or more GeoJSON files.

![image](https://user-images.githubusercontent.com/19536044/47046277-61085d00-d15a-11e8-965f-872632bffa8b.png)

