---
title: Bbox of FeatureCollection
date: 2012-09-28
layout: post.html
---

- It gets the bounding box of a FeatureCollection. 

#### Return:

**bbox** - Bounding box extent in minX, minY, maxX, maxY

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    bbox input.geojson
```

### Use Case:

- Get the bounding box of FeatureCollection.

![image](https://user-images.githubusercontent.com/11504548/46218693-eb536300-c30a-11e8-8a3d-e4f93c508d5c.png)