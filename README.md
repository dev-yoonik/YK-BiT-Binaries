
![https://yk-website-images.s3.eu-west-1.amazonaws.com/LogoV4_TRANSPARENT.png](https://yk-website-images.s3.eu-west-1.amazonaws.com/LogoV4_TRANSPARENT.png)

# YooniK Biometric in Things Binaries

This repository contains the binaries for the YooniK Biometric in Things, service integrated in 
the commercial offering of [YooniK Services](https://www.yoonik.me)


## YooniK Biometric in Things in a nutshell

The concept of Biometric In Things was designed to bring face authentication to the edge. The software comprises a set of 
complex functionalities such as face detection, face analysis and face verification capabilities. 

The YooniK.BiT supports out of the box the following camera drivers/types:

- Video4Linux 
- UVC cameras
- IP cameras (RTSP)
- Intel Realsense cameras.

## YooniK Biometric in Things Applications

### Live face capture

Detection, analysis and capture faces aligned using ICAO Token Face Images according to ISO/IEC 19794-5.

### Live face verify

Design to build face authentication/verification in edge devices using reference face image already collected.

Common use cases are face authentication based on a passport collected photo like in our [VR-eKiosk project](https://vr-ekiosk.de/) 
or by providing the picture obtained with the provided [Face capture](#live-face-capture).

### Face images verify

When you need to validate if the 2 face images belong to the same person you can use this functionality.

## Setup YooniK Biometric in Things.

To start using YooniK BiT, please visit our website and find the subscription that fits your needs.

Once you have your subscription activated, please [reach us](support@yoonik.me) to create the management resources for you.
When you get  our response (within a couple of hours) you need to setup everything in your machine:

- Download the binary files and extract them into you local machine and launch the batch file inside the package.

- Call the setup API endpoint to install everything automatically. You need to provide **x-api-key** key 
from your subscription in the http request header. This request may take some time depending on your internet connection.

Visit our [documentation page](https://dev-yoonik.github.io/YK-BiT-Documentation/) or 
follow one of our YK-BiT-SDK-** repositories for quicker integration and to start building awesome authentication applications.

## Camera configuration

Changing camera is as simply as change two lines of the configuration file. By default the config is 
compatible with UVC and Video4Linux.

#### Use UVC/Video4Linux camera
``` json
   {
   "CameraFactory": {
        "TYPE": "Generic",
        "URL": 0
   }
```

#### Use IP/RTSP camera

``` json
   {
   "CameraFactory": {
        "TYPE": "Generic",
        "URL": <ADD YOUR ENDPOINT HERE>
   }
```

#### Use Intel RealSense cameras
``` json
   {
   "CameraFactory": {
        "TYPE": "RS2",
        "URL": 0
   }
```

## Contact & Support

For more configuration information please [contact us](mailto:tech@yoonik.me) or join us at our [discord community](https://discord.gg/SqHVQUFNtN).



