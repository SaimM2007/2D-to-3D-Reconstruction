# 2D-to-3D-Reconstruction
This project demonstrates a complete 2D-to-3D image reconstruction pipeline using deep learning and 3D vision libraries. It takes a single RGB image and generates a depth map, point cloud, and mesh reconstruction.

Overview:
The system leverages Intel’s MiDaS model for monocular depth estimation, powered by PyTorch, and integrates Open3D for 3D geometry processing and visualization. It can process any single RGB image (provided the link), predict relative depth information, and generate 3D reconstructions in both point cloud and mesh formats.

Features:
- Single-image depth prediction using MiDaS (DPT-Large)
- 3D point cloud generation from RGB-D data
- Surface reconstruction with Poisson meshing
- Outlier removal and normal estimation for better surface quality
- Full GPU acceleration using CUDA (if available for user)

Tech Stack:
- Python – Core programming language
- PyTorch – Deep learning framework for MiDaS inference
- Open3D – 3D geometry processing and mesh reconstruction
- NumPy – Data manipulation
- Matplotlib – Visualization of depth maps
- OpenCV – Image preprocessing and color conversion
- PIL – Image handling and resizing

Installation:
- pip install torch torchvision torchaudio timm opencv-python matplotlib open3d

Usage:
- Run "2D_to_3D.ipynb"'s code in a Python environment (or Google Colab)

To download the generated 3D mesh when using Colab and view it:
- Run: from google.colab import files, then files.download("mesh/output_mesh.obj")
- To see the obj, you can use a website like https://3dviewer.net/
  
Output:
- Predicted Depth Map – Visual representation of scene depth
- Point Cloud (.ply) – Reconstructed spatial structure
- Mesh (.obj) – 3D model ready for rendering or further processing

Future Work:
- Integrate multiple-view reconstruction for higher accuracy
- Experiment with real-world datasets
- Add interactive visualization in a web app using Three.js or Plotly
