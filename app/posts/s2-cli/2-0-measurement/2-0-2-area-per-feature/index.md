---
title: Area per each feature
date: 2012-09-28
layout: post.html
---

- Gets the area in ha of each feature (polygon) into a geojson file and it will generate a new geojson file with all features plus an area property.

#### Return:

**Geojson file** - in each polygon (inside a geojson file) was add area property - the area is in hectares.

### Command line:

```geokit featurearea input.geojson > output.geojson```

#### Use case:
- Get the area in ha of each polygon.  

![image](https://user-images.githubusercontent.com/19536044/46110505-71f02f00-c1a9-11e8-9dcc-96ac9c52b94d.png)