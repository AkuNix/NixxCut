<p align="center">
  <img src="assets/icons/nixxcut_logo_256.png" alt="NixxCut" width="96" />
</p>

<h1 align="center">NixxCut</h1>
<h3 align="center">A native video editor for Windows and Android.</h3>

NixxCut is a fork of [Concat](https://github.com/jub0t/Concat), based on
Concat v0.2.8. It keeps Concat's native Rust engine and Slint interface,
with NixxCut branding, packaging and product direction.

This is **v0.1.0 development**. Windows builds are the current focus;
Android packaging follows. There are no public NixxCut releases yet.

## What it does

- Multi-track timeline editing, keyframes, effects and transitions.
- Local captions, text-to-speech and background removal models.
- GPU-composited preview and hardware-accelerated export.
- No account, no upload and no watermark.
- Windows and Android targets; projects stay on the local machine.

## Build from source

Prerequisites follow Concat's build setup: Rust 1.93.1, the platform's C++
toolchain, FFmpeg development libraries, LLVM/libclang, ONNX Runtime and
sherpa-onnx. On Windows, the repository's CI scripts and
`scripts/ci/fetch.sh` show the pinned versions.

```powershell
cd src
cargo build -p nixxcut
target\debug\nixxcut.exe
```

The package and executable are both named `nixxcut`. On Windows, put the sherpa-onnx DLLs on `PATH` before running.

Smoke test:

```powershell
target\debug\nixxcut.exe --version
target\debug\nixxcut.exe --smoke
```

## License and attribution

NixxCut is licensed under the **GNU Affero General Public License v3.0 or
later**. It is derived from Concat, copyright Jareer and Concat
contributors. See [LICENSE](LICENSE), [NOTICE.md](NOTICE.md) and
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
