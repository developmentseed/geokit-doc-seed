---
title: Generate id
date: 2012-09-28
layout: post.html
---

- Addig a key <id_label> in the PROPERTIES in a geojson file, the value of id can start in 1 or start_count. This script can work with aws - s3 uri.

<table border>
	<tr>
		<th style="width: 20%;">COMMAND</th> 
        <th style="width: 20%;">REQUIRED</th> 
        <th style="width: 60%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--in_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to geojson file</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--id_label</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">name of key to id</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--id_start</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">value of first id, the next value is its sequence (number)</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--zeros</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">add zeros at the beginning of the id, until it reaches the specified length. Example: --zeros 3 --> 003</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--variation</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">type of id (number or uuid), default=number</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--output_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to geojson output file</td>
	</tr>
</table>

#### Return:

**Geojson file** - Each feature in the file has an `id` property.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python  geo \
    generate_id \
    --in_file=<GEOJSON_PATH> \
    --id_label=<NEW_ID> \
    --id_start=100 \
    --zeros=5  \
    --output_file=S3://an-awesome-bucket-name/file.geojson
```

#### Use case:

- Add `ID` attribute to each feature in the geojson file.

![Screenshot from 2021-08-11 12-42-08](https://user-images.githubusercontent.com/11504548/129077460-a8bc7773-6bb8-48c2-9cc4-59b786bdb2bf.png)
