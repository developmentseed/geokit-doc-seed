---
title: XML to CSV
date: 2012-09-28
layout: post.html
---

- It converts from XML to CSV format.

<table border cellpadding="5">
	<tr>
		<th style="width: 25%;">COMMAND</th> 
        <th style="width: 25%;">REQUIRED</th> 
        <th style="width: 40%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--xml_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to CVAT-XML file.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--csv_file</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to CSV file.</td>
	</tr>       
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--full</td> 
        <td style="text-align: center; vertical-align: middle;">no</td>
        <td style="text-align: justify; vertical-align: middle;">Use True for obtaining all the attributes of the XML. Default value: False.</td>
	</tr>     
</table>

#### Return

**CSV file** - If you run the script without the full command, the CSV file will contain only these attributes: id, width, height, path, and image. But if you run the script with the `--full=True` command the CSV file will contain all the attributes of the XML file.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest cvat \
    xml2csv \
    --xml_file=<CVAT_XML> \
    --csv_file=<CSV> \
    --full=<FULL>
```

#### Use case:
- Convert XML to CSV format, using the `--full=True` command.

![image](https://user-images.githubusercontent.com/19536044/129051925-3a97a787-8a06-4356-83d0-fa63635f78e9.png)
