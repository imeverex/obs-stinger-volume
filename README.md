# Stinger Volume for OBS

OBS's built-in Stinger transition has no volume control, so the only way to make a loud stinger quieter is to re-encode the video. This plugin adds a **Stinger (Volume)** transition. It works exactly like the built-in Stinger (same options, track matte support, monitoring, and fade styles) but with a **Stinger Volume** slider (0–100%).

The slider only changes the stinger's own audio. Your scene audio still fades the way it normally does.

## Install

Download the latest build for your OS from [Releases](../../releases).

- **Windows:** run the installer, or extract the zip into `C:\ProgramData\obs-studio\plugins\`
- **macOS:** run the `.pkg`
- **Linux:** install the `.deb`

Restart OBS, then go to **Scene Transitions → + → Stinger (Volume)**.

## Build

This uses the official [obs-plugintemplate](https://github.com/obsproject/obs-plugintemplate). GitHub Actions builds Windows, macOS and Linux on every push. Push a tag like `1.0.0` to create a draft release.

Local build: `cmake --preset windows-x64` then `cmake --build --preset windows-x64` (needs Visual Studio 2022 and CMake 3.28+).

## License

GPL-2.0-or-later. The transition code is a fork of OBS Studio's `transition-stinger.c`.

## Known limitation

In Studio Mode, OBS disables the T-bar for its built-in Stinger by checking the transition's id. It can't recognise this plugin's transition, so avoid dragging the T-bar while Stinger (Volume) is selected and use the Transition button instead.
