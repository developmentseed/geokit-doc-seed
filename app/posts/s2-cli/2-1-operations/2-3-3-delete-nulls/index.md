---
title: Delete nulls
date: 2012-09-28
layout: post.html
---

- Deletes the attributes that have a null value.

#### Return:

**Geojson file** - it contains features without attributes with value as null.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node geokit \
    deletenulls input.geojson > output.geojson
```
