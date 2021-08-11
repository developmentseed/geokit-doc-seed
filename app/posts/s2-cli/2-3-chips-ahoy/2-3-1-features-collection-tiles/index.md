---
title: Features collection tiles
date: 2012-09-28
layout: post.html
---

- Script to add tiles and url-tiles to each features in a geojson file.

<table border>
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--geojson_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to geojson file</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--zoom</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">zoom to get the tile</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--url_map_service</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">tile map service url</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">original geojson with the attributes: tile, url</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--chuck</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">chuck size</td>
	</tr>
</table>
  
#### Return:

**Geojson file** - features have the properties of tile, tile's url and the uuid.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python chips_ahoy \
    fctile \
    --geojson_file=<INPUT_GEOJSON> \
    --zoom=<ZOOM> \
    --url_map_service=<URL_MAP_SERVICE> \
    --geojson_output=<OUTPUT_GEOJSON> \
    --chuck=<CHUCK_SIZE>
```

### Use Case:

- Add property of `uuid`, `tile` and `url` to the features.

![Screenshot from 2021-08-11 12-52-23](https://user-images.githubusercontent.com/11504548/129078808-cf284c44-ae6d-46d1-94fb-3349dbf6d940.png)
