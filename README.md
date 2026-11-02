# AEUltimate

**A cross-platform launcher and trainer for DragonFable, AdventureQuest, and MechQuest.**

AEUltimate brings game enhancements, custom loaders, and a modern launcher together in one application. Version 4 is a major rebuild powered by a **customized native [Ruffle](https://ruffle.rs/) engine**, replacing the previous Chromium/PPAPI-based Flash setup.

**[Download AEUltimate](https://github.com/TheFlash3113/AEUltimate/releases/latest)** · **[View all releases](https://github.com/TheFlash3113/AEUltimate/releases)**

> **Version note:** The v4.1.0 update introduces desktop-only performance and diagnostic tools. The Android build remains at **v4.0.1**; check the version in the APK filename before downloading.

## Supported Platforms

| Platform | Architecture | Notes |
| --- | --- | --- |
| Windows | x64 | Native desktop launcher; DirectX 12, Vulkan, and OpenGL options where supported |
| Linux | x64 | Portable build; Vulkan and OpenGL availability depends on the system |
| macOS | Intel (x64), Apple Silicon (ARM64) | Native desktop builds |
| Android | ARM64, x86_64 | Native Ruffle player with a touch-friendly interface |

Available assets and graphics backends vary by release and device. iOS is **not currently supported**.

## Features

- **Native Flash playback:** DragonFable, AdventureQuest, and MechQuest run through a customized Ruffle desktop or Android player, without an embedded Chromium browser.
- **Smooth Motion:** Smoother movement and animations while retaining the games' Flash timeline rates.
- **Modern interface:** A familiar AEUltimate design rebuilt with Avalonia UI and .NET 10 on desktop.
- **Trainer functionality:** Existing game modifications, custom loaders, and supported Premium features carried forward from earlier versions.
- **Flexible rendering:** Select a supported graphics backend on desktop to suit your hardware and drivers.
- **Automatic desktop updates:** Download changed application files without reinstalling the entire package.
- **Native Android support:** Play using touch controls, with mobile-specific UI and input handling.

### New in v4.1.0 — Performance & Diagnostics (Desktop)

- **Performance overlay:** Press **F9** while a game is running to show or hide live statistics.
- **Performance Analyzer:** View graphs of Flash FPS, submitted FPS, CPU timings, and supported GPU timing scopes, with indicative bottleneck analysis.
- **30-second recordings:** Capture a performance problem and export the results as a ZIP containing measurements and diagnostics.
- **System diagnostics:** View OS, CPU, RAM, graphics devices, the **actual GPU and backend used by Ruffle**, process information, and recent native warnings/errors.
- **Game launch failure detection:** If Ruffle exits unexpectedly or fails to become ready, AEUltimate provides a clearer error message and details you can copy into a bug report.

GPU measurements depend on hardware and driver support. Bottleneck findings are diagnostic clues, not definitive conclusions. Submitted FPS may vary with Smooth Motion activity and is not necessarily the physical monitor refresh rate.

## Download & Installation

Get the appropriate archive or APK from the **[latest GitHub release](../../releases/latest)**.

### Windows

1. Download the Windows x64 ZIP.
2. Extract **the entire archive** to a folder of your choice.
3. Run `AEUltimate.exe`.

### Linux

1. Download the Linux x64 archive and extract it onto a Linux filesystem.
2. Open a terminal in the extracted application directory.
3. Run `./AEUltimate`.
4. Optional: run `bash Install-Linux-Shortcut.sh` if that script is included in your build and you want an application-menu shortcut.

The launcher and `Ruffle/ruffle_desktop` both need executable permissions. The official ZIP stores these permissions, but some extraction tools or filesystems may not preserve them. If necessary, run:

`chmod +x AEUltimate Ruffle/ruffle_desktop`

### macOS

1. Download the build matching your Mac: **Intel** or **Apple Silicon**.
2. Extract the archive and open `AEUltimate.app`.
3. If macOS blocks an unrecognized application, review the warning and, if you trust the downloaded release, allow it through **System Settings → Privacy & Security**.

### Android

1. Download the build matching your Android device: **ARM64** or **x86_64**.
2. Open the APK on your device and follow Android's installation prompts.
3. Launch AEUltimate and select your game.

Android APK updates are distributed separately from the desktop auto-updater. The v4.1.0 performance and diagnostics features are **not included in the v4.0.1 Android build**.

## Performance Monitoring & Reporting (Desktop)

**Live overlay:** Open a game and press **F9**.

**System diagnostics:** Open **Settings → View Diagnostics...** and use **Copy Diagnostics** to copy the report.

**Performance capture:**

1. Open **Settings → View Diagnostics... → Performance Analyzer...**.
2. Select the running game.
3. Click **Record 30s**, then reproduce the slowdown or stutter.
4. Click **Save Capture ZIP...** and attach the ZIP to your report.

**Launch failure:** If a game fails to open, click **Copy Details** in the error window and include the result in your report. You can also try another renderer in Settings; for example, **DirectX 12** or **OpenGL** may work on Windows hardware where Vulkan fails.

## Bug Reports & Support

Please post issues in **#bug-reports** on the AEUltimate Discord server. A useful report includes:

- Your **AEUltimate version** and **operating system**.
- The affected **game**, steps to reproduce, and what happened versus what you expected.
- A copied **Diagnostics** report or **launch failure details**, when applicable.
- A **30-second Performance Analyzer ZIP** for performance problems.

**Privacy:** Diagnostics can contain hardware information, running-process details, and recent native error output. Review a report before sharing it publicly; log redaction is best-effort.

## About the Project

AEUltimate started as a DragonFable trainer and has grown over nearly five years into a cross-platform application supporting three Artix Entertainment games. Version 4 is its largest architectural update, bringing native Ruffle playback and a new desktop/mobile foundation.

Built with [Ruffle](https://ruffle.rs/), [Avalonia UI](https://avaloniaui.net/), and [.NET](https://dotnet.microsoft.com/).

AEUltimate is an independent, unofficial project and is **not affiliated with or endorsed by Artix Entertainment**. Game names and assets belong to their respective owners.

**Developed by Flash3113.** Thanks to everyone who has supported, tested, and reported issues with AEUltimate. ❤️
