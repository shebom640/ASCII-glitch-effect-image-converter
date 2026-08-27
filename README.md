# ASCII Art Animator 🎨✨

Transform any image into mesmerizing animated ASCII art. Watch your photos flicker to life as streams of glitchy characters with original colors, CRT scanlines, and smooth animations.

## Features

- 🖼️ **Any Image to ASCII** — JPG, PNG, GIF, WebP, anything
- 🎨 **Original Colors** — Preserves the actual RGB colors from your source
- ⚡ **Live Animation** — Characters change every frame for that flickering effect
- 📺 **CRT Aesthetic** — Includes scanlines and subtle glow for retro vibes
- 🖥️ **Large Canvas** — 1280×960px (96×40 character grid)
- 🔧 **Fully Customizable** — Easy tweaks to character sets, colors, resolution, glitch effects

## Quick Start

1. Open `index.html` in your browser
2. Click "Upload an image"
3. Watch it transform into animated ASCII art

## How It Works

1. **Load image** → Uploaded file is read into canvas
2. **Extract pixels** → RGB values from each grid position
3. **Calculate brightness** → Standard luminance formula
4. **Map to characters** → Dark pixels → `.:'` `, medium → `*+=-~`, bright → `#@%█`
5. **Animate** → Characters flip every 3–6 frames for a living effect
6. **Apply effects** → Glitch distortion, CRT scanlines, glow

## Customization

### Character Sets
Edit arrays in `script-image.js`:
```javascript
const darkChars = ['.', ':', "'", '`', ' '];
const mediumChars = ['*', '+', '=', '-', '~', 'o', 'x'];
const brightChars = ['#', '@', '%', '&', '$', '█', 'M', 'W'];
```

### Resolution
```javascript
const charWidth = 12;   // smaller = more detail
const charHeight = 20;
```

### Canvas Size
```javascript
canvas.width = 1280;
canvas.height = 960;
```

### Animation Speed
```javascript
if (charState[i].age > Math.random() * 3 + 3) {  // 3-6 frames
```

### Glitch Effect
```javascript
if (Math.random() < 0.02) {  // 2% chance per frame
    charState[i].glitch = 1;
}
```

## Best Images

- **High contrast** — Portraits, faces, silhouettes
- **Colorful** — Sunsets, artwork, gradients (colors are preserved!)
- **Text/logos** — Screenshots, posters, signs
- **Detailed** — Landscapes, architecture, anything with texture

## Browser Support

Chrome, Firefox, Safari, Edge, and any modern browser with Canvas API.

## Files

├── README.md # This file

├── index.html # Main page

├── style.css # Styling

└── script-image.js # Animation logic

## License

MIT — Use it however you want!

---

⚡ Built with vanilla JavaScript and Canvas API
