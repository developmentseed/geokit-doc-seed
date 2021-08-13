---
title: Bbox to FeatureCollection
date: 2012-09-28
layout: post.html
---

- It converts a bounding box to FeatureCollection.

##### Return:

**GeoJSON file** - It contains the given bounding box as polygon.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    bbox2fc --bbox="-104.99531,39.730988,-104.95754,39.753691" > output.geojson
```

### Use Case:

- Get bounding box as polygon in a GeoJSON file.

![image](https://user-images.githubusercontent.com/11504548/46216041-5fd6d380-c304-11e8-949e-2ac49bcbd28a.png)