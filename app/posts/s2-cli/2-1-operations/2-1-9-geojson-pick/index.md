---
title: Geojson pick
date: 2012-09-28
layout: post.html
---

- Removes all but specified properties from features in a FeatureCollection.

#### Return:

**Geojson file** - it contains all features only with the specified properties.

#### Command line:

```geojson-pick PROPERTYNAME1 < input.geojson > output.geojson```

#### Use case:

- Remove all the attributes except `tileid`.

![image](https://user-images.githubusercontent.com/19536044/47043335-00c1ed00-d153-11e8-9e38-20c8b4830184.png)
