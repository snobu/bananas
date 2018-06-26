# This is a highly modified fork of [this other one here](https://github.com/Azure-Samples/Custom-vision-service-iot-edge-raspberry-pi).

# Custom Vision + Azure IoT Edge on a Raspberry Pi 3

Modules:

* *camera-capture* - this module captures the video stream from a USB camera, sends the frames for analysis to the classifier module. This module is written in python and uses OpenCV to read the video feed.

* *image-classifier-service* - it is a web service over HTTP running locally that takes in images and classifies them based on a custom model built via the Custom Vision website. This module has been exported from the Custom Vision website and slightly modified to run on a ARM architecture. You can modify it by updating the model.pb and label.txt files to update the model.

## How it works

Webcam -> camera-capture (capture frame) -> image-classifier-service (get prediction) -> results to volume mounted text file
