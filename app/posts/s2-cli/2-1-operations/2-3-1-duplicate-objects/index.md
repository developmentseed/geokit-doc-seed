---
title: Duplicate objects
date: 2012-09-28
layout: post.html
---

- Gets the duplicate objects, identified by a unique attribute or primary key.This script can work with aws - s3 uri.

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
		<td style="text-align: center; vertical-align: middle;">--key</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Primary key or any key to find duplicates</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to geojson output</td>
	</tr>
</table>

#### Return:

**Geojson file** - it contains those duplicate features by a given key.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python geo \
    duplicatefeatures \
    --geojson_input=<INPUT_GEOJSON> \
    --key=key \
    --geojson_output=<OUTPUT_GEOJSON>
```
