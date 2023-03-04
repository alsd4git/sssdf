# sssdf
Some Simple Stupid DockerFiles I'll use for testing

I mainly work on windows (my bad) so these commands here are tested on powershell7, they may be sligtly different on bash

[IMAGE_TAG] is the name of the image you will create/launch ecc. you can name wathere you want, i suggest folder name but you do

# To Build: 
(inside folder dedicated)
```bash
docker build --pull --rm -f "DockerFile" -t [IMAGE_TAG]:latest "."
```
# To Run: 
```bash
docker run --rm -v ${PWD}:/app -w /app [IMAGE_TAG]:latest [command here]
```
# To launch a shell inside a temporary container: 
```bash
docker run -i -t --rm -v ${PWD}:/app -w /app [IMAGE_TAG]:latest /bin/bash
```