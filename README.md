# Mujoco-YCB-Dataset
Tools to download models from the [YCB dataset](https://www.ycbbenchmarks.com/) and use them with the MuJoCo simulator.

## Setup

```
pip install mujoco
pip install obj2mjcf==0.0.8
pip install mediapy
```

## Downloading YCB objects

You can download the models using a variant of the download script provided on the [http://ycb-benchmarks.s3-website-us-east-1.amazonaws.com/]. However, this script has been modified to work with Python 3.

```
python ycb_downloader.py
```

You can configure a few options in the script, including choosing which objects and model types to download. However, the default options will get all of the YCB object models and may take a few minutes to download.

## Using YCB Object Models in MuJoCo

After you have downloaded the YCB models, you can run the following jupyer-notebook files.

1. [Convert YCB datasets to MJCF format](https://github.com/joonhyung-lee/mujoco-ycb-dataset/blob/main/dataset_merge.ipynb)
2. [Visualize the objects in Mujoco](https://github.com/joonhyung-lee/mujoco-ycb-dataset/blob/main/render_mujoco.ipynb)

**NOTE:** A few of the models in the dataset do not have either of the `google_16k` or `tsdf` meshes available, so these will not work with MuJoCo. So the `dataset_merge.ipynb` will help you.

**NOTE:** The size, density and friction parameters of the objects are not tuned! Please carefully tune them before using.

---

This repo is modified upon https://github.com/joonhyung-lee/mujoco-ycb-dataset/tree/main.