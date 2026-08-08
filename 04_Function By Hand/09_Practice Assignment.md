# Practice Assignment: Function Q&A

Practice session with Coursera AI on 2D image functions, axis flipping, coordinate transforms, and linear combination.

## Q1: How can a 2D image be represented as a mathematical function? What does this function describe about the image?

**My answer:** 2D images can be represented by a function of x and y parameters, and each pixel is the correspondence of x and y coordinates.

**Feedback:** Correctly identified that a 2D image can be represented as a function of x and y coordinates, where each pixel corresponds to a specific (x, y) position.

**Follow-up:** What does the function's output represent at each (x, y) coordinate?

**My answer:** The value that the function returns depends on the function definition, and the values represent the brightness of the image — 0 is black.

**Feedback:** Correct — the function's output at each (x, y) coordinate represents the pixel's intensity or brightness. Values of 0 correspond to black, and higher values represent brighter pixels.

## Q2: How does this function differ for a grayscale image versus an RGB image?

**My answer (attempt 1):** idk, explain in detail.

**Hint given:** For a grayscale image, the function returns a single value at each (x, y) coordinate representing brightness intensity, usually ranging from 0 (black) to a maximum value (white). For an RGB image, the function returns a set of three values at each (x, y) coordinate — one for each color channel: Red, Green, and Blue.

**My answer (attempt 2):** In a grayscale image the function returns one value for each pixel, whereas in an RGB image, instead of a single value, a set of three values will be returned by the function for each x, y coordinate.

**Feedback:** Correct — grayscale images have a single intensity value per pixel, while RGB images have three values per pixel corresponding to the red, green, and blue channels.

## Q3: To flip an image along the vertical axis, which operation would achieve this?

**Options:**
- A) Rotate the image 90 degrees clockwise
- B) Negate the x-coordinates of the image function
- C) Swap the x and y coordinates
- D) Negate the y-coordinates of the image function

**My answer (attempt 1):** D — negate the y-coordinates.

**Feedback:** Flipping along the vertical axis (y-axis) means mirroring left to right, not rotating 180 degrees. Negating the y-coordinates flips the image upside down (along the horizontal axis), not left to right.

**My answer (attempt 2):** The x-axis should be negated.

**Feedback:** Exactly right — negating the x-coordinates flips the image along the vertical axis (left to right).

## Q4: When redefining the x and y axes in image processing, which techniques might be involved? (Select all that apply)

**Options:**
- A) Rotation
- B) Translation
- C) Scaling
- D) Color inversion

**My answer (attempt 1):** A (rotation) for sure, and maybe D (color inversion).

**Feedback:** Rotation correctly identified — it changes the orientation of the coordinate system. Color inversion (D) affects pixel values but does not change the coordinate system or axes, so it doesn't belong.

**My answer (attempt 2):** Asked what translation is, and guessed C (scaling) was wrong.

**Explanation given:** Translation shifts the entire image along the x and/or y axes (sliding it without rotating or resizing) — this changes the image's position in the coordinate system but not the axes themselves. Scaling changes the image's size by stretching or shrinking along the x and y axes, which does affect how the axes are interpreted (their units/distances).

**My answer (attempt 3):** Only A is correct.

**Feedback:** Rotation (A) is correct, but translation (B) and scaling (C) also involve redefining the x and y axes:
- Rotation changes the orientation of the axes.
- Translation shifts the origin of the axes.
- Scaling changes the scale or units along the axes.
- Color inversion (D) only changes pixel values, not the axes.

**Correct answer:** A, B, and C.

## Q5: Two images are combined with coefficients 0.5 and 0.3. The pixel value at (50, 50) is 200 in the first image and 150 in the second. What's the resulting pixel value?

**My answer:** 100 + 45 = 145

**Feedback:** Correct.

```
0.5 × 200 = 100
0.3 × 150 = 45
Sum = 100 + 45 = 145
```

## Q6: What happens to the resulting image if the linear combination coefficients sum to more than 1?

**My answer:** idk, explain that.

**Answer given:**

When the coefficients in a linear combination sum to more than 1, the resulting pixel values tend to increase overall, because you're effectively amplifying the intensity of the combined images.

For example, if the coefficients sum to 1.5, the pixel values could become brighter than in the original images. This can lead to pixel values exceeding the maximum allowed intensity (often 255 in 8-bit images), causing **clipping** or **saturation** — where pixel values are capped at the maximum, potentially losing detail in bright areas.
