---
title: Installation
date: 2012-09-28
layout: post.html
---

Geokit tool was include in a docker-container.

#### Install Geokit CLI by Container

Geokit is installed with docker, due several functionalities from other repositories like [awesome-geojson](https://github.com/tmcw/awesome-geojson) were incorporated to Geokit functionalities.

Clone the repository and build the docker image, also you can use an alias to avoid write all the command to run the Docker image. 

```
git clone git@github.com:developmentseed/geokit.git
cd geokit/
```
```
docker-compose build
alias geokit='docker run --rm -v ${PWD}:/app geokit:latest geokit'
```
or

```
docker-compose run geokit
```