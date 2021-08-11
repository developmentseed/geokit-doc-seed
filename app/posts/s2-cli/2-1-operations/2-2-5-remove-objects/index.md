---
title: Remove objects with action=delete
date: 2012-09-28
layout: post.html
---

- Removes the objects with `action=delete` in a osm file.

<table border>
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--input_osm</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to osm file to be processed</td>
	</tr>
    <tr>
		<td style="text-align: center; vertical-align: middle;">--output_osm</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">Path to osm output</td>
	</tr>
</table>

#### Return:

**OSM file** - it contains objects that have action property different to `delete`.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python geo \
    removeactionosm \
    --input_osm=<INPUT_OSM> \
    --output_osm=<OUTPUT_OSM>
```

#### Use case:

- Remove objects in the OSM file that have the action property as `delete`.

![Screenshot from 2021-08-11 10-27-48](https://user-images.githubusercontent.com/11504548/129058049-141c8045-b913-4a43-820f-8a493e6ef8bf.png)
