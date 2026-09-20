# ViswaOS Studio Asset Hub & Media Engine 🎛️✨

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Indexed Assets](https://img.shields.io/badge/Assets-27%2C071%2B-emerald.svg)](#)
[![Music Collections](https://img.shields.io/badge/Music%20Sources-86%20Genres-purple.svg)](#)
[![Engine](https://img.shields.io/badge/Architecture-WebGL%20%7C%20Zero--Lag%20DOM%20%7C%20Fast%20BPM-orange.svg)](#)

A high-performance, studio-grade creative asset management hub and interactive media engine built for editors, sound designers, composers, and filmmakers.

Engineered to index and browse over **27,000+ creative assets** across 7 primary pillars with instant search, pinpoint waveform audio scrubbing, live 3D LUT simulation, automated BPM analysis, and stem isolation.

---

## ⚡ Core Innovations & Capabilities

### 1. 🎵 Algorithmic Auto-BPM Detection & Tempo Filtering
- **Energy Envelope Autocorrelation:** Real-time algorithmic tempo estimation for WAV, MP3, FLAC, and M4A audio files, accurate between 50 and 220 BPM.
- **BPM Range Filter Chips:** Instant one-click filtering into studio tempo brackets:
  - `< 90 BPM` (Lofi, Chill, Acoustic)
  - `90 – 115 BPM` (Groove, Hip-Hop, Beats)
  - `116 – 130 BPM` (House, Pop, Dance)
  - `131 – 150 BPM` (Trap, Cinematic Score, Rock)
  - `150+ BPM` (Drum & Bass, High-Octane Action)
- **Ascending & Descending BPM Sorting:** Sort from slowest ambient drones to fastest breakbeats.

### 2. 🎚️ Stem Isolation & "⚡ Only Full Mix" Quick Filter
- **Deconstructed Melodic Stems:** Automatically tags and filters tracks into `Full Mix`, `Full Track`, `Bass`, `Drums`, `Instruments`, `Melody`, `Vocals`, `Pads & Drones`, `Melodic Hits`, `Melodic Risers`, and `Tonal Transitions`.
- **One-Click Master Track Filter:** Click `[⚡ Only Full Mix]` in the top toolbar to immediately strip out stem clutter and preview only finished, ready-to-edit songs.

### 3. 🎼 Exhaustive 2-Year Music Catalog Categorization (86 Sources)
- **Curated Soundtracks & Cinema Scores:** 14 master collections including Documentary & Cinematic, YouTube Trending, Jon Youshaei, Life of Riza, Kelly Wakasa, Now Trending, OpenArt AI, Calm & Placement, Cooking & Nature, and all 6 subgenres of Master 100 Movie Soundtracks (Epic Sci-Fi, Cyberpunk, Suspense, Emotional Grandeur, Kinetic Action, Mythos).
- **Epidemic Sound Music (55 Granular Genres):** Every category visited and attributed—from `Chill Lofi Beats`, `Cinematic Vlog`, and `Ambient Tech` to `El Sonido De Mis Videos`, `Fusion India`, and `Think Media`.
- **Multiply Music Stems:** Full key-tagged tonal transitions, reverse pianos, vocal cadences, and melodic hits.

### 4. 👟 Deep Micro-Foley Subcategory Classification
- Granular breakdown of 2,200+ Foley assets into micro-categories with dedicated filter chips:
  - `Footsteps & Movement` (pavement, gravel, boots, strides, grass)
  - `Cloth & Fabric` (rustles, jackets, denim, zippers, leather)
  - `Paper & Books` (page turns, crumples, tears, cardboard)
  - `Doors & Latches` (hinges, latches, creaks, cabinets, closures)
  - `Glass & Ceramics` (clinks, shatters, mugs, bottles, glassware)
  - `Keys & Metal` (coins, rings, chains, chimes, tools)
  - `Wood & Creaks` (floorboards, snaps, splinters, furniture)
  - `Typing & Clicks` (mechanical keyboards, switches, mouse clicks, shutters)
  - `Domestic & Tools` (kitchen utensils, clocks, drills, cutlery)

### 5. 🎨 3D LUT WebGL Color Grading Simulator
- **Trilinear 3D Interpolation:** Client-side parser for `.cube` LUT files running at 60 FPS in WebGL.
- **Interactive Split Comparison Slider:** Before/After split bar with keyboard quick-peek (`Space` / `B` key).
- **Preset Reference Frames & Drag-and-Drop:** Test color grades on built-in Portrait, Golden Hour, Cyberpunk, and Cinema shots, or drop in your own video stills (`.png`, `.jpg`).
- **Intensity Control & PNG Export:** Adjust grade opacity from 0% to 100% and export graded frames directly.

### 6. 🎬 Zero-Lag Video Poster Preview Engine
- Eliminates browser UI lockup caused by thousands of eager `<video>` elements.
- Uses lightweight SVG poster cards with a 110ms hover-to-mount preview lifecycle, dropping CPU usage from 90% to under 2%.

### 7. 🔊 Grid & List Mode Hover Autoplay & Pinpoint Playback
- **Grid Mode Autoplay:** Hover over any card to trigger smooth, debounced preview playback with animated 4-bar equalizer visualization.
- **List Mode Waveform Needle:** Interactive waveform needle displays exact timestamp on hover; click anywhere for instant pinpoint seeking.
- **Draggable Seekbar & Global Audio Bar:** Full scrubber, volume control, loop playback, and Now Playing metadata display.

### 8. 📚 Documentation & Pack Guide Hub
- Indexes 236 PDF user manuals, CSV tracklists, and Universal Category System (UCS) metadata sheets.
- Built-in reader for PDFs, HTML, and text files with one-click Explorer reveal.

---

## 🚀 Quickstart & Setup

### Mode A: Local Studio Mode (Full Desktop Streaming)
Run the high-performance Python streaming server on your local workstation:

```bash
# 1. Start the Asset Vault server
python D:\ViswaOS\SYSTEM\tools\sfx_server.py

# 2. Open in your browser
http://localhost:8765
```

### Mode B: Cloud Showcase Mode (Vercel Deployment)
The web client includes built-in static data fallback, enabling one-click deployment to Vercel:

1. Import the repository into your [Vercel Dashboard](https://vercel.com/new).
2. Framework Preset: **Other** (Zero configuration needed).
3. Click **Deploy**.

Alternatively, deploy via CLI:
```bash
npm install -g vercel
vercel --prod
```

---

## ⌨️ Studio Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| `/` | Focus search bar |
| `Space` | Play / Pause locked audio track |
| `[` | Previous page |
| `]` | Next page |
| `Esc` | Close modal / Lightbox / LUT Simulator |
| `B` (hold) | Hold to preview original un-graded image in LUT simulator |

---

## 🛠️ Tech Stack
- **Frontend:** Vanilla TypeScript / HTML5 / CSS Modern Design System (Inter & JetBrains Mono)
- **Graphics Engine:** WebGL / Canvas 2D Trilinear LUT Engine
- **Audio Analysis:** Python `wave`, `struct`, `numpy` (envelope peak autocorrelation) & `ffmpeg`
- **Server:** Threaded HTTP Streaming Bridge with HTTP Range 206 support
- **Storage:** SQLite (`vault_index.db`) + Optimized JSON Cache (`vault_data.json`)

---

## 📄 License
MIT License. Built with pride for **ViswaOS**.
