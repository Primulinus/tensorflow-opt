# tensorflow-opt

Tensorflow 1.6.0rc. CUDA version.

Compiled with SSE4.1, SSE4.2, AVX, AVX2 and FMA optimizations, for Python3.

Gets rid of these:

    The TensorFlow library wasn't compiled to use SSE4.1 instructions, but
    these are available on your machine and could speed up CPU computations.

and provides sensible speedups on modern CPUs.

Tested on Ubuntu 17.10; probably works on other modern distributions as well.

Uncompress the `.tar.xz` file, run `pip install *.whl` and there you go.
