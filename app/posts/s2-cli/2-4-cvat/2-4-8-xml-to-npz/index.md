---
title: xml to npz
date: 2012-09-28
layout: post.html
---

- Convert xml to npz format.

<table border>
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--xml_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to cvat xml file</td>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--npz_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to npz file</td>
	</tr>         
</table>

#### Return

**npz file** 

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python cvat \
    xml2npz \
    --xml_file=<CVAT_XML> \
    --npz_file=<NPZ>
```