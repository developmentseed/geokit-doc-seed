---
title: Fix ordinal suffixes
date: 2012-09-28
layout: post.html
---

- Fix ordinal suffixes of xml file.

<table border>
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--xml_input</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to xml file</td>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--xml_output</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to the output xml file</td>
	</tr>    
</table>

#### Return

**xml file** - it contains the fixed of the ordinal suffixes.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python cvat \
    fix_ordinal_suffixes \
    --xml_input=<INPUT_XML> \
    --xml_output=<OUTPUT_XML>
```
