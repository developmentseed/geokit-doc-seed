---
title: Rename a key
date: 2012-09-28
layout: post.html
---

- It changes a key name in each features in the GeoJSON file.

#### Return:

**GeoJSON file** - It contains features with the new name of the key.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest geokit \
    renamekey input.geojson --key="old_key_name>new_key_name" > output.geojson
```

#### Use case:

- Rename the key `dc_has_pattern_school` to `pattern_school` in each feature in the input file.

![image](https://user-images.githubusercontent.com/11504548/129107532-4ed95566-d646-4299-bb0d-6d2845a6f773.png)
