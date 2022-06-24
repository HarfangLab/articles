## Deep Learning Wheels

This project contains HarfangLab's wheels used in the article [Deep Learning: Who says size doesn't matter?](https://www.harfanglab.io/articles-en/how-to-run-under-5mb-deep-learning-on-windows-or-linux-edge-devices)

## Requirements

All wheels are built for python 3.8.
The `numpy-hl` wheel must be installed before the `tflite-runtime-hl` wheel.

## Wheels

### Numpy-hl

The numpy-hl 1.22.3 wheels manually modified and rebuilt for windows 64-bit, windows 32-bit and linux are available.

These wheels can be installed on the matching OS with the corresponding `pip install wheel-name`.

It will install a package `numpy-hl` that only contains numpy's core which is the bare minimum needed to run tflite's interpreter.

### Tflite-runtime-hl

The tflite-runtime 2.7.0 wheels built at HarfangLab for windows 64-bit and windows 32-bit are available. We also added the official tflite-runtime wheel for linux (which can be found on the official [pypi](https://pypi.org/project/tflite-runtime/)).

These wheels all have for dependency `numpy-hl` (see above) instead of `numpy`.

These wheels can be installed on the matching OS, once `numpy-hl` has been installed, with `pip install wheel-name`.

It will install a package `tflite-runtime-hl` that can be used just like `tflite-runtime`.