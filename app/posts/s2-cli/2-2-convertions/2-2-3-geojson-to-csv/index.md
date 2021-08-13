---
title: GeoJSON to CSV
date: 2012-09-28
layout: post.html
---

- It converts GeoJSON to CSV, and also add an osm_download_link column that contains the download link for each feature in JOSM. It works also with aws uri.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON polygons</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--osm_download_link</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Add osm_download_link</td>
	</tr>       
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--csv_out</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to CSV output</td>
	</tr>     
</table>

#### Return

**CSV file** - with osm_download_link column in the file.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    fc2csv \
    --geojson_input=<INPUT_GEOJSON>  \
    --osm_download_link \
    --csv_out=<OUTPUT_CSV>
```

#### Use case:

- Convert GeoJSON to CSV, and add an osm_download_link column to download data in JOSM.

![image](https://user-images.githubusercontent.com/19536044/46218645-c6f78680-c30a-11e8-940e-b9bf3a2c8a70.png)
