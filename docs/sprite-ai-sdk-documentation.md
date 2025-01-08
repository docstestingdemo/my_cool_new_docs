

  # Sprite-AI SDK Documentation

## Overview

Sprite-AI is a powerful SDK designed to generate and manipulate sprite assets for game development, particularly optimized for use with Phaser.js. This documentation covers the key functions available in the Sprite-AI SDK.

## Key Functions

### generateSprite(description, options)

Generates a sprite sheet based on a given description.

#### Parameters:
- `description` (string): A text description of the character or object to generate.
- `options` (object):
  - `iterations` (number, optional): Number of iterations to generate.
  - `size` (string, optional): Size of the output image (default: "1024x1024").
  - `save` (boolean, optional): Whether to save the generated image.

#### Returns:
An object or array of objects containing:
- `messages`: JSON response with frameHeight and frameWidth information.
- `image`: Base64 encoded image data URL.

#### Usage Example:
```javascript
const result = await sprite.generateSprite("medieval knight", { iterations: 1, size: "1024x1024" });
```

### generateHouseAsset(description, options)

Generates a 2D asset for use in Phaser.js games, specifically for house or building-like structures.

#### Parameters:
- `description` (string): A text description of the house or building to generate.
- `options` (object):
  - `iterations` (number, optional): Number of iterations to generate.
  - `size` (string, optional): Size of the output image (default: "1024x1024").

#### Returns:
A single response object or an array of response objects from DALL-E 3.

#### Usage Example:
```javascript
const result = await sprite.generateHouseAsset("medieval cottage", { iterations: 1 });
```

## Utility Functions

### removeBackgroundColor(inputPath, outputPath, targetColor, colorThreshold, options)

Removes a specified background color from an image.

### getUniqueColors(imagePath, options)

Retrieves an array of unique colors used in an image.

### encodeImage(imagePath)

Encodes an image file to a base64 string.

## Notes

- The SDK uses OpenAI's DALL-E 3 for image generation and GPT-4 for image analysis.
- Generated sprites are optimized for walking animations in a 2x3 grid format.
- Images are processed to grayscale and saved in PNG format when the `save` option is used.

  