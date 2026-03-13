# App Icons

Place your app icons in this directory.

## Icon Requirements

- **Format**: PNG or JPG
- **Size**: 512x512 pixels (recommended for high quality)
- **Naming**: Use the following names:
  - `qr-code-generator-icon.png`
  - `pdf-converter-icon.png`
  - `reverse-audio-icon.png`
  - `stoicism-ai-guide-icon.png`

## Current Apps

1. **QRSimple** (QR Code Generator) - Icon file: `qr-code-generator-icon.png` ✅
2. **PDF Converter** - Icon file: `pdf-converter-icon.png` ✅
3. **Reverse Audio and Singing** - Icon file: `reverse-audio-icon.png`
4. **Stoicism AI Guide** - Icon file: `stoicism-ai-guide-icon.png`

## Usage in index.html

Icons are already configured in `index.html`. To activate them:

1. Add your icon files to this directory with the names above
2. In `index.html`, uncomment the line with `background-image` and comment out the placeholder line

Example for QR Code Generator:
```html
<!-- Comment out this line: -->
<!-- <div class="app-icon placeholder">🔲</div> -->

<!-- Uncomment this line: -->
<div class="app-icon" style="background-image: url('/icons/qr-code-generator-icon.png'); background-size: cover; background-position: center;"></div>
```
