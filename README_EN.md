# Astra CPU Silencer Extreme Edition

**Fine-grained CPU power management with 10 MHz adjustment steps and a 15-second confirmation and rollback safeguard.**

Astra CPU Silencer Extreme Edition is an advanced Windows CPU power-management utility designed for users who want greater control over CPU power settings.

Built around Windows' native power-management capabilities, Extreme Edition allows you to adjust CPU-related settings without directly modifying CPU voltage or BIOS configurations.

It extends the safety-oriented design philosophy of Astra CPU Silencer Standard by offering a wider adjustment range and finer control.

## 💡 Why Choose Extreme Edition?

Extreme Edition is designed for users who want more flexibility when balancing CPU performance, temperature, fan noise, and power consumption.

Typical uses include:

- Reducing fan noise in quiet environments
- Managing CPU heat during everyday tasks
- Improving power efficiency on laptops
- Experimenting with lower CPU performance limits
- Fine-tuning power settings for different usage scenarios

Actual results depend on the CPU, system firmware, Windows configuration, workload, cooling system, and other hardware-specific factors.

## ⚙️ Main Features

- CPU frequency-limit adjustment in 10 MHz input steps
- Minimum frequency input as low as 10 MHz
- 0 MHz maximum setting for unlimited frequency
- 15-second confirmation and rollback safeguard
- Separate settings for AC and DC power
- CPU boost behavior adjustment
- Direct Windows power-plan switching
- Three convenient performance presets
- Exact-match CPU specification database
- Restoration and reset functions
- Japanese and English user interface
- Windows startup support
- Designed for Intel and AMD Ryzen processors

**Important:** An entered frequency value is not a command to lock the CPU at that exact clock speed.

Extreme Edition uses Windows power-management controls. Actual operating frequencies remain subject to Windows, CPU architecture, firmware, temperature, workload, and other system controls.

A 10 MHz input step does not guarantee that the processor can physically operate or be controlled in exact 10 MHz increments.

## 🛡️ 15-Second Confirmation and Rollback Safeguard

Extreme Edition includes a confirmation mechanism intended to reduce the risk of accidentally retaining unsuitable settings.

When an Extreme setting is applied:

1. The application first captures the existing Windows CPU power settings.
2. If the required rollback snapshot is successfully captured, the requested setting is applied.
3. A confirmation window gives the user 15 seconds to accept the change.
4. If the user confirms within the time limit, the new setting is retained.
5. If the user does not confirm, closes the confirmation window, or chooses to revert, the application attempts to restore the previously captured settings automatically.

**If the required rollback snapshot cannot be captured, the Extreme setting will not be applied.**

This mechanism is a safety precaution, not a guarantee against every possible system failure.

Unexpected application termination, system instability, power interruption, or hardware-specific behavior may prevent successful restoration.

## 🔍 Exact-Match CPU Specification Database

Extreme Edition uses a CPU specification database to identify verified processor models.

Manufacturer-published base and maximum frequencies are displayed only when the detected CPU manufacturer and model match a verified database entry.

The application does not estimate the maximum supported frequency of an unverified CPU.

For unverified processors, use:

**0 MHz = Unlimited**

### Automatic Input Correction

Based on project hardware testing, an entered value of 2500 MHz is automatically adjusted to 2400 MHz.

This is an application-specific input adjustment and does not mean that 2500 MHz is inherently unsafe for all processors.

## ⚡ Three Performance Presets

Extreme Edition includes three presets for convenient power-management adjustments.

| Preset | AC Power | DC Power |
|---|---|---|
| 🟢 Extreme Low Power | 800 MHz | 600 MHz |
| 🟡 Medium Silent | 3.0 GHz | 2.6 GHz |
| 🔴 Normal Mode | Unlimited | Unlimited |

All Extreme presets use the 15-second confirmation safeguard.

The preset values are requested settings handled through Windows power management. They do not guarantee fixed operating frequencies.

## 🔄 Windows Power-Plan Management

Extreme Edition allows users to select and activate power plans registered in Windows directly from the application's interface.

CPU-related settings can be managed separately for:

- **AC:** External power connected
- **DC:** Battery operation

Available controls and their actual effects may differ depending on the system.

## 🔧 Restore and Reset Functions

### Restore Original

Attempts to restore the saved CPU power settings and Processor-menu visibility state from before Extreme Edition changed them.

### Full Reset

- Restores CPU power settings to the Astra-defined baseline
- Resets the Processor-menu configuration to the application's baseline
- Resets application settings

**Note:** Full Reset is not a factory reset of Windows, the BIOS, or the computer.

## 🎁 60-Minute Free Trial

Extreme Edition includes a 60-minute trial for users who have not registered a license.

Trial time is accumulated across sessions.

- Total trial duration: 60 minutes
- Manually ending the trial preserves the remaining time for the next launch
- When the trial expires, the application attempts to restore the saved pre-change CPU power settings
- The Extreme Edition license-registration screen is then displayed

The trial allows users to evaluate the software on their own hardware before purchasing.

## 🔑 Extreme Edition License

Commercial distribution through BOOTH is planned.

After purchasing Extreme Edition, open:

**Menu → Register Extreme License Key**

The application displays a Machine ID used for license registration.

Enter the issued Extreme Edition license key to activate the full version.

## 💻 System Requirements

| Item | Requirement |
|---|---|
| Officially supported OS | Windows 11, 64-bit |
| Supported processor families | Intel / AMD Ryzen |
| Permissions | Administrator privileges required |
| Windows 10 | May work, but is not officially supported |

Some features may be unavailable or behave differently depending on the processor, system firmware, manufacturer-specific power management, and Windows configuration.

## 📂 Package Contents

Main application and documentation files:

- Astra CPU Silencer Extreme.exe
- Readme_JP.txt
- Readme_EN.txt

The final distribution package may also include third-party license notices, source-code archives for applicable third-party components, and other compliance documentation.

The complete file list will be finalized before release.

## 📄 Diagnostic Log

Diagnostic information used for technical support and troubleshooting is stored at:

`%APPDATA%\Astra_CPU_Silencer_Extreme\Astra_Extreme_Diagnostic_Log.txt`

## ⚠️ Disclaimer and Important Notes

Astra CPU Silencer Extreme Edition uses Windows' native power-management mechanisms and does not directly modify CPU voltage or BIOS settings.

However, no software-based power-management approach can guarantee trouble-free operation on every system.

Depending on hardware, firmware, Windows configuration, and selected settings, users may experience reduced performance, unexpected system behavior, temporary freezes, or other problems.

To the extent permitted by applicable law, the developer disclaims liability for damages arising from the use of, or inability to use, the software, including hardware damage, data loss, business interruption, and loss of opportunity.

Users are strongly encouraged to evaluate the software using the free trial before purchasing.

Use the software with an understanding of the risks associated with changing system power-management settings.

## 💌 Support and Contact

For support, questions, or bug reports:

**masatech.dev.apps@gmail.com**

---

**Development and Production**

- Itachi (Kyokan / Masa Tech!!)
- Astra
- Mahiru

*Designed for flexible CPU power management using native Windows capabilities.*
