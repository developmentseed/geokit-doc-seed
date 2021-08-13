---
title: Difference between two GeoJSON files
date: 2012-09-28
layout: post.html
---

- It gets the difference of the objects between two GeoJSON files according to a common attribute. This script can work with aws - s3 uri.

<table border cellpadding="5px">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 0%;">REQUIRED</th> 
        <th style="width: 50%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON to process.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_dif</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON difference to process.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--key</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Could be any of attribute, which is in both files.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON file** - It contains the objects that is missing in one of the input file.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    difference \
    --geojson_input=<INPUT_GEOJSON> \
    --geojson_dif=<INPUT_DIFF_GEOJSON> \
    --key=key \
    --geojson_output=<OUTPUT_GEOJSON>
```
