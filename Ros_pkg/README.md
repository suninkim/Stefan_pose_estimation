# ROS package for pose estimation

This package is a ros package for estimating the pose of Stephan chair parts.

## Deep learning

First, in the yolov3 package, run the code below to estimate the position and initial posture of the executing object.

```
roslaunch yolov3 detector.launch
```
This package is a package that adds Angle-net to the package of yolov3.

In this case, the estimation result is shown as follows.

![re_angle_net_result](https://user-images.githubusercontent.com/50347012/144415616-844f7696-4a32-4698-8e8e-338bf8c66223.png)



## Point cloud

It receives the information detected by deep learning and estimates the posture of the chair parts through the point cloud package.

Precise pose estimation is possible through point cloud, and accurate object detection is possible.

At this time, there is a code composed of services and a code composed of nodes.

```
rosrun ros_pose_estimation pose_query
```
```
rosrun ros_pose_estimation pose_estimation
```

The pose estimation result is shown in the figure below.

![re_point_cloud_result](https://user-images.githubusercontent.com/50347012/144415636-5036f365-7740-40c3-a98e-26b24d63561c.png)
