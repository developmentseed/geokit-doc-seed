---
title: Set bbox on each feature
date: 2012-09-28
layout: post.html
---

- It gets the bbox of each feature in a GeoJSON file and add it as a attribute.

#### Return:

**GeoJSON file** - It contains features with a `bbox` attribute.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    featurebbox input.geojson > output.geojson
```

#### Use case:

- Set the bbox attribute on each feature in the input file.

![image](https://user-images.githubusercontent.com/11504548/129100425-a83e3948-189c-4af5-bae5-4c2cd0943f2b.png)
