---
title: Set bbox on each feature
date: 2012-09-28
layout: post.html
---

- Gets the bbox of each feature in a geojson file and add it as a attribute.

#### Return:

**Geojson file** - it contains features with a `bbox` attribute.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node geokit \
    featurebbox input.geojson > output.geojson
```

#### Use case:

- Sets the bbox on each feature.

![Screenshot from 2021-08-11 15-42-58](https://user-images.githubusercontent.com/11504548/129100425-a83e3948-189c-4af5-bae5-4c2cd0943f2b.png)
