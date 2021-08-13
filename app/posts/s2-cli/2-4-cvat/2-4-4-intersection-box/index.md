---
title: Intersection box
date: 2012-09-28
layout: post.html
---

- It finds the boxes that intersect and are greater than the tolerance, for default tolerance is 70 (70% of the area of the small intersection box).

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--in_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to CVAT-XML file</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--tolerance</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Tolerance to filter</td>
	</tr>       
</table>

#### Return

**CSV file** - it contains the image id (as an attribute) for validating if exist duplicate boxes for the same object or feature.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest cvat \ 
    intersectionbox \
    --in_file=<CVAT_XML> \
    --tolerance=<TOLERANCE> > output.csv
```
