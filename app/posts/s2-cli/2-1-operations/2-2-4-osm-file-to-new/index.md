---
title: OSM file to new
date: 2012-09-28
layout: post.html
---

- Removes some attributes of each feature such as: `user`, `version`, `timestamp`, `changeset` and `uid`. So, it returns a new OSM file without these attributes.

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

**OSM file** - The features in the file does not have the `user`, `version`, `timestamp`, `changeset` and `uid` properties.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python geo \
    osm2new \
    --input_osm=<INPUT_OSM> \
    --output_osm=<OUTPUT_OSM>
```

#### Use case:

- Remove the attributes: `user`, `version`, `timestamp`, `changeset` and `uid`.

![Screenshot from 2021-08-11 12-33-38](https://user-images.githubusercontent.com/11504548/129076313-52183872-f2c3-4cc7-95b7-dc35a86eb950.png)
