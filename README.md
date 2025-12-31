# Dual Screen Wallpaper Tool (Ayaneo Pocket DS and Ayn Thor)

This is a dual screen wallpaper editor designed for the dual screen android devices like the Pocket DS and Thor. Import any image, position/scale it across the two screens, and export a correctly laid-out wallpaper.


## Features

### Core editing
- Import an image and position/scale it across **two screens**
- Accurate preview that matches export (no hidden cropping from overlays)
- Export wallpaper laid out to the Pocket DS dual-screen format

### Fill modes (black bars)
- **Blur Extend** (instant): quick blur fill for empty regions
- **Smart Fill (OpenCV Inpaint)** (fast): classic inpainting for a cleaner fill than blur, runs fully offline
- **AI Fill (LaMa)** (best quality, offline after download): optional on-device model download, manual “Generate” workflow

### Manual generation workflow (Smart Fill / AI Fill)
- Move/zoom your image first
- Press **Generate** to fill only the current black bars
- If you move the image again, the generated result clears (so you can regenerate for the new framing)

## How to use
1. **Import** an image
2. **Pan/zoom** until it looks right on both screens
3. If you see black bars:
   - Pick a fill mode (Smart Fill / AI Fill)
   - Press **Generate**
4. Press **Export** to save the final wallpaper

## AI Fill (LaMa) model download
AI Fill uses an optional LaMa inpainting model downloaded on demand. Once downloaded, AI Fill runs **fully offline**.

## Build
- Open the project in **Android Studio**
- Build/Run: `assembleDebug` or Run from the IDE

## Permissions
- Uses Android’s photo picker / media access for importing images
- Writes exported wallpapers to your chosen location

## Tech notes
- Fill is applied **only to empty regions** (true black bars). The real image content is never blurred/painted over.
- Preview and export use the same fill cache so results match.

## Third-party components / licenses
- **OpenCV** (used for inpainting and feather blending). OpenCV licensing details are published by OpenCV. :contentReference[oaicite:0]{index=0}
- **ONNX Runtime** (used to run the LaMa model on-device). ONNX Runtime is MIT licensed. :contentReference[oaicite:1]{index=1}
- **LaMa inpainting** model/code (Apache-2.0). :contentReference[oaicite:2]{index=2}

> Note: If you redistribute the app, ensure you comply with the license terms for all bundled/downloaded components.

## Credits
Created by **YesItsKira**.
