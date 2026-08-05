# Practice Assignment: RGB Image Structure Q&A

Practice session with Coursera AI on RGB image representation, byte size calculations, and LED matrix simulation.

## Q1: How is an RGB image represented as a data structure in computer vision? What are the key components?

**My answer:** In computer vision, RGB images are represented as 3 color channels where the dimensions are rows × columns × channels, so each pixel has 3 values.

**Feedback:** Correctly identified that an RGB image is represented with three color channels and that the dimensions include rows, columns, and channels — a fundamental concept in image representation.

**Follow-up:** What does each of the three channels represent, and how does this structure affect image processing?

**My answer:** These three channels represent the colors red, green, and blue. This gives spatial view to the image.

**Feedback:** Correct that the three channels correspond to red, green, and blue, which combine to create the full color image. The phrase "spatial view" needed clarification — the rows and columns (not the channels) are what define the spatial layout of the image.

**My clarified answer:** This structure represents one pixel by processing all the 3 values together, thus forming the desired color.

**Feedback:** Exactly right. Each pixel in an RGB image is defined by three values — one for red, one for green, one for blue — and combining these gives the pixel's color. The rows and columns define the spatial layout of pixels (mapping the image in a grid), while the three channels carry the color information at each pixel location.

## Q2: If you have a 10x10 RGB image, how many total values (or bytes) are needed to store it, assuming each channel value is one byte?

**My answer:** 300 values.

**Feedback:** Correct — a 10x10 RGB image has 10 rows, 10 columns, and 3 color channels: 10 × 10 × 3 = 300 values (bytes).

## Q3: Why is it important to understand the byte size of an image in image processing or computer vision? How does it affect performance or memory usage?

**My answer:** It is because the byte array of the image gives both good resolution and also affordable data size of the image. If we increase the bits to represent one pixel then we get more resolution, however it would result in huge image sizes.

**Feedback:** On the right track — byte size directly affects memory usage and computational efficiency. Larger images require more storage and processing power, slowing down algorithms and increasing resource consumption. The trade-off noted (more bits per pixel → more color precision, but bigger files) is important, with one refinement: *resolution* refers to the number of pixels (spatial dimensions), while *bits per pixel* refers to color depth (precision of color representation) — two related but distinct concepts.

## Q4: When simulating an LED display using Excel functions, what features/properties of RGB pixels are essential to arrange them correctly into a matrix that resembles an LED screen?

**My answer:** The property that 3 values equals one pixel, and arranging them in order, is essential.

**Feedback:** Good observation — grouping each pixel's three values (R, G, B) together is fundamental. Beyond that, the spatial/structural layout also matters: how the pixels are positioned relative to each other, and how the row/column matrix layout mirrors the original image.

**Hint given:** When simulating an LED matrix, it's important not only to group the RGB values per pixel but also to maintain the correct spatial arrangement — pixels placed in rows and columns matching the original image layout — so the visual representation looks like the intended image on the LED display.

**Answer:** To correctly simulate an LED display in Excel, three things need to be preserved together:

1. **Pixel grouping:** Each pixel's three values (R, G, B) must stay grouped and in the correct order, since scrambling the order within a pixel produces the wrong color.
2. **Row width (wrap size):** The row must wrap at exactly `width × 3` values (e.g., 32 pixels × 3 channels = 96 values per row for a 32-pixel-wide image). Wrapping at the wrong width shifts every pixel after the first row, distorting the whole image — the same issue covered in the RGB Image 32x32x3 notes.
3. **Row order (top-to-bottom):** Rows must be laid out in the same top-to-bottom order as the original image so the matrix's vertical position matches the source, not reversed or shuffled.

If any of these three are off — pixel grouping, row width, or row order — the LED matrix will show the right colors in the wrong places, producing a distorted or scrambled image even though the underlying pixel data is correct.
