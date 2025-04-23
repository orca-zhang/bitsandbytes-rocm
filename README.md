# `bitsandbytes`

[![Downloads](https://static.pepy.tech/badge/bitsandbytes)](https://pepy.tech/project/bitsandbytes) [![Downloads](https://static.pepy.tech/badge/bitsandbytes/month)](https://pepy.tech/project/bitsandbytes) [![Downloads](https://static.pepy.tech/badge/bitsandbytes/week)](https://pepy.tech/project/bitsandbytes)

The `bitsandbytes` library is a lightweight Python wrapper around CUDA custom functions, in particular 8-bit optimizers, matrix multiplication (LLM.int8()), and 8 & 4-bit quantization functions.

The library includes quantization primitives for 8-bit & 4-bit operations, through `bitsandbytes.nn.Linear8bitLt` and `bitsandbytes.nn.Linear4bit` and 8-bit optimizers through `bitsandbytes.optim` module.

There are ongoing efforts to support further hardware backends, i.e. Intel CPU + GPU, AMD GPU, Apple Silicon, hopefully NPU.

**Please head to the official documentation page:**

**[https://huggingface.co/docs/bitsandbytes/main](https://huggingface.co/docs/bitsandbytes/main)**

## License

`bitsandbytes` is MIT licensed.

We thank Fabio Cannizzo for his work on [FastBinarySearch](https://github.com/fabiocannizzo/FastBinarySearch) which we use for CPU quantization.

## Build for ROCm

``` sh
export PATH=/opt/rocm/bin:$PATH
export CMAKE_PREFIX_PATH=/opt/rocm
cmake -DCMAKE_CXX_COMPILER=hipcc -DCOMPUTE_BACKEND=rocm -B build . && cmake --build build
```