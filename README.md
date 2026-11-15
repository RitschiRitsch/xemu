# X1 BOX Community

X1 BOX Community is an unofficial fork of [izzy2lost’s X1 BOX](https://github.com/izzy2lost/xemu), an original Xbox and Sega Chihiro emulator for Android. This fork includes the xemu and hakuX cores.

## Download

[Download the signed Android ARM64 APK](https://github.com/RitschiRitsch/xemu/releases/latest) from GitHub Releases. Under **Assets**, select the `.apk` file. The accompanying `.sha256` file contains the APK checksum.

The Community APK uses its own signing key and the Android package ID `com.izzy2lost.x1box.community`. It can be installed alongside the official X1 BOX app and earlier Community debug builds. Each installation has its own settings and app data. Use the in-app Save Manager to export and import game saves if you want to move them between installations.

[Official X1 BOX on Google Play](https://play.google.com/store/apps/details?id=com.izzy2lost.x1box)

## Community Changes

- **Auto aspect ratio.** Available in global and per-game settings. Auto uses 4:3 by default and switches to 16:9 when the selected core detects widescreen output. You can select 16:9 manually for games that render widescreen without a detectable signal.
- **hakuX HD video mode detection.** Corrects AV pack reporting so games can select supported HD modes when enabled. [hakuX PR #33](https://github.com/rfandango/hakuX/pull/33)
- **Internal vibration on Android handhelds.** Uses the device vibrator for player 1 when a controller vibrator is unavailable. Tested on the AYN Odin 3.
- **Halo: Combat Evolved campaign crash fix.** Frees low physical memory for game allocations by reducing the hakuX kernel reservation. [hakuX PR #40](https://github.com/rfandango/hakuX/pull/40)

[View the v1.1.0 release notes and source tag](https://github.com/RitschiRitsch/xemu/releases/tag/community-v1.1.0)

## Two Emulation Cores

Choose the core in Settings. You can also set a different core for each game.

- **xemu** emulates the full console. It runs the most games. Based on [xemu](https://xemu.app).
- **hakuX** is a faster core that runs fewer games. Based on [hakuX](https://github.com/rfandango/hakuX).

## Features

### Playing

- Game library with list, cover-grid and carousel views, plus optional online box-art lookup
- Settings for each game
- Save states with thumbnails, in several slots
- Fast forward
- Internal resolution scale up to 6x
- Aspect ratio options for Auto, Stretch, 4:3 and 16:9
- Vulkan and OpenGL ES renderers
- Custom GPU drivers such as Turnip, on supported Adreno devices
- Cheats and mods (hakuX core)

### Controls

- On-screen controller with an editable layout. It hides when a physical controller connects.
- USB and Bluetooth controllers, with button remapping
- **Local multiplayer** with more than one controller

### Multiplayer and Online

- **System Link over LAN** lets you play System Link games with other X1 BOX devices on the same Wi-Fi. One device hosts and the others join, with host discovery built in. It also works with xemu on PC.
- **XLink Kai** lets you play System Link games with people over the internet through a PC running the XLink Kai Engine.
- **Insignia** lets you play on the Xbox Live replacement service. A setup guide in the app walks you through creating and recovering your account.

### Console Tools

- Setup wizard for your Xbox files
- Save manager to browse, export, import and delete game saves
- Xbox dashboard support, including importing a dashboard and booting it from the library
- HDD tools and an EEPROM editor for language, video modes, widescreen and MAC address
- ISO to XISO converter

### Sega Chihiro (Arcade)

- Chihiro mode with light-gun and driving controls
- Widescreen hacks for supported games

## Device Requirements

- Android 10 or newer
- A 64-bit ARM device (`arm64-v8a`)
- A GPU with Vulkan 1.1 or newer. The xemu core can also use OpenGL ES.
- 4 GB of RAM or more recommended

## Your Files

Use game images dumped from your own discs. The download contains the emulator app only.

The **xemu core** also needs these original Xbox files:

- MCPX Boot ROM
- Flash ROM (BIOS)
- Xbox hard disk image

The **hakuX core** has its own built-in system software and only requires your games.

## Credits

- [izzy2lost/xemu](https://github.com/izzy2lost/xemu) for X1 BOX and its Android integration.
- [xemu-project/xemu](https://github.com/xemu-project/xemu) and QEMU for the xemu core.
- [rfandango/hakuX](https://github.com/rfandango/hakuX) and its contributors for the hakuX core.
- Seán Roche for the Halo campaign memory fix.

## License

- The xemu-based emulator follows the xemu and QEMU licensing. It is mostly **GNU GPL v2**, with some GPLv2-compatible parts (for example BSD or MIT code in TCG). See [LICENSE](LICENSE), [COPYING](COPYING) and [COPYING.LIB](COPYING.LIB).
- The hakuX core in `android/hakux/core` is **GNU GPL v3 or later**. See the [hakuX license](android/hakux/core/LICENSE).

## Notes

- X1 BOX is not affiliated with Microsoft or Sega.
- Compatibility and performance vary by device and game.
