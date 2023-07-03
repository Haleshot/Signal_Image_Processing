# Spatial and Grey Level Resolution in Python

## Aim

The aim of this project is to apply spatial and grey level resolution techniques on a test image to obtain new images. The objectives include:

a. Apply grayscale resolution on the test image to obtain a new image.
   - Calculate the compression ratio between the test image and the new image.
   - Comment on the subjective quality of the image for various levels of grayscale resolution.

b. Apply sampling resolution on the test image to obtain a new image.
   - Calculate the compression ratio between the test image and the new image.
   - Comment on the subjective quality of the image for various down-sampling rates.

## Table of Contents

- [Aim](#aim)
- [Software](#software)
- [Prerequisite](#prerequisite)
- [Outcome](#outcome)
- [Theory](#theory)
  - [Spatial Resolution](#spatial-resolution)
  - [Grey Level Resolution](#grey-level-resolution)
- [Algorithm](#algorithm)

## Software

This project is implemented using Python.

## Prerequisite

To understand and work with this project, you should be familiar with the following concepts:

| Sr. No | Concepts                          |
| ------ | --------------------------------- |
| 1.     | Spatial resolution and grey level resolution |

## Outcome

After successful completion of this experiment, students will be able to:

1. Understand the effect of varying spatial resolution.
2. Understand the effect of varying grey level resolution.

## Theory

### Spatial Resolution

The term spatial resolution corresponds to the total number of pixels in the given image. Increasing the number of pixels improves the resolution of the image, while decreasing the number of pixels reduces the resolution.

Down-sampling: In this technique, the number of pixels in the given image is reduced depending on the sampling frequency, resulting in decreased resolution and image size.

Up-sampling: The number of pixels in a down-sampled image can be increased using up-sampling interpolation techniques. Up-sampling increases both the resolution and the size of the image. Some commonly used up-sampling techniques include nearest neighbour interpolation, bilinear interpolation, and cubic interpolation.

### Grey Level Resolution

Grey level resolution of an image depends on the number of bits required to represent each pixel. In a regular 8-bit image, each pixel is represented by 8 bits, allowing for grey levels ranging from 0 to 255. Reducing the number of bits required to represent each pixel decreases the grey level resolution.

## Algorithm

The algorithm for applying spatial and grey level resolution techniques is as follows:

Spatial Resolution: Down-sampling
1. Read the original image.
2. Select a down-sampling rate, fs.
3. The new image will consist of pixels as follows:
   - After the pixel in the first column, select every pixel after fs columns.
   - After the first row, select every pixel after fs rows.

Spatial Resolution: Up-sampling
1. Read the down-sampled image.
2. Select the up-sampling rate, fs.
3. Create a new image filled with zeros, with the size of the original image.
4. Fill this new image with pixel values from the down-sampled image by skipping rows and columns at a rate of fs.
5. The remaining values in the new image can be filled using a neighbourhood averaging technique.

Grey Level Resolution
1. Read the original image.
2. Let the number of bits needed to represent each pixel in the original image be k, with a maximum grey level of 2^k.
3. Let the number of bits needed to represent each pixel in the new image be b, with a maximum grey level of 2^b.
4. Let the pixel in the original image be referred to as r.
5. Then, the pixel in the new image corresponding to the pixel in the original image will be mapped as follows:

   ```s[i, j] = ((2^b - 1) / (2^k - 1)) * r[i, j]```

Note: The code implementation is provided in the ipynb file.