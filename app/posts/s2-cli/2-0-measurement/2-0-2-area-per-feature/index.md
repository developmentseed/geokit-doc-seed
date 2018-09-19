---
title: Get area per each feature
date: 2012-09-28
layout: post.html
---

- Applicable for *Polygon* geometry type.
- Get the area of each polygon inside a geojson file.

#### Return:

**Geojson file** - in each polygon (inside a geojson file) was add area property - the area is in hectares.

### Command line:

```geokit featurearea input.geojson > output.geojson```

#### Use case:
- Get area per each polygon.  

![image](https://user-images.githubusercontent.com/19536044/44175281-59213380-a0ab-11e8-9c9a-a6a6dd145d30.png)