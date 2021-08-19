---
title: Distance
date: 2012-09-28
layout: post.html
---

- It gets the total distance in km of LineString and MultiLineString features that there are in a GeoJSON file.

#### Return:

**Number** - total length in kilometers.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    distance input.geojson
```

#### Use case:

- Get total highways length in kilometers.

![image](https://user-images.githubusercontent.com/19536044/46213773-146df680-c2ff-11e8-87e6-548cd9c55842.png)
