---
title: Intersection box
date: 2012-09-28
layout: post.html
---

- Find the boxes that intersect and are greater than the tolerance, for default tolerance is 70 (70% of the area of the small intersection box).

<table border>
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--in_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to cvat xml file</td>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--tolerance</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">tolerance to filter</td>
	</tr>       
</table>

#### Return

**csv file** - it contains the image id (as an attribute) for validating if exist duplicate boxes for the same object or feature.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python cvat \ 
    intersectionbox \
    --in_file=<CVAT_XML> \
    --tolerance=<TOLERANCE> > output.csv
```