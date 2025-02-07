# EFI Folder for Lenovo IdeaPad 5 Pro-16ACH6 (82L500S0RE) 💻

## Technical Specifications & Compatibility 🔧

| Component               | Specification                                  | Status                  |
|-------------------------|------------------------------------------------|-------------------------|
| **📦 Model**            | IdeaPad 5 Pro-16ACH6 (82L500S0RE)              | ✅    |
| **⚡ Processor**        | AMD Ryzen™ 7 5800H (8C/16T, 3.2-4.4 GHz)       | ✅ |
| **🧠 Memory**           | 16GB DDR4 3200MHz (Single-Channel)             | ✅    |
| **💾 Storage**          | 1024GB WD_BLACK SN850 NVMe SSD                 | ✅  |
| **🎮 Graphics**         | AMD Radeon™ Integrated Graphics                | ✅ via NootedRed.kext <sup>2</sup> |
| **🖥️ Display**         | 16.0" IPS 2560×1600 (2.5K) @60Hz               | ✅ HiDPI Scaling        |
| **📡 Wireless**         | Intel® Wi-Fi 6E AX210 + BT 5.3                 | ✅ HeliPort Required <sup>3</sup> |
| **🔌 Ports**            |                                                |                         |
| ⎇ **USB-C**             | `PD 20W` • `DP 1.4` • `USB 3.2 Gen2`           | ✅ Full Functionality   |
| ⎇ **HDMI 1.4b**         | 4K@30Hz Output                                 | ⚠️ Resolution Limited  |
| ⎇ **USB-A**             | 2× SuperSpeed 10Gbps                           | ✅ Both Ports Working   |
| ⎇ **📁 SD Reader**      | UHS-I Compatible                               | ❌ No Detection         |
| ⎇ **🎧 3.5mm Combo**    | Headphone/Mic                                   | ✅ Auto-Switching       |
| **📸 Webcam**           | 720p IR Hybrid with ToF                        | ⚠️ Video Only <sup>4</sup> |
| **🔋 Battery**          | 75Wh Capacity                                  | ✅ Monitoring Active    |
| **⌨️ Input Devices**    | Keyboard & Trackpad                            | ✅ Gestures Supported   |

## Annotated System Notes 📌
1. **Storage**: Replaced stock 512GB Sk hynix SSD ([compatibility issue](https://dortania.github.io/Anti-Hackintosh-Buyers-Guide/Storage.html))
2. **Graphics**: NootedRed.kext required for full acceleration (pre-installed)
3. **Wireless**: Requires `itlwm.kext` + HeliPort.app for Wi-Fi management
4. **Webcam**: IR functions/Windows Hello unavailable in macOS
5. **HDMI**: Hardware limitation of HDMI 1.4 spec (4K@30Hz max)
6. **Battery**: Implemented via [ECEnabler](https://github.com/1Revenger1/ECEnabler) + VirtualSMC

## Status Legend 🚥
| Icon  | Description                          | Color Code     |
|-------|--------------------------------------|----------------|
| ✅    | Fully Functional                    | `#2ecc71`      |
| ⚠️    | Partially Working/Limited           | `#f1c40f`      |
| ❌    | Non-Functional                      | `#e74c3c`      |
| 🔄    | Requires Third-Party Tools          | `#3498db`      |

## Hardware Workflow Diagram
```ascii
[BIOS] → [OpenCore 0.9.7] → macOS
  ├─ CPU: ✅ SSDT-CPUR
  ├─ GPU: ✅ NootedRed
  ├─ Wi-Fi: ✅ itlwm + HeliPort
  └─ Storage: ✅ NVMeFix
