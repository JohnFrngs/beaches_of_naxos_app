# 🏖️ Beaches of Naxos — Desktop Application

> **Note:** This is a mini project developed as part of a university course assignment and uploaded here for completeness. My main portfolio with more advanced work is available at my personal website.

***

## Overview

**Beaches of Naxos** is a C# Windows Forms desktop application that serves as an interactive travel guide for the beaches of Naxos, Greece. The app showcases beach information, imagery, Google Maps integration, and practical travel tips — all within a multi-form desktop GUI.

Built with **.NET / C# WinForms** using **Visual Studio Enterprise**, published as a self-contained single-file executable.

Download the zip file / app [here](../../releases) and run .exe.

***

## Screenshots

| Main Menu | Beaches Explorer | Naxos Guide | Traveller's Guide |
|-----------|-----------------|-------------|------------------|
| Hero image with background music, navigation menu | Slideshow with image, description & Google Maps | Animated text presentation about Naxos | Rich formatted travel info |

***

## Features

- 🎵 **Background music** on launch with Play/Stop toggle
- 🖼️ **Auto-advancing image slideshow** (timer-driven) with Pause/Resume control
- 📍 **Embedded Google Maps** via WebView2 for each beach location
- 📝 **Animated text reveal** in the Naxos info section (timer-driven sequential display)
- 🗺️ **Traveller's Guide** with rich formatted text — transportation, accessibility, environment & emergency info
- 🖨️ **Print page** functionality across all forms (screen capture → PrintDocument)
- 💾 **Export to .txt** with UTF-8 BOM encoding (for proper Greek character support)
- ℹ️ **About dialog** and application exit from menu strip

***

## OOP Concepts Applied

| Concept | Where Applied |
|--------|---------------|
| **Classes & Objects** | `PictureInfo` class encapsulates beach data (title, description, image, map URL); `SoundPlayer`, `PrintDocument`, `SaveFileDialog` instantiated as objects |
| **Encapsulation** | All event handlers and internal fields declared `private`; access to form state controlled through methods |
| **Inheritance** | All forms (`Form1`–`Form4`) inherit from `System.Windows.Forms.Form` |
| **Abstraction** | WinForms abstracts UI rendering; `PrintDocument` abstracts the print pipeline |
| **Collections** | `List<PictureInfo>` used to manage beach data dynamically |
| **Event-Driven Programming** | Timer events, button click handlers, and menu strip events drive all interactivity |
| **Constructor Initialization** | `Form` constructors initialize component state, set `ReadOnly` properties, and configure UI defaults |

***

## Tech Stack

- **Language:** C# (.NET)
- **UI Framework:** Windows Forms (WinForms)
- **Browser Component:** Microsoft WebView2
- **IDE:** Visual Studio Enterprise
- **Deployment:** Single-file self-contained publish (Windows x64)

***

## Project Structure

```
GreekBeaches/
├── Form1.cs          # Main menu — music, navigation
├── Form2.cs          # Beaches slideshow — images, descriptions, Google Maps
├── Form3.cs          # Naxos info — animated sequential text display
├── Form4.cs          # Traveller's Guide — rich text, formatted sections
├── PictureInfo.cs    # Data model class for beach entries
├── Program.cs        # Entry point
└── Properties/
    └── Resources     # Embedded images, audio
```

***

## Beaches Covered

| Beach | Highlights |
|-------|-----------|
| Agia Anna | Picturesque fishing village, calm bay, easy access |
| Agios Prokopios | Golden sand, flamingo salt lake ("Pink Lake") nearby |
| Plaka | Longest beach on the island — 3+ km of fine sand |
| Glyfada | Wind & kitesurfing hotspot, crystal-clear waters |
| Aliko / Hawaii Beach | Cedar forest, sand dunes, natural coves |
| Mikri Vigla | Two-section beach — windsports south, calm swimming north |
| Kastraki | Quiet bay, minimal organization, two coves |

***

## How to Run

1. Download the `.zip` from [Releases](../../releases)
2. Extract to any folder
3. Run `GreekBeaches.exe`

> Requires Windows 10/11. No installation needed — fully self-contained.

***

## License

Copyright © 2025 Ioannis Frangistas. All rights reserved.  
See [LICENSE](LICENSE) for details.
