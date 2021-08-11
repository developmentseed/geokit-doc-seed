---
title: Add new attributes to features
date: 2012-09-28
layout: post.html
---

- Add new attributes in each features in the geojson file. This script can work with aws uri.

<table border>
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--geojson_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to geojson to process</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--tags</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Attributes to add in format: key=value</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--geojson_out</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to geojson features output</td>
	</tr>
</table>

#### Return:

**Geojson file** - Features with the new attributes that were added.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python geo \
    addattributefc \
    --geojson_input=<INPUT_GEOJSON>  \
    --tags key1=value1 \
    --tags key2=value2 \
    --geojson_out=<OUTPUT_GEOJSON>
```

#### Use case:

- Adds new attributes to each feature in the geojson file.

![Screenshot from 2021-08-11 13-08-08](https://user-images.githubusercontent.com/11504548/129080901-575e3c94-2ec0-42a4-8b0b-79d9186c971a.png)
