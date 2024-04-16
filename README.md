[comment]: <> (# CMax-SLAM)

<!-- PROJECT LOGO -->

<p align="center">

  <h1 align="center"> CMax-SLAM: Event-based Rotational-Motion Bundle Adjustment and SLAM System using Contrast Maximization (Testing Version~仅供个人学习记录用)
  </h1>

[comment]: <> (  <h2 align="center">PAPER</h2>)
  <h3 align="center">
  <a href="https://arxiv.org/pdf/2403.08119.pdf">Paper</a> 
  | <a href="https://github.com/tub-rip/cmax_slam">Original Github Page</a>
  | <a href="https://github.com/tub-rip/ECRot">Dataset</a>
  </h3>
  <div align="center"></div>

<!-- <p align="center">
  <a href="">
    <img src="https://huajianup.github.io/thumbnails/Photo-SLAM_v2.gif" alt="teaser" width="100%">
  </a>
</p> -->
<br>

# 一个只能估计rotation以及输出与深度信息无关的“Map”的SLAM系统

* 所需其他依赖文件类似于[ESVIO](https://github.com/arclab-hku/ESVIO)

需要安装gsl库:

    sudo apt install libgsl-dev


编译:

    cd ~/catkin_ws_dvs && catkin build cmax_slam

运行测试davis240c（直接采用原包）：

    roslaunch cmax_slam davis240c_testing.launch

# 测试记录

1. DAVIS240c的测试情况：实时性很差(完全不能实时，1分钟左右的rosbag要跑超过10分钟)，不同的rosbag要用不同的参数。但运动补偿的效果看着还行（也可能是本身采用了slice event,如果增大事件量会发现运动补偿的效果特别的差～～～）
效果：
* [shapes_rotation]()
* [poster_rotation]()
* [dynamic_rotation]()


# 结论


 emmmm.... :cold_sweat: :sweat_smile: :sweat: