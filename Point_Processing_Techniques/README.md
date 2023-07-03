# Image Processing Techniques in Python

## Aim

The aim of this project is to implement various point processing and spatial domain filtering techniques on a given image and comprehend the results. The objectives include:

a. Point Processing Techniques:
   i. Write a program in Python to obtain the negative of an image.
   ii. Write a program in Python to perform thresholding on an image.
   iii. Write a program in Python to perform grey level slicing of an image without background.
   iv. Write a program in Python to perform grey level slicing of an image with background.

b. Spatial Domain Filtering:
   i. Implement blurring on the given image.
   ii. Comment on your choice of a particular filtering technique for the given image.
   iii. Analyze the effect of various mask sizes for the used filter and comprehend the findings.

## Table of Contents

- [Aim](#aim)
- [Software](#software)
- [Prerequisite](#prerequisite)
- [Outcome](#outcome)
- [Theory](#theory)
  - [Point Processing Techniques](#point-processing-techniques)
  - [Spatial Domain Filtering](#spatial-domain-filtering)

## Software

This project is implemented using Python.

## Prerequisite

To understand and work with this project, you should be familiar with the following concepts:

| Sr. No | Concepts                                      |
| ------ | --------------------------------------------- |
| 1.     | Point processing techniques for image enhancement |
| 2.     | Neighborhood processing techniques for image enhancement |

## Outcome

After successful completion of this experiment, students will be able to comprehend:

- The concept of image enhancement in the spatial domain using point processing and neighborhood processing methods.

## Theory

### Point Processing Techniques

Point processing operations are applied to individual pixel values in an image. The following techniques are implemented:

- **Image Negative:** Each pixel value is subtracted from the maximum pixel value (L-1) to obtain the negative of the image.
- **Thresholding:** Pixels with values above a specified threshold are set to the maximum pixel value (L-1), while pixels below the threshold are set to 0.
- **Grey Level Slicing without Background:** Pixels within a specific range (a to b) are set to the maximum pixel value (L-1), while all other pixels are set to 0.
- **Grey Level Slicing with Background:** Pixels within a specific range (a to b) are set to the maximum pixel value (L-1), while other pixels retain their original values.

### Spatial Domain Filtering

Spatial domain filtering involves modifying pixels by considering the values of their neighboring pixels. The following technique is implemented:

- **Low Pass Filtering (Blurring):** It removes high-frequency content from the image, resulting in a smoother image. A common mask used for low pass filtering is the averaging filter, which replaces each pixel value with the average of its surrounding pixels.

Note: The code implementation is provided in the ipynb file.
