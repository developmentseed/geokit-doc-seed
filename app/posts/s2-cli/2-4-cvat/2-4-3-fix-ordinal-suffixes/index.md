---
title: Fix ordinal suffixes
date: 2012-09-28
layout: post.html
---

- It fixs the ordinal suffixes of XML file.

<table border cellpadding="5">
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--xml_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to XML file.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--xml_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to the output XML file.</td>
	</tr>    
</table>

#### Return

**XML file** - it contains the ordinal suffixes fixed.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest cvat \
    fix_ordinal_suffixes \
    --xml_input=<INPUT_XML> \
    --xml_output=<OUTPUT_XML>
```
