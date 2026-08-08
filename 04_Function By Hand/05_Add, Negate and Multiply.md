# Add, Negate, and Multiply

## Changing Images with Simple Math: A Simple Explanation

Imagine an image as a grid of numbers, where each number shows how bright a spot (pixel) is. If we add 10 to every number in the grid, it's like turning up the brightness everywhere by the same amount—so a pixel that was 4 becomes 14, 3 becomes 13, and so on. This makes the whole image look brighter. Now, if we multiply every number by 3, it's like making the bright spots even brighter and the dark spots a bit brighter too, but in proportion to their original brightness. Lastly, if we take the negative of every number, it's like flipping the brightness upside down—bright spots become dark, and dark spots become bright.

Think of it like adjusting the volume on a music player: adding a number is like turning the volume up by a fixed amount, multiplying is like turning the volume up by a factor, and negating is like flipping the sound to its opposite. These simple math operations help us change images in useful ways.

## What Happens to Pixel Values When You Add a Constant to an Image?

When you add a constant to an image, you add that same number to the value of every pixel in the image.

- For example, if the constant is 10, a pixel with value 4 becomes 14, a pixel with value 3 becomes 13, and so on.
- Even pixels that were originally 0 will become 10.
- This operation increases the brightness of the entire image uniformly.

## What Is the Effect of Negating an Image Function on Pixel Values?

Negating an image function means multiplying every pixel value by -1.

- Each pixel's brightness value changes to its negative counterpart.
- For example, a pixel with value 3 becomes -3.
- Pixels with value 0 stay the same (0 negated is still 0).
- This effectively inverts the image's intensity, turning bright areas dark and dark areas bright.

## How Does Negating and Scaling an Image Function Affect Image Contrast and Intensity?

- **Negating:** Flips the intensity values, so bright areas become dark and dark areas become bright. This inverts the image but does not change the contrast level itself; it just reverses the brightness.
- **Scaling (multiplying by a positive number):** Multiplies each pixel's intensity by that number, increasing or decreasing the overall brightness proportionally. If the scale factor is greater than 1, the image becomes brighter and the contrast between light and dark areas increases. If it's between 0 and 1, the image becomes dimmer and contrast decreases.

Together, negating and scaling can invert the image and adjust how strong the differences between light and dark areas appear.
