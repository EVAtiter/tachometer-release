[English](README.md) | [日本語](README.ja.md)

# Tachometer

A macOS menu-bar app that shows your network and disk traffic on four automotive tachometer-style analog gauges.

**➡️ [Download the latest release](https://github.com/EVAtiter/tachometer-release/releases/latest)**

## Features

- **Four independent gauges** — Network download / upload and disk read / write, each in its own small circular window (draggable anywhere, per-display position memory). Show or hide each gauge from the menu.
- **Peak-learning relative scale** — "100%" is the peak your Mac has actually observed. Choose a sliding window (5 min / 15 min / 30 min / 1 hour) or ∞ (remembered across restarts). A blue lamp blinks while a gauge is learning a new peak.
- **Calm needles** — Needle motion is smoothed (EMA + dead band) so gauges stay quiet at idle, with a full ignition-style needle sweep on launch and wake.
- **Two symbol sets** — "Cloud / Tray" or "Minimal Arrows", switchable from the menu.
- **Three display modes** — Normal / Always on Top / Widget (pinned to the desktop, click-through).
- **Day / Night lighting** — Follows the system appearance, or force Day (white) / Night (amber instrument lighting).
- **Japanese / English** — Follows the system language.

## Requirements

- macOS 14 Sonoma or later
- Apple Silicon (arm64) only

## Installation

### Homebrew

```
brew install --cask EVAtiter/tap/tachometer
```

### Manual

1. Download `Tachometer-<version>.zip` from [Releases](https://github.com/EVAtiter/tachometer-release/releases/latest)
2. Unzip and move `Tachometer.app` to `/Applications`
3. Launch it — the app lives in the menu bar (gauge icon); it does not appear in the Dock

The binary is signed with a Developer ID and notarized by Apple.

## Usage

- Operate everything from the gauge icon in the menu bar: live values, peak-hold duration slider, peak reset, display modes, lighting, symbols, and per-gauge visibility.
- Right-click any gauge window for the same menu.
- Drag a gauge to move it; positions are remembered per display.

## Background

Measurement is shared with [Gigant Monitor](https://github.com/EVAtiter/gigant-monitor-support), and the analog gauge rendering grew out of the sport-style dial of Fuel Level Plus — this app puts the two together: real traffic, on real-feeling instruments.

## License / Copyright

Copyright © 2026 EVA Titer. All rights reserved.

This repository distributes binary releases only.
