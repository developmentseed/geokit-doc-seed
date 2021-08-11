---
title: npz to xml
date: 2012-09-28
layout: post.html
---

- Convert npz to xml format.

<table border>
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--npz_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to labelMaker npz file</td>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--img_path</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path of the images in CVAT</td>
	</tr>       
	<tr>
		<td style="text-align: center; vertical-align: middle;">--img_label</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">label image eg: tower</td>
	</tr>     
</table>


#### Return

**xml file** 

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python cvat \    
    npz2xml \
    --npz_file=<NPZ> \
    --img_path=<IMG_PATH> \
    --img_label=<IMG_LABEL>  
```



