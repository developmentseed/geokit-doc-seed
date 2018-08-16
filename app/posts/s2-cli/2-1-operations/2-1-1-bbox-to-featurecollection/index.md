---
title: Bbox to feature collection
date: 2012-09-28
layout: post.html
---

- Applicable for *bbox extent in minX, minY, maxX, maxY order*
- Convert the bounding box to an geojson file, the geojson file contains the area delimited by the bounding box

#### Return:

**Geojson file** - it contains the area delimited by the bounding box.

### Command line:

```geokit bbox2fc --bbox="-104.99531,39.730988,-104.95754,39.753691" > output.geojson```

### Use Case:

- Get area delimited (boundary) from the bounding box.

![image](https://user-images.githubusercontent.com/19536044/44231235-0acf6b80-a163-11e8-8172-b6d83eb08938.png)