---
title: Clip
date: 2012-09-28
layout: post.html
---

- It gets only the features that are inside the given boundary and it deletes all features outside the boundary. This script can work with aws - s3 uri.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON to process.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_boundary</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON boundary.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return: 

**GeoJSON file** - It contains all features inside the given boundary.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    clip \
    --geojson_input=<INPUT_GEOJSON> \
    --geojson_boundary=<BOUNDARY_GEOJSON> \
    --geojson_output=<OUTPUT_GEOJSON>
```

#### Use case:

- Get only the features that are inside the boundary.

![image](https://user-images.githubusercontent.com/11504548/46220767-ccf06600-c310-11e8-896c-c9ce0351bb15.png)