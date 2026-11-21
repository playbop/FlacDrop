# FlacDrop

**FlacDrop** is a fast, native macOS audio converter for Apple Silicon built with SwiftUI and powered by FFmpeg. Drag and drop individual `.flac` files, `.cue` sheets, or entire album folders to batch-convert them into **MP3**, **M4A**, **AAC**, or **WAV** - with automatic single-file album splitting, tag preservation, and embedded cover art.

> **Download:** Grab the latest **`FlacDrop-v1.0-arm64.zip`** from the [**Releases**](../../releases/latest) page.

---

## Screenshots

<p align="center">
  <img width="256" height="256" alt="flacdrop" src="https://github.com/user-attachments/assets/405fc487-e837-44aa-b4cb-cf69c03bae6d" />
</p>
<p align="center">
  <img width="1031" height="633" alt="screenshot1" src="https://github.com/user-attachments/assets/bdaa5276-7d9f-4496-8ebc-09fbd7c37f53" />
</p>
<p align="center">
  <img width="1031" height="633" alt="screenshot2" src="https://github.com/user-attachments/assets/e04dc577-676c-49b7-8323-51f1d20dcfa0" />
</p>

---

## Features

- **Drag-and-Drop Queue:** Drop `.flac` files, `.cue` sheets, or album folders directly into the window. Track order is preserved automatically, and duplicate filenames in a batch are disambiguated.
- **CUE Sheet & Single-File Album Splitting:** Supports external `.cue` files (UTF-8, UTF-16, Windows-1252, ISO Latin-1) as well as embedded `CUESHEET` / native FLAC cue blocks inside single-file album `.flac`s, writing per-track metadata (`Title`, `Artist`, `Album`, `Track`).
- **Presets & Manual Controls:** Quick presets (`MP3 320 / 256 / 192 kbps`, `WAV Lossless`) or manual selection of format (`MP3`, `WAV`, `AAC`, `M4A`), bitrate (`96–320 kbps`), and channels (`Stereo` / `Mono`).
- **Cover Art & Track Inspector:** Click **`ⓘ`** on any track to view tags, bit depth / sample rate, and cover art. Embeds cover art into MP3 and M4A from folder artwork (`cover`, `folder`, `front`, `albumart`) or embedded FLAC art.
- **Apple Silicon Concurrent Conversion:** Runs parallel workers tuned to Performance cores with Stop / Resume support and safe output staging.

## Quick How-To Guide

1. **First Launch (macOS Gatekeeper):** Unzip `FlacDrop-v1.0-arm64.zip`, move `FlacDrop.app` to **Applications**, then **Control-click (right-click) `FlacDrop.app` > Open** *(required once because this free release is not notarized with a paid Apple Developer ID)*.
2. **Set Output Directory:** Click **Output Directory** at the bottom-left of the sidebar to choose where converted files go (defaults to **Downloads**).
3. **Pick Format & Quality:** Open **Settings** to choose a **Preset** or **Manual** format/bitrate/channels.
4. **Drop Audio Files:** Drag `.flac` files, `.cue` sheets, or album folders into the **Conversion Queue**. *(If dropping a standalone `.cue` file, click **Grant Access** when macOS asks for folder permission to read its `.flac`.)*
5. **Convert:** Click **Convert**. You can click **Stop Conversion** anytime and **Resume Conversion** later for any remaining tracks.

---

## Requirements & Licensing

- **Requirements:** macOS 14.0 (Sonoma) or later on Apple Silicon (`arm64`).
- **Third-Party Components:** FlacDrop bundles a static LGPL v2.1 build of FFmpeg (`libmp3lame` + native codecs). The license and exact corresponding source archives are available in [`third-party-sources/`](third-party-sources/).
