# Jewelry AR Ring Try-On

A browser-based augmented-reality ring try-on. Point your phone or laptop camera at your hand and a ring is placed on your ring finger in real time using automatic hand tracking.

## Features
- Real-time hand tracking (MediaPipe) the ring follows finger position, angle, and width
- Works on mobile (front/rear camera with flip) and desktop webcam
- Ring catalog carousel to switch styles
- Capture a photo of your try-on and save or share it
- Single self-contained `index.html` no build step

## Usage
Open `index.html` over **HTTPS** and tap **Enable camera**.

> Camera access requires a secure (HTTPS) origin. It will not work when opened as a local `file://`.
> An internet connection is needed on first load the hand-tracking engine and fonts load from a CDN.

## Deploy (DigitalOcean App Platform)
1. Push this repo to GitHub.
2. DigitalOcean → **Create → Apps** → connect this repo, branch `main`.
3. It auto-detects a **Static Site** (leave build command empty, output dir `/`).
4. **Create Resources** you get an HTTPS URL where the camera works.

## Embedding
```html
<iframe src="index.html" allow="camera; fullscreen"
        style="width:100%;height:100dvh;border:0"></iframe>
```
The `allow="camera"` attribute is required or the camera will not start inside an iframe.

## Roadmap
- Swap placeholder rings for real product cutout PNGs (transparent background)
- Match store branding (fonts, colors, wordmark)
