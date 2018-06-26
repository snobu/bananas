# This is a highly modified fork of [this other one here](https://github.com/Azure-Samples/Custom-vision-service-iot-edge-raspberry-pi).

## Containers:

* camera-capture
* image-classifier-service

## How it works

Webcam -> camera-capture (capture frame) -> image-classifier-service (get prediction) -> results to volume mounted text file
