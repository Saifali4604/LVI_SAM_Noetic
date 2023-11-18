# LVI-SAM
<p align='center'>
    <img src="./doc/demo.gif" alt="drawing" width="800"/>
</p>

## Dependency
  ```
  sudo apt-get install -y ros-noetic-navigation
  sudo apt-get install -y ros-noetic-robot-localization
  sudo apt-get install -y ros-noetic-robot-state-publisher
  sudo add-apt-repository ppa:borglab/gtsam-release-4.2
  sudo apt update
  sudo apt install libgtsam-dev libgtsam-unstable-dev
  ```
  ```
  sudo apt-get install -y libgoogle-glog-dev
  sudo apt-get install -y libatlas-base-dev
  wget -O ~/Downloads/ceres.zip https://github.com/ceres-solver/ceres-solver/archive/1.14.0.zip
  cd ~/Downloads/ && unzip ceres.zip -d ~/Downloads/
  cd ~/Downloads/ceres-solver-1.14.0
  mkdir ceres-bin && cd ceres-bin
  cmake ..
  sudo make install -j4
  ```

## Install

Use the following commands to download and compile the package.

```
cd ~/catkin_ws/src
git clone https://github.com/Saifali4604/LVI_SAM_Noetic
cd ..
catkin_make
```

```
cd 
git clone https://github.com/Saifali4604/LVI_SAM_Noetic
```
open file maneger then LVI-SAM folder go to config and copy " brief_k10L6.bin " and paste it in catkin_ws/src/LVI_SAM_Noetic/config/
now ypu can delete LVI-SAM folder in home

## Datasets

[https://drive.google.com/drive/folders/1q2NZnsgNmezFemoxhHnrDnp1JV_bqrgV?usp=sharing]

**Note** that the images in the provided bag files are in compressed format. So a decompression command is added at the last line of ```launch/module_sam.launch```. If your own bag records the raw image data, please comment this line out.

**New:** more datasets are available at [LVI-SAM-Easyused](https://github.com/Cc19245/LVI-SAM-Easyused).

---

## Run the package

1. Run the launch file:
```
roslaunch lvi_sam run.launch
```
2. Play existing bag files:
```
rosbag play handheld.bag 
```

---

## Related Packages

  - [LVI_SAM_fixed by epicjung](https://github.com/epicjung/LVI_SAM_fixed)
  - [LVI-SAM-modified by skyrim835](https://github.com/skyrim835/LVI-SAM-modified)
  - [LVI-SAM-Easyused by Cc19245](https://github.com/Cc19245/LVI-SAM-Easyused)

---

## Acknowledgement
[(https://github.com/TixiaoShan/LVI-SAM)]
