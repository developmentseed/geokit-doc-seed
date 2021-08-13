---
title: Delete nulls
date: 2012-09-28
layout: post.html
---

- It deletes the attributes that have a null value.

#### Return:

**GeoJSON file** - It contains features without attributes with value as null.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    deletenulls input.geojson > output.geojson
```
