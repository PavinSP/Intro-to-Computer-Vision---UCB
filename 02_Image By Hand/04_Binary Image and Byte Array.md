# Binary Image and Byte Array

## Key Facts

- 8 bits are in a byte
- Range of byte array is 0-255

## Binary Images and Byte Arrays Made Simple

Imagine you have a picture made up of tiny dots called pixels. In a binary image, each pixel is like a simple light switch that can only be ON or OFF, represented by 1 or 0. For example, if you want to highlight all pixels brighter than a certain level, say 3, you turn those pixels ON (1) and the rest OFF (0). So, pixels with values like 4, 5, 6, or 7 become 1, and those with 3 or less become 0. This way, you create a clear black-and-white image based on your condition.

Now, think about a byte array as a row of tiny boxes, each holding a number from 0 to 255 (because a byte has 8 bits, and 2 to the power of 8 is 256). These numbers represent pixel brightness in a grayscale image, where 0 is completely black and 255 is pure white. For example, a row might look like this: 255 (bright white), 0 (black), 128 (medium gray). By arranging these numbers in rows and columns, you form a grayscale image where each pixel has a shade of gray.

## Q&A

### What is the range of values in a byte array and why?

The range of values in a byte array is from 0 to 255.

This is because:
- A byte consists of 8 bits.
- Each bit can be either 0 or 1.
- The total number of combinations for 8 bits is (2^8 = 256).
- Since counting starts from 0, the values go from 0 up to 255 (which is 256 values in total).

This range allows each byte to represent an integer within that span, commonly used to represent pixel intensity in images.

### How does the byte array range apply to image processing?

- Each pixel in a grayscale image is often stored as a byte.
- The value of the byte (0 to 255) represents the brightness of that pixel.
- 0 means the pixel is completely black.
- 255 means the pixel is completely white.
- Values in between represent different shades of gray.
- By arranging these bytes in a matrix (rows and columns), you create the full grayscale image.
- This allows computers to efficiently store and manipulate images using these byte values.
- This concept is fundamental in computer vision for tasks like image filtering, enhancement, and analysis.

## Example: Thresholding in Medical Imaging for Tumor Detection

**Context:** In medical imaging, such as MRI scans, images are often represented as byte matrices where each pixel's intensity is stored as a value between 0 and 255 (an 8-bit byte). These values indicate different tissue densities.

**Operation:** To highlight potential tumors, a thresholding operation is applied. For instance, pixels with intensity values greater than a certain threshold (say 100) are set to 1 (white), indicating suspicious areas, while others are set to 0 (black), representing normal tissue.

**Why Relevant:** This operation converts the grayscale byte matrix into a binary image, making it easier for doctors and AI algorithms to focus on areas of interest quickly.

**Connection to Concept:** This example shows how the byte array (with values 0-255) is processed by applying a condition (greater than threshold) to create a binary image, exactly like the example in the content where pixels greater than 3 were set to 1.
