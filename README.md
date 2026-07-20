[English](README.md) | [日本語](README.ja.md)

# Tachometer / Tachometer Plus

A macOS menu-bar app that shows your Mac's network, disk, memory, and power activity on automotive tachometer-style analog gauges.

**➡️ [Download the latest release](https://github.com/EVAtiter/tachometer-release/releases/latest)**

This repository distributes **Tachometer Plus**, the Developer ID–signed build with all six gauges. A five-gauge edition without the power meter, simply called **Tachometer**, is also available on the Mac App Store.

## Gauges

| Gauge | Tachometer | Tachometer Plus |
| --- | --- | --- |
| Network download / upload | ✅ | ✅ |
| Disk read / write | ✅ | ✅ |
| Memory | ✅ | ✅ |
| Power (SoC power draw) | — | ✅ |

Each gauge lives in its own small circular window (draggable anywhere, per-display position memory) and can be shown or hidden individually from the menu.

## Features

- **Peak-learning relative scale** (traffic gauges) — "100%" is the peak your Mac has actually observed. Choose a sliding window (5 min / 15 min / 30 min / 1 hour) or ∞ (remembered across restarts). A blue lamp blinks while a gauge is learning a new peak.
- **Memory pressure warning** — the memory gauge's lamp lights amber and blinks in sync with macOS's own memory pressure signal (normal / warning / critical).
- **Power peak memory** (Plus only) — the power meter remembers its all-time peak draw indefinitely (not a sliding window), with its own reset command. The lamp blinks green while a new peak is being set.
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

1. Download `Tachometer-Plus-<version>.zip` from [Releases](https://github.com/EVAtiter/tachometer-release/releases/latest)
2. Unzip and move `Tachometer Plus.app` to `/Applications`
3. Launch it — the app lives in the menu bar (gauge icon); it does not appear in the Dock

The binary is signed with a Developer ID and notarized by Apple. Tachometer Plus runs without App Sandbox, which the power meter needs to read SoC power data.

## Usage

- Operate everything from the gauge icon in the menu bar: live values, peak-hold duration slider, peak reset, display modes, lighting, symbols, and per-gauge visibility.
- Right-click any gauge window for the same menu.
- Drag a gauge to move it; positions are remembered per display.

## Background

Measurement is shared with [Gigant Monitor](https://github.com/EVAtiter/gigant-monitor-support), and the analog gauge rendering grew out of the sport-style dial of Fuel Level Plus — the memory and power gauges are in fact that app's fuel and power gauges, redrawn in Tachometer's dial style. This app puts real system activity on real-feeling instruments.

## License / Copyright

Copyright © 2026 EVA Titer. All rights reserved.

This repository distributes binary releases only.
