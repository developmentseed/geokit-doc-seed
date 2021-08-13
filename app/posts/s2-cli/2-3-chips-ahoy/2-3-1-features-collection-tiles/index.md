---
title: Features collection tiles
date: 2012-09-28
layout: post.html
---

- It adds the tiles and url-tiles to each features in a GeoJSON file.

<table border cellpadding="5">
	<tr>
		<th style="width: 20%;">COMMAND</th> 
        <th style="width: 20%;">REQUIRED</th> 
        <th style="width: 50%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to GeoJSON file</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--zoom</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Zoom to get the tile</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--url_map_service</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Tile map service url</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--geojson_output</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Original GeoJSON with the attributes: tile, url</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--chuck</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Chuck size</td>
	</tr>
</table>
  
#### Return:

**GeoJSON file** - features have the properties of tile, tile's url and the uuid.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest chips_ahoy \
    fctile \
    --geojson_file=<INPUT_GEOJSON> \
    --zoom=<ZOOM> \
    --url_map_service=<URL_MAP_SERVICE> \
    --geojson_output=<OUTPUT_GEOJSON> \
    --chuck=<CHUCK_SIZE>
```

### Use Case:

- Add property of `uuid`, `tile` and `url` to the features.

![image](https://user-images.githubusercontent.com/11504548/129078808-cf284c44-ae6d-46d1-94fb-3349dbf6d940.png)
