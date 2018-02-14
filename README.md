# tensorflow-opt

Tensorflow 1.6.0rc. CUDA version.

Compiled with SSE4.1, SSE4.2, AVX, AVX2 and FMA optimizations, for Python3.

Gets rid of these:

    The TensorFlow library wasn't compiled to use SSE4.1 instructions, but
    these are available on your machine and could speed up CPU computations.

and provides sensible speedups on modern CPUs.

Tested on Ubuntu 17.10; probably works on other modern distributions as well.

Required dependencies:

```sh
wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1704/x86_64/cuda-repo-ubuntu1704_9.0.176-1_amd64.deb

dpkg -i *deb

sudo apt-key adv --fetch-keys \
  http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/7fa2af80.pub

apt update

apt install cuda-9.0 -y

echo 'export CUDA_HOME=/usr/local/cuda' >> ~/.bashrc
echo 'export PATH=$PATH:$CUDA_HOME/bin' >> ~/.bashrc
echo 'export LD_LIBRARY_PATH=$CUDA_HOME/lib64' >> ~/.bashrc

source ~/.bashrc
```

CUDNN is also required. It can be downloaded here:
https://developer.nvidia.com/cudnn

The exactly file you want is `cudnn-9.0-linux-x64-v7.tgz`

```sh
tar xzf cudnn-9.1-linux-x64-v7.tgz
sudo cp cuda/lib64/* /usr/local/cuda/lib64/
sudo cp cuda/include/cudnn.h /usr/local/cuda/include/
```

Uncompress the `.tar.xz` file, run `pip install *.whl` and there you go.
