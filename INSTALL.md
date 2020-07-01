Follow instructions to patch the local repo of PyTorch to avoid -Wall complaint: https://github.com/dzhulgakov/spconv#install-on-ubuntu-16041804

The fix for custom `CUDA_ROOT` is applied from https://github.com/traveller59/spconv/issues/78

```
conda install cmake cudnn boost
conda install -c conda-forge cudatoolkit-dev
CUDA_ROOT=$CONDA_PREFIX python setup.py bdist_wheel
pip install dist/*
# test
python example/mnist_sparse.py
```
