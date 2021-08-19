---
title: Each feature into a row
date: 2012-09-28
layout: post.html
---

- It sets each feature into a row from FeatureCollection.
  
#### Return:

**JSON file** - each feature was organized into a row.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    fc2frows input.geojson > output.json
```

### Use Case:

- Set each feature into a row.

![image](https://user-images.githubusercontent.com/19536044/129390539-09bf41c2-5bda-4eac-98e5-bf0c58db3844.png)
