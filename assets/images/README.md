# Background Image Instructions

This directory contains the hero background image for the website.

## Current Setup
- The CSS currently references `hero-bg.svg` as a placeholder
- To use the actual background image provided, follow the steps below

## To Replace with Your Background Image
1. Download the image from: https://github.com/user-attachments/assets/c9f7a651-2f29-4116-ac18-14f3bce3989f
2. Save it as `hero-bg.jpg` in this directory (replace the placeholder)
3. Update the CSS in `_sass/main.scss` line 44 to change from:
   ```scss
   url('../images/hero-bg.svg')
   ```
   to:
   ```scss
   url('../images/hero-bg.jpg')
   ```

## Image Details
- Original filename: 2812725700_3fcb639ce5_o (appears to be a Flickr photo)
- Recommended format: JPG 
- Recommended size: 1920x1080 or larger for best quality
- The gradient overlay will be applied on top for text readability