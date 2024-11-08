# Person Detector using DeepStream on railway tracks 

Person Detector using DeepStream on railway tracks  to avoid accidents during train crossing on the tracks 

# Features

- This app is built on Nvidia DeepStream SDK, which provides a complete streaming analytics toolkit for object detection.
- Ability to integrate it with the CCTV present on-site and connect to cloud to create a end to end IOT/AI-ML application.



![sample-photo](trainsafety.png)
## Tech Stack

- [DeepStream] - Streaming Analytics toolkit for video, image, audio processing/understanding.
- [TensorRT] - TensorRT is a machine learning framework that is used to run machine learning inference on Nvidia hardware.
- [YOLOV5] - YOLO is a advanced computer vision algorithm that is used in object detection.
- [Jetson] - It is a SOM device manufactured by Nvidia for running tensor intensive application.

![Jetson](https://i.imgur.com/eCMj2EV.jpg)

## Working
This application can be run on any NVIDIA powered such as DGPUs, Jetson Nano, Xavier, etc.

### Installation of Dependencies
1. Installing System Dependencies for DeepStream
    ```sh
    sudo apt install \
    libssl1.0.0 \
    libgstreamer1.0-0 \
    gstreamer1.0-tools \
    gstreamer1.0-plugins-good \
    gstreamer1.0-plugins-bad \
    gstreamer1.0-plugins-ugly \
    gstreamer1.0-libav \
    libgstrtspserver-1.0-0 \
    libjansson4=2.11-1
    uuid \
    uuid-dev
    ```
2. DeepStream installation on Jetson Device
Download the deb file under - DeepStream 5.1 for Jetson from [here](https://developer.nvidia.com/deepstream-getting-started)

    ```sh
    sudo apt-get install ./deepstream-5.1_5.1.0-1_amd64.deb
    ```

### Starting the application
1. Installing git related software
    ```sh
    sudo apt install git git-lfs
    ```
2. Clone the repo
    ```sh
    git clone [https://github.com/purushogit/DEEPSTREAM-PROJECT.git]
      ```
3. Download the lfs files
    ```
    git lfs pull
    ```
4. Running the application

    1. Firstly we need to build the application
        ```sh
        make clean && make -j$(nproc)
        ```
    2. Put the video source location / RTSP urls in the input_sources.txt (video location in this case)
        ```
        file:///home/purushotham/Documents/deepstream-5.1/sources/apps/sample_apps/train-safety/final.h264
        ```
    3. After running the step 1 a binary file would have been created of the app. To run the binary use the following command
        ```
        ./train-safety source-path
        ```
Find the link of the demo videos below:
[![DeepStream]](https://youtu.be/YgoWKVqKqF4)
