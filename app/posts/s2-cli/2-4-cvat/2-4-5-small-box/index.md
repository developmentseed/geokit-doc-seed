---
title: Small box
date: 2012-09-28
layout: post.html
---

- Find the boxes with an area smaller than the image, for default tolerance is 1 (1% of area image).

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

**csv file** - it contains the image id (as an attribute), which is useful for validating if exist small boxes that don't belong to an object or feature.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python cvat \
    smallbox \
    --in_file=<CVAT_XML> \
    --tolerance=<TOLERANCE>  > output.csv
```

#### Use case:
- Find the smaller boxes that maybe don't belong to an object or feature, this is useful for validating.

![image](https://user-images.githubusercontent.com/19536044/129048747-8323de5b-e210-4cc6-aba3-9c0269b2e8d2.png)