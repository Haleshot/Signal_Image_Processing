# Image Morphological Operations

## Aim

The aim of this project is to perform erosion on the given test image using different structuring elements. The structuring elements include a square-shaped structuring element of sizes 11x11, 15x15, and 45x45, as well as a circular-shaped structuring element of the same sizes. Additionally, the project involves analyzing the effect of changing the structuring element and increasing its size on the eroded image. Finally, dilation is performed on the given test image with broken text characters using a suitable structuring element to demonstrate the joining of the broken segments.

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

| Sr. No | Concepts                               |
| ------ | -------------------------------------- |
| 1.     | Morphological operations (dilation, erosion, opening, and closing) |

## Outcome

After successfully completing this experiment, students will be able to:

- Implement dilation and erosion operations on images.
- Analyze the effects of changing the size and shape of the structuring element on the eroded image.

## Theory

### Dilation

Dilation is a morphological operation that expands the boundaries of objects in an image. It is defined as follows:

A ⊕ B = { Z | [(B ⊖ Z) ∩ A] ∈ A }

In the above equation, A represents the image, and B is the structuring element. The symbol ⊕ denotes dilation. The operation involves taking the reflection of B about its origin and shifting it by Z. Dilation of A with B yields a set of all displacements, Z, such that the overlap of (B ⊖ Z) and A contains at least one element.

### Erosion

Erosion is a morphological operation that erodes or shrinks the boundaries of objects in an image. It is defined as follows:

A ⊖ B = { Z | (B ⊖ Z) ∈ A }

In the above equation, A represents the image, and B is the structuring element. The symbol ⊖ denotes erosion. The operation involves taking the reflection of B about its origin and shifting it by Z. Erosion of A by B yields a set of all points where B, translated (shifted by Z), is entirely contained within A. Erosion reduces the number of pixels from the object boundary.

Note: The code implementation is provided in the ipynb file.
