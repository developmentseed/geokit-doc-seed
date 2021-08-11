---
title: Features in polygons
date: 2012-09-28
layout: post.html
---

- Script to add tag `_where` and fields by location `(mode_filter)`. This work with aws uri.

<table border>
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 20%;">REQUIRED</th> 
        <th style="width: 50%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--geojson_in_polygon</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to geojson polygons</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--geojson_in_features</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to geojson features</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--tags_polygon</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">Fields in geojson_in_polygon to add features</td>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--mode_filter</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Filtering mode: <br/> - include : geometry of feature <br/> - include__centroid: centroid geometry of feature <br/> - intersect__<% area> : (polygons) is taken in minimum area (1, 10, 20, 30, 40, 50, 60, 70, 80, 90) of  intersection to consider inside</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--mode_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Output mode: <br/> - merged: all features in one file <br/> - by_location: features in two files, inside and outside <br/> - by_polygon_tag: features in multiple files, outside and other by tag</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--geojson_out_features</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to geojson features output</td>
	</tr>
</table>

#### Return:

**Geojson files** - Different geojson files according the output mode that contains features inside and outside polygons.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python geo \
    features_in_polygons \
    --geojson_in_polygon=<INPUT_GEOJSON>  \
    --geojson_in_features=<INPUT_GEOJSON> \
    --tags_polygon=tag_1 \
    --tags_polygon=tags_2 \
    --mode_filter=include \
    --mode_output=by_polygon_tag \
    --geojson_out_features=<OUTPUT_GEOJSON>
```
