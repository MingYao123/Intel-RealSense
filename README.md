﻿# Intel-RealSense
Intel-RealSense Emotion Recognize
使用RealSense SR300 DepthCamera作为采集设备，使用RealSense接口完成数据采集。
从CK+动态表情库中提取数据，转化成统一的RealSense标准。

## DF_FaceTracking.cs
从CK+动态表情库中提取，特征点信息  
 
版本：V1226    
修改：修改基础数据记录格式，FaceDate记录完整78个点，编号从0到77。     
      每行包含 日期 时间 Id (World_xyz Image_xy )*78 HeadPostion_xyz PoseEuler_pitch/roll/yaw  

版本：V1221     
修改：增加深度限定，面部离摄像头在25cm内，才能开始记录数据。      
      FaceDateLess记录原有32个点的数据

<img src="https://github.com/EStormLynn/Intel-RealSense/blob/master/Image/界面.png" width="663" height="350" alt="程序界面"/>1


## Python Extrack Landmarks From CK+
从CK+动态表情库中提取，特征点信息  

主要完成：  
1.将CK+库中表情的特征点和Realsense采集的特征点关联，进行转换   
2.将每个表情的多张图片序列，数据信息整合到一个txt中，方便做动态表情识别   
3.实现Python递归动态处理一个目录下多个文件夹，多个文件的数据  


<img src="https://github.com/EStormLynn/Intel-RealSense/blob/master/Image/landmarkPoint%20of%20RS%20and%20CK%2B.png" width="680" height="350" alt="landmarkPoint of RS and CK+"/>1