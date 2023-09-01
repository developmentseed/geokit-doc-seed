---
title: Match point sequences
date: 2012-09-28
layout: post.html
---

- It filters points inside polygons.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 40%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_polygons</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Filter buffer file path (polygons).</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_points</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Points file path (points).</td>
	</tr>     
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Filter check file path (points).</td>
	</tr>      
</table>

#### Return:

**GeoJSON file** - points filtered.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest mapillary \
    match_point_sequences \
    --geojson_polygons=<INPUT_GEOJSON> \
    --geojson_points=<INPUT_GEOJSON> \
    --geojson_output=<OUTPUT_GEOJSON>
```
