---
title: xml to csv
date: 2012-09-28
layout: post.html
---

- Convert xml to csv format.

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
		<td style="text-align: center; vertical-align: middle;">--csv_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to csv file</td>
	</tr>       
	<tr>
		<td style="text-align: center; vertical-align: middle;">--full</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: center; vertical-align: middle;">use True for obtaining all the attributes of the xml</td>
	</tr>     
</table>

#### Return

**csv file** 

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python cvat \
    xml2csv \
    --xml_file=<CVAT_XML> \
    --csv_file=<CSV> \
    --full=<FULL>
```

#### Use case:
- Convert xml to csv format.

![image](https://user-images.githubusercontent.com/19536044/129051925-3a97a787-8a06-4356-83d0-fa63635f78e9.png)
