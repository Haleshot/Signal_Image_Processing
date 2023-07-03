# Image Classification and Histogram Equalization

## Aim

The aim of this project is to classify test images as low contrast, high contrast, dark, and bright images by plotting their histograms. The objectives include:

- Implementing histogram equalization on the low contrast, dark, and bright images.
- Examining the effect of equalization on the test images by comparing the histograms of the original images with the equalized images.

## Table of Contents

- [Aim](#aim)
- [Software](#software)
- [Prerequisite](#prerequisite)
- [Outcome](#outcome)
- [Theory](#theory)

## Software

This project is implemented using Python.

## Prerequisite

To understand and work with this project, you should be familiar with the following concepts:

| Sr. No | Concepts                                    |
| ------ | ------------------------------------------- |
| 1.     | Histograms for various types of images       |
| 2.     | Histogram equalization                       |

## Outcome

After successful completion of this experiment, students will be able to:

- Understand the concept of histograms and their role in image classification.
- Implement histogram equalization for enhancing image contrast.

## Theory

### Histogram

A histogram is a graph that represents the distribution of pixel intensities in an image. The x-axis represents the intensity values, and the y-axis represents the frequency of occurrence of each intensity value.

### Histogram Stretching

Histogram stretching is a technique used to enhance image contrast. It involves stretching the range of pixel intensities in an image. The modified pixel value is calculated using the following formula:

s = ((s_max - s_min) / (r_max - r_min)) * (r - r_min) + s_min

where:
- s is the modified pixel value
- s_max is the maximum grey level of the output image
- s_min is the minimum grey level of the output image
- r_max is the maximum grey level of the input image
- r_min is the minimum grey level of the input image
- r is the original pixel value

### Histogram Equalization

Histogram equalization is a technique used to redistribute the intensity values in an image to achieve a more uniform histogram. The steps involved in histogram equalization are as follows:

1. Plot the histogram of the original image.
2. Calculate the probability density function (PDF) of the image.
3. Calculate the cumulative distribution function (CDF) of the image.
4. Perform mapping of pixel values based on the CDF to obtain the output image.
5. Plot the histogram of the output image.

Note: The code implementation is provided in the ipynb file.