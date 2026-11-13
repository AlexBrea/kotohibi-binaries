# kotohibi-binaries

Prebuilt binaries that [Kotohibi](https://github.com/AlexBrea/kotohibi) downloads on first run. Release assets only.

| Component | Version | License | Source |
|---|---|---|---|
| FFmpeg (static, LGPL build, no GPL or nonfree parts) | 9.0.2 | LGPL-2.1-or-later | https://ffmpeg.org/releases/ffmpeg-9.0.2.tar.xz |
| whisper-cli (whisper.cpp) | 1.9.5 | MIT | https://github.com/ggml-org/whisper.cpp/tree/v1.9.5 (commit d1be6fde11ac6e0407606b4e42fe72d34add8037) |

Every archive contains its license text and a `BUILD-INFO.txt` with the exact build configuration. Verify downloads
against the `SHA256SUMS` file of each release. The build scripts are in `scripts/build-binaries` of the Kotohibi
repository.
