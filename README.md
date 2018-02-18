# tensorflow-opt

Tensorflow 1.6.0rc. CUDA version.

Compiled with SSE4.1, SSE4.2, AVX, AVX2 and FMA optimizations, for Python3.

Tested on Ubuntu 17.10; probably works on other modern distributions as well.

## Compatibility

* `tensorflow-1.6.0rc1-cp36-cp36m-linux_x86_64-cuda60.whl.tar.xz`: for
GPUs with compute capability 6.0. Tested on [Exoscale](https://www.exoscale.ch) GPU instances
with Tesla P100 GPUs.

* `tensorflow-1.6.0rc1-cp36-cp36m-linux_x86_64-cuda61.whl.tar.xz`: for
GPUs with compute capability 6.1. Tested on [OVH](https://www.ovh.com) Cloud GPU instances
with GTX-1080 Ti GPUs.

## Installation

Required dependencies:

```sh
wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1704/x86_64/cuda-repo-ubuntu1704_9.0.176-1_amd64.deb

dpkg -i *deb

sudo apt-key adv --fetch-keys \
  http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1704/x86_64/7fa2af80.pub

apt update

apt install -y cuda-9.0
apt install -y python3-dev python3-pip libcupti-dev pandas
```

CUDNN is also required. It can be downloaded here:
https://developer.nvidia.com/cudnn

The exactly file you want is `cudnn-9.0-linux-x64-v7.tgz`

```sh
tar xzf cudnn-9.1-linux-x64-v7.tgz
sudo cp cuda/lib64/* /usr/local/cuda/lib64/
sudo cp cuda/include/cudnn.h /usr/local/cuda/include/
```

Now, uncompress the `.tar.xz` file downloaded from this repository and run `pip3 install *.whl`
to install Tensorflow.

Additional packages you may want to install:

```sh
pip3 install keras h5py pandas
```
