---
title: Buffer
date: 2012-09-28
layout: post.html
---

- It creates a buffer in LineString features for a given radius.

#### Return:

**GeoJSON file** - It contains the buffer of the LineStrings.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    buffer input.geojson --unit=meters --radius=10000  > output.geojson
```

### Use Case:

- Create a buffer of the LineString with 10 meters of radiu.

![image](https://user-images.githubusercontent.com/11504548/46221331-6d935580-c312-11e8-9315-5a8ae7d9af71.png)