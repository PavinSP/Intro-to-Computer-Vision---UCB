# Practice Assignment: RGB Image Q&A

Practice session with Coursera AI on computer vision concepts (RGB channels, bit depth, and color counts).

## Q1: How does an RGB image represent colors using its three channels?

**My answer:** RGB has 3 channels one for red, one for green and one for blue. Each pixel in an image is represented by 3 numbers from these 3 channels, for example red is represented by 255 0 0.

**Feedback:** Correctly identified that RGB images have three channels—red, green, and blue—and that each pixel is represented by three numbers corresponding to these channels.

## Q2: How do the three channel values combine to create colors beyond pure red, green, or blue? What is the significance of 255?

**My answer:** When two colors are mixed we get different colors from R, G, and B — for example cyan is got by 0, 255, 255. The number 255 means white and it is 2 to the power 8, and it is the maximum range.

**Feedback:** Correctly identified that mixing different intensities of red, green, and blue channels produces various colors, like cyan from green and blue at full intensity (0, 255, 255). Correctly noted that 255 is the maximum value for an 8-bit channel (2⁸ − 1).

**Clarification:** 255 itself doesn't mean white — rather, when all three channels are at 255 (255, 255, 255), the resulting color is white. Each channel's intensity contributes to the overall color.

## Q3: What color results from RGB values (255, 255, 0)? Why?

**My answer:** Yellow, because red and green gives yellow.

**Feedback:** Correct — when red and green channels are at full intensity (255) and blue is zero, the resulting color is yellow.

## Q4: Why does each channel use a byte (8 bits) to represent intensity? What advantages does this provide?

**My answer:** idk

**Hint given:** Think about what 8 bits per channel means in terms of the number of possible intensity levels. How might having 256 levels (0–255) per channel impact color detail and smoothness? Also consider how using a byte per channel affects image data size.

**My follow-up answer:** It can tell the image quality in detail because representing with 255 numbers is vast, and idk about the size part.

**Feedback:** Using 8 bits per channel allows each channel to represent 256 different intensity levels, capturing fine gradations in color and brightness for smoother transitions and more detail. Using a byte per channel also standardizes how image data is stored and processed, making it efficient for computers to handle. More bits per channel increases image quality but also file size; fewer bits reduce file size but can cause color banding or loss of detail.

## Q5: How does 8-bit depth per channel balance image quality and data size?

**My answer:** 8 bit depth per channel retains quality for affordable size.

**Feedback:** Correct — 8-bit depth per channel strikes a balance by providing enough color detail (256 levels per channel) to produce high-quality images while keeping data size manageable for storage and processing.

## Q6: How many total possible colors can each pixel represent in an 8-bit-per-channel RGB image?

**My answer (attempt 1):** Each pixel can represent only one color.

**Feedback:** Correct that each pixel represents one color at a time, but the question asks how many *different* colors that single pixel can represent given the 8-bit depth per channel.

**My answer (attempt 2):** Total number of colors would be permutation of 0-255, 0-255, 0-255.

**Feedback:** On the right track thinking about the ranges for each channel, but the total number of colors is calculated by **multiplying** the number of possible intensity values per channel, not permutations:

```
256 (Red) × 256 (Green) × 256 (Blue)
```

**My answer (attempt 3):** 16,908,288

**Feedback:** Close, but not quite right. Worked through step by step:

```
256 × 256 = 65,536
65,536 × 256 = ?
```

**My answer (attempt 4):** 16,777,216

**Feedback:** Correct! **16,777,216** is the total number of colors an 8-bit-per-channel RGB image can represent per pixel, from 256 × 256 × 256 = 16,777,216.

## Q7: Why is 8-bit depth per channel a common standard? Advantages and limitations?

**My answer:** idk, you tell me.

**Answer given:**

Using 8 bits per channel means each channel can represent 256 intensity levels, allowing for over 16 million total colors. This provides a good balance between:

- **Color richness:** Enough colors to represent images with smooth gradients and realistic colors.
- **File size and processing:** 8 bits per channel keeps image file sizes manageable and processing efficient compared to higher bit depths.

**Limitation:** 8 bits might not capture extremely subtle color variations or very high dynamic range scenes perfectly.
