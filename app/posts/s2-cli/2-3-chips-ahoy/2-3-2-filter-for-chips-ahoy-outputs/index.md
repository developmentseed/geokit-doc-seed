---
title: Filter for chips ahoy outputs
date: 2012-09-28
layout: post.html
---

- It separates the features tagged as `yes` and `no` in polygons(tiles) and points.

<table border>
	<tr>
		<th style="width: 20%;">COMMAND</th> 
        <th style="width: 20%;">REQUIRED</th> 
        <th style="width: 50%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: left; vertical-align: middle;">&nbsp;--geojson_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: left; vertical-align: middle;">&nbsp;Path to GeoJSON file</td>
	</tr>
    <tr>
		<td style="text-align: left; vertical-align: middle;">&nbsp;--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: left; vertical-align: middle;">&nbsp;GeoJSON separated in no, yes (tile - point)</td>
	</tr>
</table>

#### Return

**GeoJSON files** - One file of the tiles (polygons) tagged as `yes`, one file of the tiles (polygons) tagged as `no` and one file of the schools (points).

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest chips_ahoy \
    filter_chips \
    --geojson_file=<INPUT_GEOJSON> \
    --geojson_output=<OUTPUT_GEOJSON>
```
