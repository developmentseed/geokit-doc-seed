---
title: Add new attributes to features
date: 2012-09-28
layout: post.html
---

- It adds new attributes in each features in the GeoJSON file. This script can work with aws - s3 uri.

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
		<td style="text-align: justify; vertical-align: middle;">--tags</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Attributes to add in format: key=value.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_out</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON file** - It contains features with the new attributes that were added.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    addattributefc \
    --geojson_input=<INPUT_GEOJSON>  \
    --tags key1=value1 \
    --tags key2=value2 \
    --geojson_out=<OUTPUT_GEOJSON>
```

#### Use case:

- Add the attributes: `project` and `country` to each feature in the GeoJSON file.

![image](https://user-images.githubusercontent.com/11504548/129080901-575e3c94-2ec0-42a4-8b0b-79d9186c971a.png)
