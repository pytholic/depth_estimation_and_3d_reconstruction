# Setup
Follow instruction on Midas [github](https://github.com/isl-org/MiDaS) for setting up the environment. Then install Open3D.

```shell
conda create -n <env_name>
conda activate <env_name>

conda install pytorch torchvision opencv
pip install timm

conda install -c open3d-admin open3d
```

# Usage

## Depth Estimation
Run the following command in terminal for estimating `depth`.

```shell
python run.py --model_type dpt_large --input_path <path to input images directory> --output_path <path to output images directory>
```

## 3D Reconstruction
Open **jupyter notebook** and run `main.ipynb` step by step for 3D reconstruction.

# Notes
You will need **camera intrinsics matrix** for this to work. You can calobrate your camera to get the matrix, or you can use some libraries like [COLMAP](https://github.com/colmap/colmap) to get it. I did both. I calibrated to get the matrix, and also used `COLMAP` parts from the **instant-ngp** [github](https://github.com/NVlabs/instant-ngp) to get the camera intrinsics.