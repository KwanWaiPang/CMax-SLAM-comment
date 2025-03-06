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

# 测试记录

1. DAVIS240c的测试情况：实时性很差(完全不能实时，1分钟左右的rosbag要跑超过8分钟)，不同的rosbag要用不同的参数。但运动补偿的效果看着还行（也可能是本身采用了slice event,如果增大事件量会发现运动补偿的效果特别的差～～～）估算的pose也不以ros输出

运行测试davis240c（直接采用原包）：

    roslaunch cmax_slam davis240c_testing.launch

效果：
* [shapes_rotation](https://www.bilibili.com/video/BV1F1421Z7PR/?vd_source=a88e426798937812a8ffc1a9be5a3cb7)
* [poster_rotation](https://www.bilibili.com/video/BV1RD421p7Yp/)
* [dynamic_rotation](https://www.bilibili.com/video/BV1dm411B7Fw/)

2. DVXplorer（640*480分别率）

运行测试ecrot_handheld（作者提供的数据集）：

    roslaunch cmax_slam ecrot_handheld.launch

运行测试tub_main_building（作者提供的数据集）：

    roslaunch cmax_slam ecrot_mount.launch

效果：
* [river](https://www.bilibili.com/video/BV1Yz421r7bs/)
* [tub_main_building](https://www.bilibili.com/video/BV1Vz421C7eS/)

3. 如果在aggressive的情况，且增大num_events_per_packet为50000，运动补偿的效果极差，部分情况还不如不做CM运动补偿

<p align="center">
  <a href="">
    <img src="pics/2024-04-16 16-21-47 的屏幕截图.png" alt="teaser" width="60%">
  </a>
  <a href="">
    <img src="pics/2024-04-16 16-21-57 的屏幕截图.png" alt="teaser" width="60%">
  </a>
  <a href="">
    <img src="pics/2024-04-16 16-22-18 的屏幕截图.png" alt="teaser" width="60%">
  </a>
  <a href="">
    <img src="pics/2024-04-16 16-22-36 的屏幕截图.png" alt="teaser" width="60%">
  </a>
  <a href="">
    <img src="pics/2024-04-16 16-24-56 的屏幕截图.png" alt="teaser" width="60%">
  </a>
  <a href="">
    <img src="pics/2024-04-16 16-25-34 的屏幕截图.png" alt="teaser" width="60%">
  </a>

</p>

