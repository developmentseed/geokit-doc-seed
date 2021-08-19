---
title: NPZ to XML
date: 2012-09-28
layout: post.html
---

- It converts from NPZ to XML format.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 40%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--npz_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to labelMaker NPZ file.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--img_path</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path of the images in CVAT.</td>
	</tr>       
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--img_label</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Label image e.g., tower.</td>
	</tr>     
</table>

#### Return

**XML file** 

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest cvat \    
    npz2xml \
    --npz_file=<NPZ> \
    --img_path=<IMG_PATH> \
    --img_label=<IMG_LABEL>  
```
