# LiveRecon3D

Public repository for our paper: "***RGBD-based Real-time 3D Reconstruction System: Architecture Design and Implementation***". 

## System Design

In online mode, the capturing system  is composed of multiple Kinect v2 sensors and a single computer.  In offline mode, the system can take multiple RGB-D streams as input.

The pipeline design is shown as follows. The whole system runs in two graphic cards, one is mainly used to do background matting and the second one is used to do volume reconstruction.

<img src="https://notes.sjtu.edu.cn/uploads/upload_de53bcb2b6532e484f01b0867d51ba8e.png" style="zoom:80%;" />

## Dataset

To evaluate the results of our system, we introduce a multi-view dataset, captured by 3 kinect v2 cameras. The cameras are placed at 90 degrees from each other, and the distance between them is about 2-3m.

The environment  and one typical frame of our dataset  are  as shown, and the whole dataset will be released soon. 

<img src="https://notes.sjtu.edu.cn/uploads/upload_464545f9fd56b569563e3825891e9119.png" style="zoom:80%;" />

The details of the dataset can be seen from table below.

| Camera         | Kinect v2                             |
| -------------- | ------------------------------------- |
| **Num**        | **3**                                 |
| **Resolution** | **color: 1920x1080 + Depth: 512x424** |
| **Scenes**     | **6**                                 |

## Reconstruction Results

### Our dataset

The result can be seen from the video below. The foreground dynamic objects is reconstructed in real-time frame rate of 30 FPS, each frame takes about 65 ms in total. And the background can be replaced by any 3D models, virtual scene rendered by the rendering engine or reconstructed model from the real scene.

[![YouTube link](https://notes.sjtu.edu.cn/uploads/upload_cdea4d0b0c89b0d2e771e99fad21004a.png)](https://youtu.be/q9Vf05e0QHc)

### Other datasets

We test our system on the dataset published in paper [A New Free Viewpoint RGB-D Video Dataset](https://github.com/sjtu-medialab/Free-Viewpoint-RGB-D-Video-Dataset). The reconstruction results is as follows:

[![YouTube link](https://notes.sjtu.edu.cn/uploads/upload_4953a316a5711b16495dedd92da85b95.png)](https://youtu.be/JqFG8aSdpfw)