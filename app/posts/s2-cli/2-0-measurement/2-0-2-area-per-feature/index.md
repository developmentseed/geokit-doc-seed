---
title: Area per each feature
date: 2012-09-28
layout: post.html
---

- It gets the area of each feature (Polygon/MultiPolygon) into a GeoJSON file and it will generate a new GeoJSON file with all features with an area attribute.

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
		<td style="text-align: justify; vertical-align: middle;">--unit_measurement</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Unit of area measurement: <br/> - square_meters: area in square meters.<br/> - hectares: area in hectares. <br/> - square_kilometers: area in square kilometers.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON file** - Each polygon/multipolygon feature in the GeoJSON file has an area attribute in the unit measurement selected.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    featurearea \
    --geojson_input=<INPUT_GEOJSON> \
    --unit_measurement=square_kilometers \
    --geojson_output=<OUTPUT_GEOJSON>
```

#### Use case:
- Get the area in square kilometers of each polygon/multipolygon.  

![images](https://user-images.githubusercontent.com/11504548/184227033-e013c324-e7fd-47d6-8fb9-aa0b5225b48e.png)
