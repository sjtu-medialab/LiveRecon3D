# LiveRecon3D

Public repository for our paper: "A real-time 3D reconstruction system with multiple RGB-D cameras ". The result can be seen from the video below. The foreground dynamic objects is reconstructed in real-time framerate of 30 fps, each frame takes about 65 ms in total. And the background can be replaced by any 3D models, virtual scene rendered by the rendering engine or reconstructed model from the real scene  using BundleFusion.

<iframe src="//player.bilibili.com/player.html?aid=211774233&bvid=BV1ra411C7TG&cid=517398500&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>



## System Design

In online mode, the capturing system  is composed of multiple Kinect v2 sensors and a single computer.  In offline mode, the system can take multiple RGB-D streams as input.

<img src="https://notes.sjtu.edu.cn/uploads/upload_cb9f848ea99e35a3cecd6a9dc7a8006e.png" style="zoom:40%;" />

The pipeline design is shown as follows. The whole system runs in two graphic cards, one is mainly used to do background matting and the second one is used to do volume reconstruction.

<img src="https://notes.sjtu.edu.cn/uploads/upload_de53bcb2b6532e484f01b0867d51ba8e.png" style="zoom:80%;" />

## Dataset

To test our system, we introduce a multi-view dataset, captured by 3 synced cameras. The environment  and one typical frame of our dataset  are  as shown. The whole dataset will be released soon. 

<img src="https://notes.sjtu.edu.cn/uploads/upload_464545f9fd56b569563e3825891e9119.png" style="zoom:80%;" />


<img src="![](https://notes.sjtu.edu.cn/uploads/upload_adb878ba5bb7302fbdb28369e75aa93f.png)" style="zoom:80%;" />