---
title: GeoJSON to OSM
date: 2012-09-28
layout: post.html
---

- It converts GeoJSON file to OSM format.

#### Return

**OSM file** - it contains the FeatureCollection in OSM format file.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest \
    geojsontoosm input.geojson > output.osm
```

#### Use case:

- Convert from GeoJSON to OSM format file.

![image](https://user-images.githubusercontent.com/19536044/47044616-4fbd5180-d156-11e8-8a2d-beaba2ed325e.png)
