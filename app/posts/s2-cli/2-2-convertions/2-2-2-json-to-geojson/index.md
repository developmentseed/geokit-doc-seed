---
title: json to geojson
date: 2012-09-28
layout: post.html
---

- Gets a geojson file from json file.
  
#### Return:

**Json file** 

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node geokit \
    jsonlines2geojson \
    input.json > output.geojson 
```

