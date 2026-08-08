# Linear Combination

## Linear Combination of Images: A Simple Explanation

Imagine you have two pictures, and you want to blend them together to create a new image. But you want to do it carefully so the colors or brightness don't get too bright or too dark. This is where the idea of a "linear combination" comes in. It's like mixing paint colors in specific amounts so the final color looks just right.

Here's how it works: You take a part of the first image and a part of the second image, multiply each by a number (called a coefficient), and then add them together. The important rule is that these numbers should add up to 1, so the mix stays balanced. For example, if you take 70% of the first image and 30% of the second, you multiply each pixel's value by 0.7 and 0.3 respectively, then add them. This way, you get a smooth blend without making the image too bright or too dark.

Think of it like making a smoothie: if you use 70% banana and 30% strawberry, you get a tasty mix that's not too banana-heavy or too strawberry-heavy. Similarly, linear combination helps combine images in a balanced way.

## What Is the Formula for Linear Combination of Two Images?

The formula for the linear combination of two images f(x, y) and g(x, y) is:

```
h(x, y) = a · f(x, y) + b · g(x, y)
```

where:

- h(x, y) is the resulting combined image,
- a and b are coefficients (weights) such that a + b = 1,
- f(x, y) and g(x, y) are the pixel values at position (x, y) in the two images.

This ensures the combined image maintains balanced intensity values.

## What Is the Purpose of Coefficients a and b in Linear Combination?

The coefficients a and b in the linear combination serve to control how much each image contributes to the final combined image. Specifically:

- **a** determines the weight or influence of the first image (f(x, y)).
- **b** determines the weight or influence of the second image (g(x, y)).

Since a + b = 1, these coefficients ensure the overall brightness or intensity of the combined image stays balanced and doesn't become too bright or too dark.

In short, they let you decide the mix ratio between the two images. For example, if a = 0.7 and b = 0.3, the final image will be mostly like the first image but with some influence from the second.

## How Would Changing Coefficients a and b Impact Image Blending Results?

Changing the coefficients a and b affects the blend by adjusting how much each image contributes to the final result:

- If a is larger and b is smaller (e.g., a=0.8, b=0.2), the combined image will look more like the first image (f(x, y)) with a subtle influence from the second image.
- If b is larger and a is smaller (e.g., a=0.3, b=0.7), the combined image will resemble the second image (g(x, y)) more.
- If a and b are equal (e.g., both 0.5), the images contribute equally, resulting in a balanced blend.

So, by adjusting these coefficients, you control the dominance and influence of each image in the blend.

## How Can You Calculate a Pixel Value Using Given Coefficients a and b?

To calculate a pixel value in the blended image using coefficients a and b, follow these steps:

1. Identify the pixel values at the same position (x, y) in both images: f(x, y) and g(x, y).
2. Multiply the pixel value from the first image by coefficient a.
3. Multiply the pixel value from the second image by coefficient b.
4. Add the two results together.

The formula is:

```
h(x, y) = a · f(x, y) + b · g(x, y)
```

For example, if a = 0.7, b = 0.3, f(x, y) = 4, and g(x, y) = 8:

```
h(x, y) = 0.7 × 4 + 0.3 × 8 = 2.8 + 2.4 = 5.2
```

This value (5.2) is the pixel value in the blended image at position (x, y).

## How Can You Apply Linear Combination to Blend Three Images Practically?

To blend three images f(x, y), g(x, y), and k(x, y) using linear combination, you extend the formula by adding a third coefficient:

```
h(x, y) = a · f(x, y) + b · g(x, y) + c · k(x, y)
```

where:

- a, b, and c are coefficients (weights),
- The sum of the coefficients should be 1: a + b + c = 1.

Practically, you:

1. Choose coefficients a, b, and c to control the contribution of each image.
2. For each pixel position (x, y), multiply each image's pixel value by its coefficient.
3. Add the three results to get the blended pixel value.

For example, if a=0.5, b=0.3, c=0.2, and the pixel values at (x, y) are 10, 20, and 30 respectively:

```
h(x, y) = 0.5 × 10 + 0.3 × 20 + 0.2 × 30 = 5 + 6 + 6 = 17
```

This gives the blended pixel value at that position.
