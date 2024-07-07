# 3D Point Cloud Creation for an Image using Monocular Depth Estimation
Calculate 3D point cloud from an image by estimating the depth of objects in the image and the projecting the depth in 3D using camera intrinsic parameters.

## Benchmark  Monocular Depth Estimation Model:  
Based on my research and recent developments in available monocular depth estimation, two models were selected:
   1) [Depth Anything Model-V2](https://github.com/LiheYoung/Depth-Anything)
   2) [Metric3D](https://github.com/YvanYin/Metric3D/tree/main)

Both the models offer great depth accuracy, but Metric 3D model stood out for me with the provided [configurations](https://github.com/devanjanmishra/DepthMaps_3DPointCloud_Creation/tree/main/mono/configs) for different conditions.

Metric3D models also provides with normal estimations from the model itself, rather relying on external libraries like opencv,open3d which is an additional benefit.
Sample Inclusion from [output](https://github.com/devanjanmishra/DepthMaps_3DPointCloud_Creation/tree/main/data/sample_output):

<div style="display: flex; justify-content: space-around; align-items: flex-start;">
  <div style="text-align: center; width: 33%;">
    <p><strong>Input: RGB Image</strong></p>
    <img src="data/sample_input/IMG20240610231100.jpg" alt="Image 1" style="width: 100%;"/>
  </div>
  <div style="text-align: center; width: 34%;">
    <p><strong>Output: Depth Image</strong></p>
    <img src="data/sample_output/depth.jpg" alt="Image 2" style="width: 100%;"/>
  </div>
  <div style="text-align: center; width: 33%;">
    <p><strong>Output: Normals Image</strong></p>
    <img src="data/sample_output/normal.jpg" alt="Image 3" style="width: 100%;"/>
  </div>
</div>
