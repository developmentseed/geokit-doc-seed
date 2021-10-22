---
title: Filter by property or geometry
date: 2012-09-28
layout: post.html
---

- It filters features by given property or geometry and it will generate a new GeoJSON files with the filtered features.

<table border cellpadding="5px">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 20%;">REQUIRED</th> 
        <th style="width: 50%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON to process.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--mode_filter</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Filtering mode: <br/> - by_properties: filter by given properties.<br/> - by_properties_strict: features must have all given properties to filter. <br/> - by_geometry: filter by given geometry type.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--props</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Property/Geometry to filter. In case of properties, they can be: key=value or key=*.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--mode_output</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Output mode: <br/> - merged: all features in one file <br/> - by_props: features in each file according filtered properties. <br/> - by_geometry: features in each file according the filtered geometries.<br>Defaul value: merged.</br></td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON file** - Different GeoJSON files according the output mode that contains the filtered features.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    fc_filter \
    --geojson_input=<INPUT_GEOJSON> \
    --mode_filter=by_properties \
    --props=key1=value1 \
    --props=key2=value2 \
    --mode_output=by_props \
    --geojson_output=<OUTPUT_GEOJSON>
```

#### Use case:

- Filter by property: From a set of different features in a GeoJSON file, filter only buildings.

![image](https://user-images.githubusercontent.com/11504548/46221600-63be2200-c313-11e8-9f23-e6d3d86767dd.png)

- Filter by geometry: From a set of different types of features in a GeoJSON file, filter only LineString type.

![image](https://user-images.githubusercontent.com/11504548/46836199-27a8a980-cd76-11e8-8ed2-247e0bef7f69.png)
