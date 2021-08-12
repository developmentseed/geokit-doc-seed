---
title: Distance per each feature
date: 2012-09-28
layout: post.html
---

- Add distance as an attribute; it contains the length in kilometers that has each feature in a geojson file.

#### Return:

**Geojson file** - with distance attribute

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node geokit \
    featuredistance \
    input.geojson > output.geojson
```

#### Use case:

- Get the length in kilometers by each feature.

![image](https://user-images.githubusercontent.com/19536044/129275038-9e282133-e992-4e26-bc87-f09ce3b3092f.png)

