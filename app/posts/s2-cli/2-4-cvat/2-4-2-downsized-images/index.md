---
title: Downsized images
date: 2012-09-28
layout: post.html
---

- Downsize the images from big size to 512x512. Supports only jpg files.

<table border>
	<tr>
		<th style="width: 30%;">COMMAND</th> 
        <th style="width: 30%;">REQUIRED</th> 
        <th style="width: 30%;">DESCRIPTION</th>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--img_path</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to images folder</td>
	</tr>
	<tr>
		<td style="text-align: center; vertical-align: middle;">--output_path</td> 
        <td style="text-align: center; vertical-align: middle;">yes</td>
        <td style="text-align: center; vertical-align: middle;">path to the output images folder</td>
	</tr>    
</table>

#### Return

**images** - downsized images, it works for many images inside a folder.

#### Command line:

```
docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python cvat \
    downsized_imgs \ 
    --img_path=<IMG_FOLDER> \
    --output_path=<OUTPUT_FOLDER>
```

#### Use case:

- Downsize the image from 1280x853 to 512x512 size. 

![image](https://user-images.githubusercontent.com/19536044/129049472-b8d56e9f-d75d-43ed-a17e-478bf04b417b.png)




