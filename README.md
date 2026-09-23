[English](README.md) | [日本語](README.ja.md)

# Tachometer Plus / Tachometer Lite

A macOS menu-bar app that shows your Mac's CPU, GPU, network, disk, memory, power, and temperatures on automotive-style instruments.

**➡️ [Download the latest release](https://github.com/EVAtiter/tachometer-release/releases/latest)**

This repository distributes **Tachometer Plus**, the Developer ID–signed build with every instrument. An edition without power, GPU, ANE, and temperatures is available on the Mac App Store as **Tachometer Lite** (the installed app is named Tachometer).

## Instruments

| Instrument | Tachometer Lite | Tachometer Plus |
| --- | --- | --- |
| CPU/GPU Gauge (tachometer) | CPU needle only | ✅ CPU and GPU needles + ANE lamp |
| Network download / upload | ✅ | ✅ |
| Disk read / write | ✅ | ✅ |
| Free memory (fuel gauge) | ✅ | ✅ |
| Power Meter (whole-Mac power draw) | — | ✅ |
| CPU / GPU Temperature | — | ✅ |
| System Monitor | CPU history only | ✅ CPU and power history + GPU / ANE bars |

Each instrument lives in its own window (draggable anywhere, per-display position memory) and can be shown or hidden individually from the menu. The CPU/GPU Gauge and the temperature gauges are hidden by default.

## Features

- **Peak-learning relative scale** (traffic gauges) — "100%" is the peak your Mac has actually observed. In "Peak Hold Settings…", choose a sliding window (5 min to 1 hour) or ∞ (remembered across restarts). A blue lamp blinks while a gauge is learning a new peak.
- **Memory pressure warning** — the memory gauge's lamp lights amber and blinks in sync with macOS's own memory pressure signal (normal / warning / critical).
- **Power peak memory** (Plus only) — the Power Meter remembers its all-time peak draw indefinitely. The lamp blinks green while a new peak is being set.
- **ANE lamp** (Plus only) — the CPU/GPU Gauge's pink lamp lights when the Apple Neural Engine is working and blinks as its utilization rises.
- **Temperature gauges** (Plus only) — CPU and GPU temperatures on a 40–100 °C scale. The lamp lights at 85 °C and blinks at 95 °C.
- **System Monitor** — about 50 seconds of CPU and power history drawn as stacked cubes, in three layouts (Overlay / Split / Center; Plus only). Click it to switch to a numeric readout.
- **Gather Gauges** — lines up the other instruments around the CPU/GPU Gauge's current position.
- **Quick Reveal** — rest the pointer at the bottom edge of the screen for about half a second to bring the instruments to the front (off by default).
- **Calm needles** — Needle motion is smoothed (EMA + dead band) so gauges stay quiet at idle, with a full ignition-style needle sweep on launch and wake.
- **Two symbol sets** — "Cloud / Tray" or "Minimal Arrows", switchable from the menu.
- **Window placement** — "Always on Top" and "Pin to Wallpaper" (pinned to the desktop, click-through). With both off, windows behave normally.
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

The binary is signed with a Developer ID and notarized by Apple. Tachometer Plus runs without App Sandbox, which it needs to read power, GPU and ANE activity, and temperatures.

## Usage

- Operate everything from the gauge icon in the menu bar: per-instrument visibility, Gather Gauges, Quick Reveal, peak-hold settings, window placement, lighting, symbols, and the System Monitor layout.
- Right-click any instrument window for the same menu.
- Drag an instrument to move it; positions are remembered per display.
- Click the System Monitor to switch between the graph and the numeric readout.

## Background

Measurement is shared with [Gigant Monitor](https://github.com/EVAtiter/gigant-monitor-support), and the analog gauge rendering grew out of the sport-style dial of Fuel Level Plus — the memory and power gauges are in fact that app's fuel and power gauges, redrawn in Tachometer's dial style. This app puts real system activity on real-feeling instruments.

## Support

- Questions, bug reports, and requests: [GitHub Discussions](https://github.com/EVAtiter/tachometer-release/discussions)
- Email: info@slack-kingdom.com

## Privacy

The app collects no personal information and does not communicate over the internet. See [Privacy Policy](PRIVACY.md).

## License / Copyright

Copyright © 2026 EVA Titer. All rights reserved.

This repository distributes binary releases only.
