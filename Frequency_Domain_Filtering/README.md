# Frequency Domain Filtering with Butterworth Filter

## Aim

The aim of this project is to implement a suitable frequency domain Butterworth filter to blur the given test image. The objectives include:

- Implementing the Butterworth filter in the frequency domain.
- Changing the filter order and summarizing the findings when the filter order increases.

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

| Sr. No | Concepts                                |
| ------ | --------------------------------------- |
| 1.     | Frequency domain filtering concepts      |

## Outcome

After successful completion of this experiment, students will be able to:

- Implement frequency domain filtering using the Butterworth filter.
- Comprehend the effects of frequency domain filtering on an image.
- Summarize the findings when the filter order increases.

## Theory

### Basic steps in frequency domain filtering:

1. Multiply the input image by (-1)^(x+y).
2. Compute the Discrete Fourier Transform (DFT) of the image obtained in step (1) to obtain F(u,v).
3. Multiply F(u,v) by a filter function H(u,v).
4. Compute the inverse DFT of the result obtained in step (3).
5. Take the real part of the result obtained in step (4).
6. Multiply the result in (5) by (-1)^(x+y).

### Butterworth Filter:

For Butterworth High Pass Filter (HPF):

H(u,v) = 1 / [1 + (D_0 / D(u,v))^2n]

For Butterworth Low Pass Filter (LPF):

H(u,v) = 1 / [1 + (D(u,v) / D_0)^2n]

where:
- D(u,v) is the distance from the point (u,v) to the origin of the frequency rectangle for an MxN image.
- D(u,v) = [(u - M/2)^2 + (v - N/2)^2]^0.5
- D_0 is the cutoff frequency.
- n is the filter order.

The filter transfer function H(u,v) is the filter response in the frequency domain.

Note: The code implementation is provided in the ipynb file.