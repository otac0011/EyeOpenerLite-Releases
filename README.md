# EyeOpener Lite

**Guided signal- and power-integrity checks for PCB layouts.**

> **Releases-only repository.** This repo hosts the prebuilt Windows installer for EyeOpener Lite. The source code is proprietary and lives in a private repository.

## Install

**Recommended: [Retinue Launcher](https://github.com/otac0011/RetinueLauncher-Releases).** Install the launcher once; its **Available tools** tab installs and updates this tool and the other PCB tools (CastGuidance, FishLadder, EyeOpener Lite) from their official release pages. Nothing is installed until you choose it, and each tool's own installer shows its license.

**Or download the installer directly:**

→ **[Download the latest release](https://github.com/otac0011/EyeOpenerLite-Releases/releases/latest)** (Windows installer, about 100 MB)

Run `EyeOpenerLite-Setup-<version>.exe`. The installer shows the End User License Agreement, which you must accept to install. It installs to `Program Files\EyeOpener Lite` (it asks for administrator rights), adds a Start Menu entry, the validation report and an uninstaller (Settings → Apps). The app is self-contained: no separate .NET install is needed.

### Windows SmartScreen

The installer is not code-signed yet, so Windows may show **"Windows protected your PC"** the first time you run it. Click **More info → Run anyway**. You can check the download against the SHA-256 digest shown for the asset on the release page.

### System requirements

- Windows 10 or 11, 64-bit (x64)
- About 400 MB of disk space; field solves on large boards use several GB of RAM
- A GPU with Direct3D 11 for the 3-D board view; a CUDA or OpenCL card is optional (it speeds up EM solves)

## What it does

One window, four steps:

1. **Board**: open an ODB++ job (or a CAD stackup) and look at it in 2-D, 3-D and as a see-through skeleton; confirm the stackup.
2. **Nets**: nets grouped into links (differential pairs, buses, clocks), each with a link type: generic digital, high-speed serial or DDR.
3. **Check**: a checklist in the order a pro works: stackup, impedance, return path, coupling, TDR, signal quality, timing, loss, eye. Each check gives a verdict, the offending copper lit on the board, a plot and what to change.
4. **Report**: findings worst first.

Walkthroughs on real example boards ship with it, and `VALIDATION.html` (installed beside the app) shows how each check compares with reference results. A command-line tool, `eyelite.exe`, is installed beside the app.

## License

Distributed under a **proprietary End User License Agreement**; see [`LICENSE`](LICENSE). Open-source components and example boards it ships are listed with their licenses in [`THIRD-PARTY-NOTICES.txt`](THIRD-PARTY-NOTICES.txt).

**Summary** (the file is authoritative):

- ✅ Install and use on any device you own: personal, educational, or commercial
- ✅ Share **unmodified** copies (no fee)
- ❌ Sell, sublicense, or rent
- ❌ Modify, reverse-engineer, or create derivative works
- ❌ Distribute in modified form
- ❌ Remove or obscure copyright notices

This is **not** open-source software. Source code is held privately.

## Reporting a bug

[Open an issue](https://github.com/otac0011/EyeOpenerLite-Releases/issues). Please include the version (shown in the title bar, or `eyelite --version`), what step you were on, and a screenshot if applicable.

## Disclaimer

PCB designs and electronic circuits can pose safety and reliability risks. All values, recommendations, and outputs produced by EyeOpener Lite are **starting points for engineering judgment only**, not a substitute for qualified engineering review.

---

© 2026 EyeOpener Lite Developer. All rights reserved.
