---
title: JSON to GeoJSON
date: 2012-09-28
layout: post.html
---

- It gets a GeoJSON file from JSON file.
  
#### Return:

**GeoJSON file** - from JSON file

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node geokit \
    jsonlines2geojson input.json > output.geojson 
```
