---
title: Rename a key
date: 2012-09-28
layout: post.html
---

- Changes a key name in each features in the geojson file.

#### Return:

**Geojson file** - it contains features with the new name of the key.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node geokit \
    renamekey input.geojson --key="old_key_name>new_key_name" > output.geojson
```

#### Use case:

- Rename a key in each feature in the file

![Screenshot from 2021-08-11 16-44-49](https://user-images.githubusercontent.com/11504548/129107532-4ed95566-d646-4299-bb0d-6d2845a6f773.png)
