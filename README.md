# PoP: The Sands of Time - GOG Preservation Patch

This patch package brings GOG's official Preservation Program QoL update (**v1.00.181 GOG v2**) to other versions of the game (Steam, Ubisoft Connect, Retail CD/DVD, etc.).

## Features & Fixes

- All credit for the logic of the patch goes to GOG team. This patch is merely an adaptation for other versions.
- You can find the details of the implementation in their blog - https://www.gog.com/en/game/prince_of_persia_the_sands_of_time

## 📁 Package Contents

Ensure the following files are placed in your patch folder:

```text
├── gog_patch.bat         # 1-click patcher script (converts POP.EXE to gpp.exe)
├── dx.dll                # Direct3D 9 wrapper
├── di.dll                # DirectInput 8 wrapper
├── gog_core.dll          # Preservation engine runtime
├── gog_pop1.dll          # Game-specific FOV and camera plugin
├── SDL3.dll              # SDL3 runtime
├── tomlplusplus-3.dll     # TOML configuration parser
├── gog.toml              # Master configuration file
├── dinput8_wrap.dll      # (Optional) Controller mapper fallback
└── dixi.ini              # (Optional) Gamepad GUID layout definitions
```

## How to Apply the Patch

1. Copy all the patch files above (including `gog_patch.bat`) into your game installation directory (where `POP.EXE` is located):
   * **Steam**: `...\Steam\steamapps\common\Prince of Persia The Sands of Time\`
   * **Retail / Other**: `C:\Games\Prince of Persia The Sands of Time\`
2. Double-click **`gog_patch.bat`**.
3. It will read your `POP.EXE`, apply the binary patches, and create the patched executable **`gpp.exe`**.

#### Launching the Game:
* Run the game normally from steam first (so that it installs any dependencies needs, and verify it works).
* Run `gpp.exe` directly.

## Verification

The patch modifies 13 specific instruction points in `POP.EXE` (v1.00.181):
* **Original `POP.EXE` | SHA256**: `6587D499F4EA6D0895179F74487045BC2C82A9D4E08A0A5046C1FB88EE3B6EC9`
* **Patched `gpp.exe` | SHA256**: `09A958390015A4611B26926C82EE1505FA1926D0323F2EFCA18310BC08B5C80D`
