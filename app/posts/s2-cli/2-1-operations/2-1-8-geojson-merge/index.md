---
title: Merge GeoJSON files
date: 2012-09-28
layout: post.html
---

- It merges multiple GeoJSON files into one FeatureCollection. This script can work with aws - s3 uri.

<table border cellpadding="5">
	<tr>
		<th style="width: 15%;">COMMAND</th> 
        <th style="width: 15%;">REQUIRED</th> 
        <th style="width: 15%;">MULTIPLE</th> 
        <th style="width: 25%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_input</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON to process.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--folder_path</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Path to folders with GeoJSON files.</td>
	</tr>  
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--recursive</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Flag to search under folder path. Default: False.</td>
	</tr>        
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON file** - It contains all features.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    merge_fc \
    --geojson_inputs=<INPUT_GEOJSON> \
    --geojson_inputs=<INPUT_GEOJSON> \
    --folder_path=<FOLDER_PATH> \
    --recursive \    
    --geojson_output=<OUTPUT_GEOJSON>
```   

#### Use case:

- Merge two GeoJSON files.

![image](https://user-images.githubusercontent.com/19536044/47046277-61085d00-d15a-11e8-965f-872632bffa8b.png)

