---
title: Generate id
date: 2012-09-28
layout: post.html
---

- It adds a key <id_label> in the PROPERTIES in a GeoJSON file, the value of id can start in 1 or in a given value. This script can work with aws - s3 uri.

<table border cellpadding="5px">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 20%;">REQUIRED</th> 
        <th style="width: 60%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--in_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON to process.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--id_label</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Key name for id. Default value: id.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--id_start</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Value of first id, the next value is its sequence (number). Default value: 1.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--zeros</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Add zeros at the beginning of the id value until it reaches the specified length. Example: --zeros 3 --> 003. Default value: 0.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--variation</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Type of id (number or uuid). Default value: number.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--output_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON file** - It contains features that have an `id` property.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    generate_id \
    --in_file=<GEOJSON_PATH> \
    --id_label=<NEW_ID> \
    --id_start=100 \
    --zeros=5  \
    --output_file=S3://an-awesome-bucket-name/file.geojson
```

#### Use case:

- Add `ID` attribute to each feature in the GeoJSON file.

![image](https://user-images.githubusercontent.com/11504548/129077460-a8bc7773-6bb8-48c2-9cc4-59b786bdb2bf.png)
