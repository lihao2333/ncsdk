# Introduction

This Dockerfile can be used to easily build a Docker image that has the Intel® Movidius™ Neural Compute SDK installed on Ubuntu 16.04.
这是在基于lihao2333/intel:v0 的基础上，安装django

## Build the image



If you've already cloned the NCSDK, you can execute the following command from within the ncsdk directory instead:

$ docker build -t lihao2333/intel:v1 -f ./extras/docker/Dockerfile .

This creates an image named "ncsdk".

*Note: If you are running Docker behind a proxy you must configure proxy settings for Docker before you can build the image. See the NCSDK Docker documentation for more information.*

## Run the container

After the image is built, execute the following command to run the container that we named "ncsdk":

$ docker run --net=host --privileged -v /dev:/dev --name ncsdk -i -t ncsdk /bin/bash

## Additional Information

See the full NCSDK documentation for Docker at https://movidius.github.io/ncsdk/ for more information.
