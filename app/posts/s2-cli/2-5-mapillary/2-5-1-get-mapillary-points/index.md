---
title: Get mapillary points
date: 2012-09-28
layout: post.html
---

- It gets points and sequences for a bbox or boundaries from mapillary.

( * ) Convert the human date to timestamp (milliseconds) [here](https://www.epochconverter.com/). 

( ** ) Download a short area in order to recognize the organization id, then check out if the organization id belongs to the required organization `https://graph.mapillary.com/$ORGANIZATION_ID?access_token=$TOKEN&fields=name`.


<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 40%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--input_aoi</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to geojson file of boundaries or bbox in the format 'xMin, yMin, xMax, yMax'.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--field_name</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">A field name from the GeoJSON boundaries.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--timestamp_from *</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Timestamp to filter images. Value in milliseconds.</td>
	</tr> 
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--only_pano</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Filter only panoramic image.</td>
	</tr> 
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--organization_ids **</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Filter by organization id from Mapillary.</td>
	</tr>  
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--output_file_point</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Pathfile for geojson point file.</td>
	</tr>    
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--output_file_sequence</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Pathfile for geojson sequence file.</td>
	</tr>       
</table>

#### Return:

**GeoJSON file** - mapillary points.

**GeoJSON file** - mapillary sequences.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data -e MAPILLARY_ACCESS_TOKEN=${MAPILLARY_ACCESS_TOKEN} -it developmentseed/geokit:python.latest mapillary \
    get_mapillary_points \
    --input_aoi=<INPUT_GEOJSON> \
    --field_name=area \
    --timestamp_from=1651366800000 \
    --organization_ids=1805883732926354 \
    --output_file_point=<OUTPUT_GEOJSON_POINTS> \
    --output_file_sequence=<OUTPUT_GEOJSON_SEQUENCES>
```
