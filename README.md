<div id="top" align="center">

# CVPR 2023 3D Occupancy Prediction Challenge
**The world's First 3D Occupancy Benchmark for Scene Perception in Autonomous Driving.**


<a href="#devkit">
  <img alt="devkit: v0.1.0" src="https://img.shields.io/badge/devkit-v0.1.0-blueviolet"/>
</a>
<a href="#license">
  <img alt="License: Apache2.0" src="https://img.shields.io/badge/license-Apache%202.0-blue.svg"/>
</a>

<img src="./figs/occupanc_1.gif" width="696px">

</div>

## Getting start！

### 1、Prepare dataset

organize as following 

```python
Occupancy3D
├── projects/
├── tools/
├── ckpts/
│   ├── r101_dcn_fcos3d_pretrain.pth
├── data/
│   ├── can_bus/
│   ├── occ3d-nus/
│   │   ├── maps/
│   │   ├── samples/     # You can download our imgs.tar.gz or using the original sample files of the nuScenes dataset
│   │   ├── v1.0-trainval/
│   │   ├── gts/
│   │   │── annotations.json
```
### 2、Generate the `info` files for training and validation

```python
python tools/create_data.py occ --root-path ./data/occ3d-nus --out-dir ./data/occ3d-nus --extra-tag occ --version v1.0-trainval --canbus ./data --occ-path ./data/occ3d-nus
```