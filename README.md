| <img width="200" alt="kabaddi_api_logo" src="https://github.com/user-attachments/assets/0db53696-7212-47be-befd-abd803126286"> | <h2 align="center">SathurangamPy - A Comprehensive Python Library Exclusive for OpenCv</h2><p align="center"><a href="#Demo">View Demo</a></p> |
|:---:|:---|

<!--[![License](https://img.shields.io/pypi/l/sathuran.svg)](https://github.com/kabaddiPy/kabaddiPy/blob/main/LICENSE)
[![PyPI version](https://badge.fury.io/py/kabaddiPy.svg)](https://badge.fury.io/py/kabaddiPy)
[![Python Versions](https://img.shields.io/pypi/pyversions/kabaddiPy.svg)](https://pypi.org/project/kabaddiPy/) -->

---

`Sathurangam is a Python library for OpenCV, simplifying tasks like edge detection, grayscale conversion, cropping, and rotation with a single line of code for all level of users`

## Installation 

install the package `sathurangamPy` using pip:


```shell
pip install sathurangam
```

Deployed here: https://pypi.org/project/sathurangam/

## Flow Diagram

<div align=center">
</div>


## Usage

Here's a quick example to getting started with `sathurangamPy` package:


```python
import sathurangamPy as sp
import cv2

path = "image.png/jpg"

#Convert image to grayscale
gray = sp.grayscale_converter(path)

cv2.imshow('gray',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Features

SathurangamPy provides a wide range of tools for handling OpenCV image processing tasks. Some of its key features include:

### Image Cropping:

```python
crop = sp.image_crop(path,50, 50, 200, 200)
```

### Image Rotation:

```python
rotate_img = sp.image_rotate(path,-45)
```

### Image Blurring :

```python
blur_img = sp.image_blur(path, 7)
# Error handling when an invalid kernel size occurs(even number)
```

### Binary Thresholding:

```python
binary_threshold = sp.bin_threshold(path,127)
```


The library offers simple methods for image manipulations, making it a versatile tool for developers. 
allowing complex operations with minimal code, and handles image display without needing `waitKey()` or `destroyAllWindows()`


## Requirement:

make sure to opencv is installed on your system

```python
pip install opencv-python
```

## License

This project is licensed under the MIT License


## Contact

Reach out me [Sherin Nishara S](mailto:sherinars2004@gmail.com)
---

<p align="center">
  Made with ❤️ sherin
</p>
