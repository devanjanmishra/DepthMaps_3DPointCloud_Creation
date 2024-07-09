# 3D Point Cloud Creation for an Image using Monocular Depth Estimation
Calculate 3D point cloud from an image by estimating the depth of objects in the image and the projecting the depth in 3D using camera intrinsic parameters.

## Benchmark  Monocular Depth Estimation Model:  
Based on my research and recent developments in available monocular depth estimation, two models were selected:
   1) [Depth Anything Model-V2](https://github.com/LiheYoung/Depth-Anything)
   2) [Metric3D](https://github.com/YvanYin/Metric3D/tree/main)

Both the models offer great depth accuracy, but Metric 3D model stood out for me with the provided [configurations](https://github.com/devanjanmishra/DepthMaps_3DPointCloud_Creation/tree/main/mono/configs) for different conditions.

Metric3D models also provides with normal estimations from the model itself, rather relying on external libraries like opencv,open3d which is an additional benefit.
Sample Inclusion from [output](https://github.com/devanjanmishra/DepthMaps_3DPointCloud_Creation/tree/main/data/sample_output):

![image](https://github.com/devanjanmishra/DepthMaps_3DPointCloud_Creation/assets/50066136/27715284-7058-4cf1-9e68-531a5f0a0e8e)  


## Projecting Depth Map in 3D
The depth map, RGB image and Normal image are scaled down to reduce the overall number of points in 3D point cloud.

There are two examples included currently:
#### 1) Study Table with all Point of Interests in same Relative Depth 
<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/devanjanmishra/DepthMaps_3DPointCloud_Creation/blob/main/data/sample_input/IMG20240610231531.jpg" alt="Description of image" style="width: 30%; height: 170px"/>
  <img src="https://github.com/devanjanmishra/DepthMaps_3DPointCloud_Creation/blob/main/data/sample_output/GIF_Video_IMG20240610231531.gif" alt="Description of gif" style="width: 45%;"/>
</div>  

#### 2) Study Table with Point of Interests at contrasting depth 
<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/devanjanmishra/DepthMaps_3DPointCloud_Creation/blob/main/data/sample_input/IMG20240610231100.jpg" alt="Description of image" style="width: 30%; height: 170px"/>
  <img src="https://github.com/devanjanmishra/DepthMaps_3DPointCloud_Creation/blob/main/data/sample_output/GIF_Video_IMG20240610231100.gif" alt="Description of gif" style="width: 45%;"/>
</div>

## To-Do List

- [x] Select Appropriate Depth Estimation Model.  
- [x] Create Depth Map and Normal Map using selected Monocular Depth Estimation.  
- [x] Create Point Cloud using Depth Map, Normal Map and Camera Intrinsics( Given or Previously calculated).  
- [ ] Validate Point Cloud Accuracy by comparing the dimensions in actual world and Point Cloud.

## Citations and Acknowledgments
This project uses the following resources:

- [Metric3D](https://github.com/YvanYin/Metric3D/tree/main) - For Monocular Depth Estimation Model.  
  @article{hu2024metric3dv2,
  title={Metric3D v2: A Versatile Monocular Geometric Foundation Model for Zero-shot Metric Depth and Surface Normal Estimation},
  author={Hu, Mu and Yin, Wei and Zhang, Chi and Cai, Zhipeng and Long, Xiaoxiao and Chen, Hao and Wang, Kaixuan and Yu, Gang and Shen, Chunhua and Shen, Shaojie},
  journal={arXiv preprint arXiv:2404.15506},
  year={2024}
}

## License
The Metric 3D code is under a 2-clause BSD License for non-commercial usage. For further questions, contact Dr. Wei Yin [yvanwy@outlook.com] and Mr. Mu Hu [mhuam@connect.ust.hk].
