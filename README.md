# PyTorch-vs-TensorFlow
Example models in both PyTorch and TensorFlow to handle the well known MNIST series of datasets.

## Main Dependencies

Conda:
```bash
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -o Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
conda create --name pt
conda create --name tf
```

PyTorch: 1.10.2
```bash
conda activate pt
pip install torch torchvision
pip install sklearn
# verify CUDA was linked properly
python3 -c "import torchvision; print('Module loaded successfully')"
```
TensorFlow: 2.10.0
```bash
conda activate tf
conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/
python3 -m pip install tensorflow
# Verify install:
python3 -c "import tensorflow as tf; print(tf.config.list_physical_devices('GPU'))"
```

## Usage
* Clone the repo and run either the 'PyTorch-MNIST.py'(WIP) or 'TF-MNIST.py' files
* Output will be in the terminal
