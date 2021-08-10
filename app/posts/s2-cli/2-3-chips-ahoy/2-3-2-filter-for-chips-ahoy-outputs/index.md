---
title: Filter for chips ahoy outputs
date: 2012-09-28
layout: post.html
---

- Adds an osm_download_link column per each feature and each link downloads the feature in JOSM.

#### Return

**CSV file** - with osm_download_link column in the file.

#### Command line:

```geokit fc2csv input.geojson  > output.csv```

#### Use case:

- Add an osm_download_link column to download data in JOSM.

![image](https://user-images.githubusercontent.com/19536044/46218645-c6f78680-c30a-11e8-940e-b9bf3a2c8a70.png)