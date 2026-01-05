# App Icons

Place your app icons in this directory.

## Icon Requirements

- **Format**: PNG or JPG
- **Size**: 512x512 pixels (recommended for high quality)
- **Naming**: Use descriptive names like `app1-icon.png`, `app2-icon.png`, etc.

## Usage in index.html

Replace the placeholder emoji icons with actual images:

```html
<div class="app-icon">
    <img src="/icons/app1-icon.png" alt="App Name 1" style="width: 100%; height: 100%; object-fit: cover; border-radius: 22px;">
</div>
```

Or use the icon as background:

```html
<div class="app-icon" style="background-image: url('/icons/app1-icon.png'); background-size: cover; background-position: center;"></div>
```

