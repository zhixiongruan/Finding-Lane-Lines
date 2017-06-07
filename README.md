# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

工作流程

这个流程包括6个步骤:

1. 将摄像头拍摄的RGB彩色图片转变成灰度图片。

2. 对上面的灰度图片加入高斯模糊。这样做的目的是为了让我们关注具有强烈对比的图片中的边缘，减弱噪声边缘的影响。

3. 通过Canny边缘识别算法对上面的图片进行边缘识别,找出车道线的位置。

4. 我们找到了很多个边缘，然后划定一个只有车道线的边缘四边形区域，并只显示这个区域内的边缘。

5. 通过Hough变换,画出上面的图片的车道线。

6. 将步骤5中的图片与原始图片结合则产生了识别出车道线的图片。

[结果图](https://github.com/zhixiongruan/Finding-Lane-Lines/tree/master/test_images_output)


两个视频项目处理：将视频分解成一张张图片，将图片按上面6步处理完后再还原成视频，并保留到[test_videos_output](https://github.com/zhixiongruan/Finding-Lane-Lines/tree/master/test_videos_output)文件夹下。


### 2. Identify potential shortcomings with your current pipeline


有以下几个缺点：

1.容易受旁边车辆影响，如果突然出来一辆车并闯进四边形区域里，车道线会出现混乱；

2.应该还有更好的优化方法，但我现在没找到，通过以后的学习再来进行优化；

3.挑战视频没完成，要完成它还需要一些知识和时间。


### 3. Suggest possible improvements to your pipeline

建议：

1.加强python的学习；

2.加强英语的学习；

3.多查看文档。

这个项目还有很大改进空间，以后我会继续优化它。
