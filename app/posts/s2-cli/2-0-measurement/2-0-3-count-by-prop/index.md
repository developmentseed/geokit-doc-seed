---
title: Count feature by property
date: 2012-09-28
layout: post.html
---

- Gets the total number of features that exist inside the a geojson file (according to a chosen property).

#### Return: 
**Number** - total number of features.

### Command line:

```geokit countfeature input.geojson --prop property=*```

**Note:** The property can be building, highway, landuse, etc.

#### Use case:
- Get the total number of features.  

![image](https://user-images.githubusercontent.com/19536044/46213477-4468ca00-c2fe-11e8-94df-82ef7f65823d.png)