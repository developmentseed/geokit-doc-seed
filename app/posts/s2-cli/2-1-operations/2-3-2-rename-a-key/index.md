---
title: Rename a key
date: 2012-09-28
layout: post.html
---

- It renames one or more attributes of the features in the GeoJSON file.

<table border cellpadding="5px">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 20%;">REQUIRED</th> 
        <th style="width: 50%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON to process.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--props</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Attributes to rename. This can be multiple and in the following format: old_key=new_key</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON file** - It contains features with the new names of the attributes.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    renamekey \
    --geojson_input=<INPUT_GEOJSON> \
    --props=old_key_1=new_key_1 \
    --props=old_key_2=new_key_2 \
    --geojson_output=<OUTPUT_GEOJSON>
```

#### Use case:

- Rename the attribute `dc_has_pattern_school` to `pattern_school` in each feature in the input file.

![Image](https://user-images.githubusercontent.com/11504548/184251665-27df7077-23f9-480d-8faf-9b0de8a60ce1.png)
