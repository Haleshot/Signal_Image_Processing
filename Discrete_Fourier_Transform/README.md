# Discrete Fourier Transform (DFT) in Python

## Aim

The aim of this project is to obtain the twiddle factor matrix and perform the following tasks using it:

- Find the DFT and IDFT of the sequence [1, 2, 2, 1] using the twiddle factor matrix.
- Compute the DFT using matrix method and the FFT function.
- Observe and comment on the execution time required for each of the above methods.

## Table of Contents

- [Aim](#aim)
- [Software](#software)
- [Prerequisite](#prerequisite)
- [Outcome](#outcome)
- [Theory](#theory)
  - [Discrete Fourier Transform (DFT)](#discrete-fourier-transform-dft)
- [Algorithm](#algorithm)

## Software

This project is implemented using Python.

## Prerequisite

To understand and work with this project, you should be familiar with the following concepts:

| Sr. No | Concepts                     |
| ------ | ---------------------------- |
| 1.     | Discrete Fourier Transform   |

## Outcome

After successful completion of this experiment, students will be able to:

- Implement inverse and forward DFT on the given sequence.

## Theory

### Discrete Fourier Transform (DFT)

The Discrete Fourier Transform (DFT) is used for performing frequency analysis of discrete time signals. DFT provides a discrete frequency domain representation, whereas other transforms are continuous in the frequency domain.

The N-point DFT of a discrete time signal x[n] is given by the equation:

X(k) = Σ(x(n) * W<sub>N</sub><sup>nk</sup>)

Where N is chosen such that N ≥ L (length of x[n]).
The inverse DFT allows us to recover the sequence x[n] from the frequency samples.

The twiddle factor is given by:

W<sub>N</sub><sup>nk</sup> = e<sup>(-jθ)</sup> = cos(θ) - j sin(θ)

Where θ = (2πnk) / N, n = 0 to N-1, and k = 0 to N-1.

### Algorithm

The algorithm for performing the DFT using the twiddle factor matrix is as follows:

1. Assign a value for the time period, N.
2. Assign the frequency and sampling frequency.
3. Give the sampling period rate, n.
4. Define the sine function: sin(2π(f/fs)n).
5. Find the DFT using the built-in function `fft()`.
6. Find the DFT using the formula mentioned above.
7. Plot the input function.
8. Plot the DFT (absolute value) when the built-in function is used.
9. Plot the DFT (absolute value) when the DFT formula is used.
10. Display the output.

Note: The code implementation is not provided in this README file.