# App Icons Instructions

You need to create 2 PNG icon files for your PWA:

## Required Icons:
1. **icon-192.png** (192x192 pixels)
2. **icon-512.png** (512x512 pixels)

## Easy Way to Create Icons:

### Option 1: Use Online Tool (EASIEST)
1. Go to: https://www.pwabuilder.com/imageGenerator
2. Upload any image (logo, card symbol 🃏, or text "پینک")
3. Download the generated icons
4. Rename them to: icon-192.png and icon-512.png

### Option 2: Use Canva (FREE)
1. Go to canva.com
2. Create custom size: 512x512 pixels
3. Design your icon (suggestion: Card game theme with Persian text "پینک")
4. Download as PNG
5. Use online tool to resize to 192x192: https://www.iloveimg.com/resize-image

### Option 3: Simple Text Icon
1. Go to: https://favicon.io/favicon-generator/
2. Text: "پینک" or "🃏"
3. Background: #667eea (purple gradient color)
4. Font: Any Persian font
5. Download and resize to 192x192 and 512x512

## Icon Design Tips:
- Use the app's purple gradient colors (#667eea, #764ba2)
- Include card symbols 🃏 or Persian text "پینک"
- Keep it simple and recognizable at small sizes
- Use high contrast for visibility

## Icon Placement:
Save both icon files in the SAME folder as your HTML file:
```
/your-folder/
  ├── index.html (or penak-pwa.html)
  ├── manifest.json
  ├── service-worker.js
  ├── icon-192.png  ← Add this
  └── icon-512.png  ← Add this
```

## Quick Test Icon (Temporary):
If you want to test PWA without custom icons, you can use:
- Download any 512x512 PNG from the internet
- Save as both icon-192.png and icon-512.png
- Later replace with your custom design
