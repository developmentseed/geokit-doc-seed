---
title: Keep attributes in features
date: 2012-09-28
layout: post.html
---

- It allows you to keep only the keys (properties) that are specified, removing the others ones. This script can work with aws - s3 uri.

<table border cellpadding="5px">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 50%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON to process.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--keys</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Keys to keep. Can be multiple.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_out</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON file** - It contains features with the keys that were keep.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    keepattributes \
    --geojson_input=<INPUT_GEOJSON>  \
    --keys=key1 \
    --keys=key2 \
    --keys=key3 \
    --geojson_out=<OUTPUT_GEOJSON>
```

#### Use case:

- Keep only the keys: `country`,`dc_has_pattern_school` and `project`

![image](https://user-images.githubusercontent.com/11504548/129079849-0047ae06-9527-4b62-b44c-86129fca377f.png)
