# BARIM-Head-Pose-Database
BARIM Head Pose Database from the Augmented Reality & Intelligent Medicine Lab at Beijing Institute of Technology

This database consists of 24 sequences collected using the Hololens2 mixed reality device. The participants were positioned approximately 1 meter away from the device, and a total of 20 individuals were involved in the dataset collection (including two participants who were recorded twice, with one of them being female). The participants followed three rules during the data collection: 1) Keeping their heads at the same level as the device, 2) Keeping the Hololens 2 device stationary, and 3) Rotating their heads slowly.

The collected data includes frames where the participants' faces are completely occluded due to extreme head rotations. These frames had been removed, resulting in some discontinuity in the sequence. However, this does not affect the frame-by-frame pose estimation. If the data is used for tracking tasks, please be mindful of this situation.

For each sequence, there are four camera parameter files included. The "Depth Long Throw_extrinsics.txt" file contains the intrinsic matrix of the depth camera, which is the same for all sequences. The "Depth Long Throw_lut.bin" file is used to reconstruct point clouds from the depth maps. The "Depth Long Throw_rig2world.txt" and "pv.txt" files represent the global rotation and translation between the depth camera and the RGB camera. These pieces of information are used for aligning the RGB and depth data. In this dataset, the reconstructed point clouds have already been provided and aligned with the RGB data.

Each sequence contains average of 500 frames. For each frame, the dataset provides the following files: "_rgb.png", "_depth.pgm", "_mask.png", and "_pcd.ply". The point cloud data has already been aligned with the RGB images.The "_pose.txt" file provides the head pose angles for each frame. The order of the Euler angles in the file is pitch, roll, and yaw.

If you use our data, please cite the paper:

@article{
author = {Dongsheng Ma, Tianyu Fu, Yifei Yang, Kaibin Cao, Jingfan Fan, Deqiang Xiao, Hong Song, Ying Gu, Jian Yang},
title = {Fusion-Competition Framework of Local Topology and Global Texture for Head Pose Estimation}
}
