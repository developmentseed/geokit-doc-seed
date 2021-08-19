---
title: Downsized images
date: 2012-09-28
layout: post.html
---

- It downsizes the images from big size to 512x512. Supports only JPG files.

<table border cellpadding="5">
	<tr>
		<th style="width: 25%;">COMMAND</th> 
        <th style="width: 25%;">REQUIRED</th> 
        <th style="width: 40%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--img_path</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to images folder.</td>
	</tr>
	<tr>
		<td style="text-align: justify; vertical-align: middle;">--output_path</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: justify; vertical-align: middle;">Path to the output images folder.</td>
	</tr>    
</table>

#### Return

**JPG files** - downsized images, it works for many images inside a folder.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest cvat \
    downsized_imgs \ 
    --img_path=<IMG_FOLDER> \
    --output_path=<OUTPUT_FOLDER>
```

#### Use case:

- Downsize the image from 1280x853 to 512x512 size. 

![image](https://user-images.githubusercontent.com/19536044/129049472-b8d56e9f-d75d-43ed-a17e-478bf04b417b.png)




