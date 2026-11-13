<div align="center">

<p align="center"><img src="assets/kotohibi-icon.svg" alt="Kotohibi icon" width="96" /></p>

# Kotohibi binaries

### ことひび

**Listen. Read. Understand.**

Prebuilt, hash-pinned binaries that [Kotohibi](https://github.com/AlexBrea/kotohibi) downloads
during its first-run setup, so nobody needs Homebrew, Python or a terminal.

![Platform: macOS](https://img.shields.io/badge/platform-macOS%20arm64%20%7C%20x86__64-blue)
![FFmpeg: LGPL](https://img.shields.io/badge/FFmpeg-LGPL--2.1%2B-green)
![whisper.cpp: MIT](https://img.shields.io/badge/whisper.cpp-MIT-green)

</div>

---

## What is here

This repository holds **release assets only**. Kotohibi's setup wizard fetches them from
[Releases](https://github.com/AlexBrea/kotohibi-binaries/releases); each file is verified against an exact
size and SHA-256 before it is installed.

| Component | Version | License | Upstream source |
|---|---|---|---|
| FFmpeg (static, LGPL build: no GPL or nonfree parts) | 9.0.2 | LGPL-2.1-or-later | [ffmpeg-9.0.2.tar.xz](https://ffmpeg.org/releases/ffmpeg-9.0.2.tar.xz) |
| whisper-cli (whisper.cpp, Metal + Accelerate) | 1.9.5 | MIT | [v1.9.5](https://github.com/ggml-org/whisper.cpp/tree/v1.9.5) (commit `d1be6fde11ac6e0407606b4e42fe72d34add8037`) |

Archives are named `<component>-<version>-macos-<aarch64|x86_64>.tar.gz`.

## Verify a download

Every release ships a `SHA256SUMS` file:

```bash
shasum -a 256 -c SHA256SUMS
```

Each archive also contains its license text and a `BUILD-INFO.txt` with the exact build configuration and the
system libraries it links (only macOS system libraries).

## How they are built

The builds are reproducible from pinned sources with the scripts in
[`scripts/build-binaries`](https://github.com/AlexBrea/kotohibi/tree/main/scripts/build-binaries) of the
Kotohibi repository (the repository becomes public with Kotohibi 1.0.0; until then the pinned upstream
sources above are the corresponding source). The FFmpeg build fails its own audit if it contains any GPL or
nonfree component.

## License

The binaries keep the licenses of their upstream projects (see the table and the license file inside each
archive). Kotohibi itself is licensed under MIT OR Apache-2.0.
