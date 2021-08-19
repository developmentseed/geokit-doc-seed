---
title: OSM to GeoJSON
date: 2012-09-28
layout: post.html
---

- It converts OSM file to GeoJSON format.

#### Return

**GeoJSON file** - it contains the FeatureCollection in GeoJSON format file.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    osmtogeojson input.osm > output.geojson
```

#### Use case:

- Convert from OSM to GeoJSON format file.

![image](https://user-images.githubusercontent.com/19536044/47044659-64014e80-d156-11e8-9e7e-6e2d592b8354.png)
