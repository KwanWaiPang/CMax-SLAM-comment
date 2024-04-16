[comment]: <> (# CMax-SLAM)

<!-- PROJECT LOGO -->

<p align="center">

  <h1 align="center"> CMax-SLAM: Event-based Rotational-Motion Bundle Adjustment and SLAM System using Contrast Maximization (中文注释版~仅供个人学习记录用)
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


* 所需其他依赖文件类似于[ESVIO](https://github.com/arclab-hku/ESVIO)

需要安装gsl库:

    sudo apt install libgsl-dev


编译:

    cd ~/catkin_ws_dvs && catkin build cmax_slam