---
title: OSM file to new
date: 2012-09-28
layout: post.html
---

- It removes some attributes of each feature such as: `user`, `version`, `timestamp`, `changeset` and `uid`. So, it returns a new OSM file without these attributes.

<table border cellpadding="5px">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 50%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--input_osm</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to OSM file to process.</td>
	</tr>
    <tr>
		<td style="text-align: justify; vertical-align: middle;">--output_osm</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to OSM output.</td>
	</tr>
</table>

#### Return:

**OSM file** - The features in the file does not have the `user`, `version`, `timestamp`, `changeset` and `uid` properties.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest geo \
    osm2new \
    --input_osm=<INPUT_OSM> \
    --output_osm=<OUTPUT_OSM>
```

#### Use case:

- Remove the attributes: `user`, `version`, `timestamp`, `changeset` and `uid`.

![image](https://user-images.githubusercontent.com/11504548/129076313-52183872-f2c3-4cc7-95b7-dc35a86eb950.png)
