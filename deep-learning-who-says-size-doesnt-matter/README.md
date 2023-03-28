## Deep Learning Wheels

This project contains HarfangLab's wheels used in the article [Deep Learning: Who says size doesn't matter?](https://www.harfanglab.io/articles-en/how-to-run-under-5mb-deep-learning-on-windows-or-linux-edge-devices)

## Requirements

`tflite_runtime-2.11.0-cp310-cp310-linux_x86_64.whl` is built for python 3.10. All other wheels are built for python 3.8

## Wheels for Python 3.8

### Numpy-hl

The numpy-hl 1.22.3 wheels manually modified and rebuilt for windows 64-bit, windows 32-bit and linux are available.

These wheels can be installed on the matching OS with `pip install wheel-name`.

It will install a package `numpy-hl` that only contains numpy's core which is the bare minimum needed to run tflite's interpreter.

### Tflite-runtime-hl

The tflite-runtime 2.7.0 wheels built at HarfangLab for windows 64-bit and windows 32-bit are available. We also added the official tflite-runtime wheel for linux (which can be found on the official [pypi](https://pypi.org/project/tflite-runtime/)).

These wheels all have for dependency `numpy-hl` (see above) instead of `numpy`.

These wheels can be installed on the matching OS, once `numpy-hl` has been installed, with `pip install wheel-name`.

It will install a package `tflite-runtime-hl` that can be used just like `tflite-runtime`.


## Wheel for Python 3.10

### Tflite-runtime 2.11.0

Additionally to what was presented in the article, we have studied using `tflite-runtime` with Python 3.10. Python 3.10 is not currently supported on Tensorflow-lite, so we built our own `linux` wheel for `tflite-runtime` on python 3.10. Please note that `numpy` with the version `1.24.2` will be necessary to run with our wheel. To date, we have not optimized the size of this version of numpy.
