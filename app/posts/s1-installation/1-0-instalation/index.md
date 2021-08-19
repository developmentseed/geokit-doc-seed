---
title: Installation
date: 2012-09-28
layout: post.html
---

Geokit tool was include in a docker-container.

### Install Geokit CLI by Container

Geokit can be built from the repository or pulled from docker-hub.


#### 1. Building from repository
```
git clone git@github.com:developmentseed/geokit.git
cd geokit/
docker-compose build
```

When the docker is built, 3 images are created: one for Node, one for Python, and one for Java.
```
developmentseed/geokit:node.latest
developmentseed/geokit:python.latest
developmentseed/geokit:java.latest
```

- **Geokit-node:** It is a command-line interface (CLI) tool written in Node, that contains several functionalities for measurements, conversions, and operations of GeoJSON files, also we used it to incorporate functionalities of another repository like [awesome-geojson](https://github.com/tmcw/awesome-geojson).
     
- **Geokit-python:** It is a command-line interface (CLI) tool written in Python3, that contains all the basic functionalities for measurements, conversions and operations of GeoJSON, Shapefile, OSM, XML and others. You can use `--help` to show the commands available and also the options by each script.
    
- **Geokit-java:** It is a command-line interface (CLI) tool written in Java, useful for obtaining functionalities from another repository like [osmosis](https://github.com/openstreetmap/osmosis.git) that helps to process [OpenStreetMap](http://www.openstreetmap.org/) data.

Also you can use an alias to avoid write all the command to run the Docker image.
```
alias geokit-node='docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:node.latest'
```

```
alias geokit-python='docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:python.latest'
```

```
alias geokit-java='docker run --rm -v ${PWD}:/mnt/data developmentseed/geokit:java.latest'
```


#### 2. Pulling from [docker-hub](https://hub.docker.com/r/developmentseed/geokit)

```
docker pull developmentseed/geokit:node.latest
docker pull developmentseed/geokit:python.latest
docker pull developmentseed/geokit:java.latest
```

#### Access to Geokit for development mode
```
cd geokit/
docker run --rm -ti -v ${PWD}:/mnt/data developmentseed/geokit:node.latest bash
docker run --rm -ti -v ${PWD}:/mnt/data developmentseed/geokit:python.latest bash
docker run --rm -ti -v ${PWD}:/mnt/data developmentseed/geokit:java.latest bash
```

