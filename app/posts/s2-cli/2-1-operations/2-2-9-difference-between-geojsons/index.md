---
title: Difference between two geojson files
date: 2012-09-28
layout: post.html
---

- Gets the difference of the objects between two geojson files according to a common attribute. This script can work with aws - s3 uri.

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
		<td style="text-align: center; vertical-align: middle;">--geojson_dif</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to geojson difference to process</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--key</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Could be any of attribute, which is in both files</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to geojson output</td>
	</tr>
</table>

#### Return:

**Geojson file** - It contains the objects that is missing in one of the input file

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python geo \
    difference \
    --geojson_input=<INPUT_GEOJSON> \
    --geojson_dif=<INPUT_DIFF_GEOJSON> \
    --key=key \
    --geojson_output=<OUTPUT_GEOJSON>
```
