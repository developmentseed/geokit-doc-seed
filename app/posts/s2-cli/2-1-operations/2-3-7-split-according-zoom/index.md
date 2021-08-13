---
title: Split a file according to zoom level
date: 2012-09-28
layout: post.html
---

- It divides the features in a GeoJSON file according to a given zoom level (works for zoom <= 15), and it will generate GeoJSON files into a folder.

#### Return:

**GeoJSON files** - The number of files will depend of the given zoom level.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    splitbyzoom input.geojson --folder=folder_name --zoom=10
```
