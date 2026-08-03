# Double Image

## Key Facts

- The range of double array is -3.4 x 10^38 to 3.4 x 10^38
- The range of normalized double array is 0-1

## Why We Need Normalized Double Arrays in Image Processing

In computer vision, images are often represented as arrays of numerical values.
These arrays are typically of the data type double, which has a range of approximately -3.4 x 10^38 to 3.4 x 10^38.
However, when working with images, we often need to perform operations such as scaling, normalization, or other mathematical operations that require the data to be within a specific range, typically 0 to 1.
This is where the concept of normalized double arrays comes into play.

A normalized double array is a double array that has been scaled to a range of 0 to 1.
This is done by dividing each element of the array by the maximum value in the array.
For example, if we have an array of double values, we can normalize it by dividing each element by the maximum value in the array.
The resulting normalized double array will have values between 0 and 1, which can then be used for various image processing operations.
This is particularly useful in applications such as image enhancement, filtering, and other mathematical operations that require the data to be within a specific range.

## Understanding Double Arrays and Normalization in Images (Simple Terms)

Imagine you have a collection of numbers that represent an image, but instead of simple whole numbers, these numbers can be decimals, both positive and negative, and can be very small or very large. This collection is called a "double array." Think of it like a set of temperature readings from different places, where some might be below zero (negative), some might be just a little above zero, and some might be very high. When we want to turn this collection into an image, we arrange these numbers into rows and columns, like a grid, so the image can be displayed properly.

Now, sometimes these numbers can be all over the place — some very big, some very small, some negative. To make the image easier to work with, especially for things like showing probabilities (which are always between 0 and 1), we "normalize" the numbers. Normalization is like adjusting all the temperatures so they fit nicely between 0 and 1, kind of like converting all temperatures to a scale from freezing (0) to boiling (1). This way, the image data becomes more consistent and easier to analyze or display.

## How to Normalize a Double Array Practically

To normalize a double array practically, you typically follow these steps:

1. Find the minimum and maximum values in the array.
2. Subtract the minimum value from every element in the array. This shifts the range so the smallest value becomes 0.
3. Divide each result by the range (which is max - min). This scales all values to be between 0 and 1.

In formula form, for each element x in the array:

```
normalized_x = (x - min) / (max - min)
```

This process ensures all values fit between 0 and 1, which is useful for image processing and probability maps.

## Converting and Normalizing Double Arrays: A Simple Explanation

In this part of the course, we learned about using double arrays to represent images. Unlike byte arrays that only hold whole numbers between 0 and 255, double arrays can hold decimal numbers, both positive and negative, and even very large or very small values. This flexibility allows us to represent more detailed information, like probabilities or measurements that aren't just whole numbers.

Imagine you have a list of numbers like -0.05, -0.3, 4305, -3.4, 0, and 3.2. We can organize these numbers into rows and columns to form an image-like structure called a "double image matrix." But sometimes, these numbers can be very large or negative, which makes it hard to work with them directly. So, we "normalize" the array, which means we adjust all the numbers to fit between 0 and 1. Think of it like resizing a picture to fit perfectly inside a frame — no part is too big or too small. This is especially useful when dealing with probabilities, which always range from 0 and 1.

## Converting and Normalizing Double Arrays: A Step-by-Step Example

Let's take the example numbers and see how they get converted into a normalized image matrix. Our starting values are:

```
-0.05, -0.3, 4305, -3.4, 0, 3.2
```

### Step 1: Identify the Minimum and Maximum Values

First, we look at all the numbers to find the smallest (minimum) and largest (maximum) values.

- Minimum: -3.4 (the most negative number)
- Maximum: 4305 (the largest positive number)

### Step 2: Shift the Range (Subtract Minimum)

Next, we subtract the minimum value (-3.4) from every number in the list. This shifts our range so that the smallest number becomes 0.

```
-0.05 - (-3.4) = 3.35
-0.3  - (-3.4) = 3.1
4305  - (-3.4) = 4308.4
-3.4  - (-3.4) = 0
0     - (-3.4) = 3.4
3.2   - (-3.4) = 6.6
```

Now our numbers are: 3.35, 3.1, 4308.4, 0, 3.4, 6.6

### Step 3: Scale to 0-1 Range (Divide by Range Size)

Our new range of numbers goes from 0 to 4308.4. To make them fit between 0 and 1, we divide each number by the total size of this range (which is 4308.4).

```
3.35    / 4308.4 ≈ 0.00078
3.1     / 4308.4 ≈ 0.00072
4308.4  / 4308.4 = 1.0    (the maximum value becomes 1)
0       / 4308.4 = 0.0    (the minimum value becomes 0)
3.4     / 4308.4 ≈ 0.00079
6.6     / 4308.4 ≈ 0.00153
```

**Resulting Normalized Values:**
`0.00078, 0.00072, 1.0, 0.0, 0.00079, 0.00153`

These numbers now all fall between 0 and 1, making them perfect for use in image processing or probability maps where consistent ranges are important.

The denominator (the range) is calculated from the original, unshifted array: range = max - min.

To visualize this, imagine a number line.
- Original values range from -3.4 to 4305.
- Step 2 shifts this range to start at 0, so it becomes 0 to 4308.4.
- Step 3 then squishes this range to fit perfectly between 0 and 1.

Each number is scaled proportionally, so the relative differences between values are preserved.

So basically the denominator is the range between the max and the min value of the original array. The min value only becomes 0 after the shift step (Step 2) — it is not 0 in the original array.

### Example

```
Values: 2, 4, 6
Min: 2, Max: 6
Range: 6 - 2 = 4

2 - 2 = 0
4 - 2 = 2
6 - 2 = 4

Normalized: 0/4, 2/4, 4/4 = 0, 0.5, 1
```
