---
title: Simplify sequences
date: 2012-09-28
layout: post.html
---

- It simplifies mapillary sequences by buffer.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 40%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Pathfile for geojson input.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--buffer</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Buffer size for simplifying.</td>
	</tr>   
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_out</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Pathfile for geojson output.</td>
	</tr>       
</table>

#### Return:

**GeoJSON file** - mapillary sequences simplified.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest mapillary \
    simplify_sequence \
    --geojson_input=<INPUT_GEOJSON> \
    --buffer=0.000015 \
    --geojson_out=<OUTPUT_GEOJSON>
```