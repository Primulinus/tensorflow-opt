# tensorflow-opt

Tensorflow. Recent snapshot, compiled with SSE4.1, SSE4.2, AVX, AVX2 and
FMA optimizations.

Gets rid of these:

    The TensorFlow library wasn't compiled to use SSE4.1 instructions, but
    these are available on your machine and could speed up CPU computations.

and provides sensible speedups on modern CPUs.
