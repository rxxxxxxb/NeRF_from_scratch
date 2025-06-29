# NeRF from scratch: Minimal Working Example

This repo contains minimal, self-contained PyTorch implementation of NeRF that demonstrates the core NeRF concepts on the Blender 'ficus' dataset. 
This is inspired by the [TinyNeRF tutorial](https://github.com/bmild/nerf/tree/master) and is ideal for learning and experimentation.


The process will involve two main parts:

- Single-Image Training: We will first explore how NeRF works by training it on a single image.
- Multi-Image Training: We will subsequently extend the training to multiple images captured from multiple angles.


Important concepts related to NeRF : 
- Camera Pose and Intrinsics
  - Each image in a multi-view dataset has an associated camera pose (extrinsics: rotation + translation) and intrinsics (focal length, principal point, etc.) used to compute rays.


- **Signed Distance Function**
  - These are mathematical functions that take a point in space and tell how far that point is from a surface.  
- **Ray Marching / Ray Sampling**
  - NeRF models the 3D scene by casting rays from the camera into the scene and sampling points along these rays in 3D space.  
- **Volume Rendering**
  - Volume rendering combines the predicted colors and densities along each ray using a physics-inspired equation to estimate how light accumulates along the ray.
- **Positional Encoding**
  - Neural networks have difficulty representing high-frequency functions (such as fine scene details). Positional encoding transforms input coordinates into a higher-dimensional space using sinusoidal functions.    
