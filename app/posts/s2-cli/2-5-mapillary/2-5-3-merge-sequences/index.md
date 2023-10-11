---
title: Merge sequences
date: 2012-09-28
layout: post.html
---

- It merges sequences and removes duplicate values.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 40%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Checked sequence file path.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Merge sequence file path.</td>
	</tr>          
</table>

#### Return:

**GeoJSON file** - sequences merged.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest mapillary \
    merge_sequences \
    --geojson_input=<INPUT_GEOJSON> \
    --geojson_output=<OUTPUT_GEOJSON>  
```
