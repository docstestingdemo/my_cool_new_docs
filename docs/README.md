

  # sprite-ai

## Overview

sprite-ai is an npm module that provides utility functions for generating sprite sheets and game assets using AI. It leverages OpenAI's DALL-E 3 and GPT models to create customized sprites and assets for game development.

## Installation

```
npm install sprite-ai
```

## Main Functions

### generateSprite(description, options)

Generates a sprite sheet based on a given description.

#### Parameters:
- `description` (string): A description of the character or object to generate.
- `options` (object):
  - `iterations` (number): Number of iterations to generate.
  - `size` (string): Size of the image (default: "1024x1024").
  - `save` (boolean): Whether to save the generated image locally.

#### Returns:
An object or array of objects containing:
- `messages`: JSON object with frameHeight and frameWidth information.
- `image`: Base64 encoded image data URL.

### generateHouseAsset(description, options)

Generates a 2D game asset based on a given description.

#### Parameters:
- `description` (string): A description of the house or asset to generate.
- `options` (object):
  - `iterations` (number): Number of iterations to generate.
  - `size` (string): Size of the image (default: "1024x1024").

#### Returns:
A single response object or an array of response objects from DALL-E 3.

## Utility Functions

### removeBackgroundColor(inputPath, outputPath, targetColor, colorThreshold, options)

Removes a specific background color from an image.

### getUniqueColors(imagePath, options)

Extracts unique colors from an image.

### encodeImage(imagePath)

Encodes an image file to base64.

## Usage Examples

```javascript
import { sprite } from 'sprite-ai';

// Generate a sprite
const spriteResult = await sprite.generateSprite('cartoon cat', { size: '512x512' });

// Generate a house asset
const houseAsset = await sprite.generateHouseAsset('medieval cottage', { iterations: 3 });
```

## Notes

- The module uses OpenAI's API, so you need to have proper authentication set up.
- Generated images are optimized for use with Phaser.js game framework.
- The sprite generation function creates a 6-frame walking animation in a 2x3 grid layout.

  