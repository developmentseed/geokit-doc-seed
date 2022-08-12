---
title: Distance per each feature
date: 2012-09-28
layout: post.html
---

- It gets the length of each feature (LineString/MultiLineString) into a GeoJSON file and it will generate a new GeoJSON file with all features with a distance attribute.

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
        <td style="text-align: justify; vertical-align: middle;">Unit of distance measurement: <br/> - meters: length in meters.<br/> - kilometers: length in kilometers.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON file** - Each linestring/multilinestring feature in the GeoJSON file has a distance attribute in the unit measurement selected.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    distance \
    --geojson_input=<INPUT_GEOJSON> \
    --unit_measurement=kilometers \
    --geojson_output=<OUTPUT_GEOJSON>
```

#### Use case:

- Get the length in kilometers of each linestring/multilinestring.

![Image](https://user-images.githubusercontent.com/11504548/184247418-bc3704f0-b36e-42ea-a6b3-d658149a11a4.png)
