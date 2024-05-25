# Image Edge Detection using Sobel Operator and Averaging Filter

## Aim

The aim of this project is to apply Sobel's mask on the given test image to obtain the components of the gradient, |g_x|, |g_y|, and |g_x+g_y|. Additionally, a 5x5 averaging filter is applied on the test image followed by implementing the sequence from step a. The project concludes with summarizing the observations after comparing the results obtained in step a and b.

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

| Sr. No | Concepts        |
| ------ | --------------- |
| 1.     | Sobel operator  |

## Outcome

After successful completion of this experiment, students will be able to:

- Understand the significance of filter masks for edge enhancement.
- Implement Sobel operator for edge detection.
- Apply Sobel's mask to obtain the components of the gradient.
- Apply an averaging filter to the test image and observe the effects.
- Compare the results obtained from step a and b and summarize the observations.

## Theory

### Sobel Operator

The Sobel operator is a commonly used edge detection filter. It consists of two 3x3 masks: F_x and F_y, which are applied to the image to obtain the horizontal and vertical gradient components, respectively.

```
F_x = |-1 -2 -1|      F_y = |-1  0  1|
      | 0  0  0|            | -2 0  2|
      | 1  2  1|            | -1 0  1|
```

To apply the Sobel operator:
1. Convolve the F_x mask with the original image to obtain the x gradient of the image.
2. Convolve the F_y mask with the original image to obtain the y gradient of the image.
3. Add the results of the above two steps to obtain the combined gradient image, |g_x+g_y|.

### Averaging Filter

An averaging filter is a simple low-pass filter that helps in reducing noise and blurring the image. It involves convolving the image with a suitable filter mask.

### Observations

After applying the Sobel operator with the averaging filter and comparing the results obtained in step a and b, the following observations can be made:

- The Sobel operator enhances the edges in the image by highlighting the changes in intensity.
- The averaging filter blurs the image and reduces the noise.
- When the Sobel operator is applied after the averaging filter, the edges appear smoother and less pronounced compared to applying the Sobel operator directly on the original image.
- The combined gradient image, |g_x+g_y|, obtained from the Sobel operator shows the overall intensity changes in the image.

> [!NOTE]
>  The code implementation is not provided in this README file.
