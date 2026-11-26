# CineUnlock for Sony a7S III

Experimental firmware utility for the **Sony a7S III (ILCE-7SM3) running firmware 5.01**. Includes an S-Log3 False Color LUT exporter.

## Downloads

| Download | What it contains |
| --- | --- |
| [CineUnlock 0.4.0 Preview 2 for macOS](https://github.com/AndrewCreator/CineUnlock/releases/download/v0.4.0-preview.2-glass-falsecolor.1/CineUnlock-Sony-a7S-III-0.4.0-preview.2-macOS-arm64.zip) | Complete desktop app for Apple Silicon. |
| [Classic LUT](https://github.com/AndrewCreator/CineUnlock/releases/download/v0.4.0-preview.2-glass-falsecolor.1/FalseColorSLog3.cube) · [Minimal LUT](https://github.com/AndrewCreator/CineUnlock/releases/download/v0.4.0-preview.2-glass-falsecolor.1/FalseColorMinimalSLog3.cube) | 33³ monitoring LUTs for S-Log3. |
| [Release notes and checksums](https://github.com/AndrewCreator/CineUnlock/releases/tag/v0.4.0-preview.2-glass-falsecolor.1) | Testing scope, known limitations and SHA-256 digests. |

## Compatibility

- **Mac** — Apple Silicon with **macOS 15 or later**. The application uses an ad hoc signature. macOS may block the first launch of a downloaded copy. A fresh installation on a separate Mac remains unverified.
- **Camera preparation** — the utility targets the ILCE-7SM3 on 5.01 and expects Sony’s original `BODYDATA.DAT` for that version. The wizard checks the connected body and requires a writable card in slot 1 for package transfer.
- **False Color** — the `.cube` files use Sony’s built-in Display LUT. For SD media, copy the file into `Private/Sony/PRO/LUT`, import it in **Manage User LUTs**, select it in **Select LUT** and enable **Display LUT** in Log Shooting. [Sony’s LUT guide](https://helpguide.sony.net/ilc/2410/v1/en/contents/211h_manage_lut.html)

## Testing on the maintainer’s camera

**Hardware tests covered one Sony a7S III. A second body has not been tested.** An earlier modified 5.01 build installed from SD, showed “Body update complete” and returned to the shooting screen.

| Feature | Observed result |
| --- | --- |
| Shutter Angle | 180° and 90° worked. Angle remained available after power-off. |
| Variable Shutter | Worked in the maintainer’s tests on the same body. |
| BIG6 | The swipe-down screen remained available after a full power cycle in a separate test. |
| De-Squeeze | Temporary 1.3× and 2× LCD preview worked. The tested recordings retained their original proportions. |
| False Color | Both LUT exports were verified offline. Camera import and display remain unverified. |

The published build passed offline checks for the wizard, simulated USB recovery and retry blocking after an interrupted write. Installing the published build and recovering from a failed write on camera hardware remain unverified. Firmware preparation is experimental. An interruption while writing can require service.

## Feedback

Use [GitHub Issues](https://github.com/AndrewCreator/CineUnlock/issues) for reports. Include the Mac model, macOS version, camera model, firmware version, the wizard step and the exact error. Redact serial numbers and omit camera backups and firmware dumps.

## Distribution and attribution

Distributed with permission, as confirmed by the project maintainer. Third-party materials retain their respective terms. See [third-party notices](https://github.com/AndrewCreator/CineUnlock/releases/download/v0.4.0-preview.2-glass-falsecolor.1/THIRD-PARTY-NOTICES.txt). Sony is a trademark of its owner. CineUnlock is an independent project.
