---
title: XML to NPZ
date: 2012-09-28
layout: post.html
---

- It converts from XML to NPZ format.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--xml_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to CVAT-XML file.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--npz_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to NPZ file.</td>
	</tr>         
</table>

#### Return

**NPZ file** 

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest cvat \
    xml2npz \
    --xml_file=<CVAT_XML> \
    --npz_file=<NPZ>
```
