---
title: Download images
date: 2012-09-28
layout: post.html
---

- It downloads the Mapillary images and obtains output points with the images URL.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 40%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--input_file_points</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Mapillary points file path.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--output_images_path</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Output images path.</td>
	</tr>     
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--output_file_points</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Output points for images.</td>
	</tr>      
</table>

#### Return:

**GeoJSON file** - output points with the images URL.

**Folder** - it contains the downloaded images from Mapillary.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data -e MAPILLARY_ACCESS_TOKEN=$MAPILLARY_ACCESS_TOKEN -it developmentseed/geokit:python.latest mapillary \
    download_mapillary_imgs \
    --input_file_points=<INPUT_GEOJSON> \
    --output_images_path=<OUTPUT_IMAGES PATH> \
    --output_file_points=<OUTPUT_GEOJSON>
```
