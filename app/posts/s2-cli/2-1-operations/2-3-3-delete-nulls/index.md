---
title: Delete nulls
date: 2012-09-28
layout: post.html
---

- It deletes the attributes or the features, according to the selected option, that has an empty or null value.

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
		<td style="text-align: justify; vertical-align: middle;">--delete_feat</td> 
        <td style="text-align: center; vertical-align: middle;">No</td>
        <td style="text-align: justify; vertical-align: middle;">Delete the features that have attributes with empty or null values.<br/>Add this in the command line will delete the features that have attributes with empty or null values, otherwise, will delete only the attributes instead the features.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON output.</td>
	</tr>
</table>

#### Return:

**GeoJSON file** - It contains features without attributes with value as null.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    deletenulls \
    --geojson_input=<INPUT_GEOJSON> \
    --delete_feat \
    --geojson_output=<OUTPUT_GEOJSON>
```

#### Use case:

- Delete the attributes with an empty or null value.

![Image](https://user-images.githubusercontent.com/11504548/184385801-a7b1fcc8-533b-4f57-99b4-d6b8e893c799.png)