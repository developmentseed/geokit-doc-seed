---
title: Features in polygons
date: 2012-09-28
layout: post.html
---

- It adds the tag `_where` and fields to the features according in which polygons they are. This works with aws - s3 uri.

<table border cellpadding="5px">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 20%;">REQUIRED</th> 
        <th style="width: 50%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_in_polygon</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON polygons.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_in_features</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON features.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--tags_polygon</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Fields in geojson_in_polygon to add to the features. Default value: ""</td>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--mode_filter</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Filtering mode: <br/> - include : includes all the geometry of feature. <br/> - include__centroid: includes the centroid of the feature. <br/> - intersect__<% area> : (polygons) includes a minimum area of the feature (1, 10, 20, 30, 40, 50, 60, 70, 80, 90).</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--mode_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Output mode: <br/> - merged: all features in one file. <br/> - by_location: features in two files, inside and outside. <br/> - by_polygon_tag: features in multiple files, outside and other by tag.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_out_features</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON files** - Different GeoJSON files according the output mode that contains features inside and outside polygons.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    features_in_polygons \
    --geojson_in_polygon=<INPUT_GEOJSON>  \
    --geojson_in_features=<INPUT_GEOJSON> \
    --tags_polygon=tag_1 \
    --tags_polygon=tags_2 \
    --mode_filter=include \
    --mode_output=by_polygon_tag \
    --geojson_out_features=<OUTPUT_GEOJSON>
```
