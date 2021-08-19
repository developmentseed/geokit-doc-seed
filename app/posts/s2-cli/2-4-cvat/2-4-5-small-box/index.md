---
title: Small box
date: 2012-09-28
layout: post.html
---

- It finds the boxes with an area smaller than the image.

<table border cellpadding="5">
	<tr>
		<th style="width: 20%;">COMMAND</th> 
        <th style="width: 20%;">REQUIRED</th> 
        <th style="width: 50%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--in_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to CVAT-XML file.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--tolerance</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Tolerance to filter. Default value: 1.0 (1% of image area).</td>
	</tr>       
</table>

#### Return

**CSV file** - it contains the image id (as an attribute), which is useful for validating if exist small boxes that don't belong to an object or feature.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest cvat \
    smallbox \
    --in_file=<CVAT_XML> \
    --tolerance=<TOLERANCE>  > output.csv
```

#### Use case:
- Find the smaller boxes that maybe don't belong to an object or feature.

![image](https://user-images.githubusercontent.com/19536044/129048747-8323de5b-e210-4cc6-aba3-9c0269b2e8d2.png)
