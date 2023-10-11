---
title: Create custom sequences
date: 2012-09-28
layout: post.html
---

- It adds URLs to review the images of the sequences.

In Mapillary, many sequences have only a frontal view (road). These sequences are not useful when we want to have a view to the facade building or lots, so we can remove them.

In order to delete unnecessary sequences, it is necessary to have the generated custom sequence files and upload them to the tool. We have 2 tools that help us to do it:
1. A plugin in [JOSM](https://josm.openstreetmap.de/) to be able to see an image of a sequence and to be able to delete it if necessary (download it from s3://ds-data-projects/JOSM/osm-obj-info.jar). 

2. An [app](https://filter_sequences.surge.sh/) that allows us to load GeoJSON files and view random images of a sequence, it allows us to delete sequences by marking with a check.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 40%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_points</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Point file path.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--output_file_sequence</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Custom sequence file path.</td>
	</tr>          
</table>

#### Return:

**GeoJSON file** - it contains a new attribute with URLs to review the images of the sequences.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data -e MAPILLARY_ACCESS_TOKEN=$MAPILLARY_ACCESS_TOKEN -it developmentseed/geokit:python.latest mapillary \
    create_custom_sequences \
    --geojson_points=<INPUT_GEOJSON> \
    --output_file_sequence=<OUTPUT_GEOJSON> 
```


