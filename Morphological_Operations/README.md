# Morphological Operations for Noise Removal

## Aim

The aim of this project is to apply a suitable sequence of morphological operations on a given noisy fingerprint test image in order to obtain a noise-free image.

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

- Implement erosion, dilation, opening, and closing operations to remove noise from an image.

## Theory

### Dilation

Dilation is a morphological operation that expands the boundaries of objects in an image. It is defined as follows:

A ⊕ B = { Z | [(B ⊖ Z) ∩ A] ∈ A }

In the above equation, A represents the image, and B is the structuring element. The symbol ⊕ denotes dilation. The operation involves taking the reflection of B about its origin and shifting it by Z. Dilation of A with B yields a set of all displacements, Z, such that the overlap of (B ⊖ Z) and A contains at least one element.

### Erosion

Erosion is a morphological operation that erodes or shrinks the boundaries of objects in an image. It is defined as follows:

A ⊖ B = { Z | (B ⊖ Z) ∈ A }

In the above equation, A represents the image, and B is the structuring element. The symbol ⊖ denotes erosion. The operation involves taking the reflection of B about its origin and shifting it by Z. Erosion of A by B yields a set of all points where B, translated (shifted by Z), is entirely contained within A. Erosion reduces the number of pixels from the object boundary.

### Opening

Morphological opening of an image is performed by first applying erosion followed by dilation:

A ∘ B = OPEN(A, B) = D(E(A))

In the above equation, A represents the image, B is the structuring element, D represents the dilation operation, and E represents the erosion operation. The symbol ∘ denotes opening. Opening is useful for removing noise and fine details from the image while preserving the overall shape of objects.

### Closing

Morphological closing of an image is performed by first applying dilation followed by erosion:

A ∙ B = CLOSE(A, B) = E(D(A))

In the above equation, A represents the image, B is the structuring element, D represents the dilation operation, and E represents the erosion operation. The symbol ∙ denotes closing. Closing is useful for filling small holes and gaps in objects while preserving their overall shape.

To remove noise from the given image, it is recommended to apply opening and closing operations in the correct order. This helps in reducing the noise and improving the overall quality of the image.

Note: The code implementation is provided in the ipynb file.
