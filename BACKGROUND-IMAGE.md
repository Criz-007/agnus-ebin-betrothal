# Background Image Setup

## Download the Background Image

Your beautiful floral background image is available at:
**https://github.com/user-attachments/assets/926cf672-e1b5-4488-bc77-ae59ec1069bc**

## How to Add It

1. **Right-click** on the image URL above and select "Save link as..." or "Download linked file"
2. **Save the file** as `background.jpg` in the same folder as `index.html`
3. **That's it!** The page is already configured to use it

## What if I skip this step?

No problem! The page has a beautiful gradient fallback background that matches the floral color scheme:
- Warm rose and beige tones
- Professional and elegant
- Loads instantly

## File Structure

Your folder should look like this:
```
agnus-ebin-betrothal/
├── index.html
├── background.jpg          ← Add this file
├── README.md
├── CUSTOMIZATION.md
├── HOW-TO-DEPLOY.md
└── BACKGROUND-IMAGE.md
```

## For Developers

The CSS is set up with a fallback chain:
```css
background: 
    linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)),
    url('background.jpg') center/cover no-repeat,
    linear-gradient(135deg, #c9a690 0%, #8b6f5c 50%, #d4a896 100%);
```

This means:
1. **First choice:** Your `background.jpg` image with 30% dark overlay
2. **Fallback:** A beautiful gradient if the image isn't found
