---
title: Count tags
date: 2012-09-28
layout: post.html
---

- Get the total of images tagged and boxes tagged according to their classification.

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
</table>

#### Return:

**Number** - stats of the images and boxes that were tagged.

### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python cvat \
    count_tag \
    --xml_file=<CVAT_XML>
```

### Use Case:

- Get stats of the images and boxes that were tagged according to their classification.

![image](https://user-images.githubusercontent.com/19536044/129048712-73989a8c-f5c8-48a3-9601-114d8ac5dd7c.png)
