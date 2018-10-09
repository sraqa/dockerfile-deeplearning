# Deeplearning docker image

Dockerfile is for an image based on conda/miniconda3. The base image is Ubuntu instead of Debian, the image uses CPU version of Tensorflow.

## How to build the image

1. Clone or download this repo (git clone https://github.com/sraqa/dockerfile-deeplearning)
2. Navigate to the new directory
3. Build the docker image with command:

`docker build -t sraqa/deeplearn .`
* Mind the trailing dot. This tells docker to use the Dockerfile in your current directory.

## How to run the image

* To run the image, type:

`docker run -it -p 8888:8888 sraqa/deeplearn`
* Open the browser and navigate to http://localhost:8888 (this will open Jupyter notebook)

* To run the image with persistent storage, type:

`docker run -it -p 8888:8888 -v $PWD:/notebook sraqa/deeplearn`
* Open the browser and navigate to http://localhost:8888 (this will open Jupyter notebook and save your work to the directory you are currently in.
