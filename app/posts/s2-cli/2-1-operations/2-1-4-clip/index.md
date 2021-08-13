---
title: Clip
date: 2012-09-28
layout: post.html
---

- It gets only the features that are inside the given boundary and it deletes all features outside the boundary.

#### Return: 

**GeoJSON file** - It contains all features inside the given boundary.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    clip input.geojson boundary.geojson > output.geojson
```

#### Use case:

- Get only the features that are inside the boundary.

![image](https://user-images.githubusercontent.com/11504548/46220767-ccf06600-c310-11e8-896c-c9ce0351bb15.png)