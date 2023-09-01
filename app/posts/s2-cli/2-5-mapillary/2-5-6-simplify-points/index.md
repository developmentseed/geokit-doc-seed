---
title: Simplify points
date: 2012-09-28
layout: post.html
---

- It simplifies points in a mapillary sequence according to a given distance in meters.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 40%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--input_points</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Pathfile for geojson input.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--points_distance</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Distance in meters applied for simplifying.</td>
	</tr>   
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--output_points</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Pathfile for geojson output.</td>
	</tr>       
</table>

#### Return:

**GeoJSON file** - mapillary points simplified.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest mapillary \
    simplify_points \
    --input_points=<INPUT_GEOJSON> \
    --points_distance=4 \
    --output_points=<OUTPUT_GEOJSON>
```
