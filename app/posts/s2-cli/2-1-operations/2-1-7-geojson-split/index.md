---
title: Split GeoJSON files
date: 2012-09-28
layout: post.html
---

- It splits a GeoJSON file into smaller GeoJSON files. This script can work with aws - s3 uri.

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
		<td style="text-align: justify; vertical-align: middle;">--size</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Size of geometries per split file.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_out</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON files** - Each file contains a especific number of features.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    fc_split \
    --geojson_input=<INPUT_GEOJSON> \
    --size=number_size \
    --geojson_output=<OUTPUT_GEOJSON>
```
