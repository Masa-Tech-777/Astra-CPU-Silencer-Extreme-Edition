Astra CPU Silencer Extreme v2.5.1
README / English
============================================================

■ Introduction

Astra CPU Silencer Extreme is the extended edition of Astra CPU Silencer.

It uses standard Windows CPU power-management controls to provide a wider
adjustment range for maximum frequency, minimum processor performance,
and boost behavior.

It does not use a custom kernel driver and does not directly modify CPU voltage.


■ Supported Environment

・Windows 11 64-bit
・Intel CPUs
・AMD Ryzen CPUs
・Administrator privileges are required

※ Windows 10 may work, but it is not officially supported.
※ Actual behavior may vary depending on the CPU, BIOS, Windows power plan,
   thermal conditions, and manufacturer-specific power-management features.


■ Extreme Edition

Extreme allows maximum and minimum frequency input in 10 MHz steps.

Minimum input value:

10 MHz

Default values:

・Maximum: 0 MHz = Unlimited
・Minimum: 1400 MHz

0 MHz means Unlimited and does not overclock the CPU.

The minimum-frequency value is converted to the Windows
"Minimum processor state (%)" setting.
It does not force the CPU to run continuously at the entered MHz.


■ 15-Second Safety Check

Before applying an Extreme setting, the application captures the current
Windows CPU power settings.

The new setting is then applied temporarily.

You have 15 seconds to choose:

[Keep Settings]

If you do not confirm within 15 seconds, close the confirmation window,
or choose [Revert Settings], Astra CPU Silencer Extreme restores the
Windows values captured immediately before the temporary change.

If the required rollback snapshot cannot be captured, the Extreme setting
is not applied.

This safety check also applies to Extreme presets.


■ CPU Specification Database

Maximum-frequency limits are based only on an exact CPU-model match in the
CPU specification database.

For a verified CPU:

・The registered base frequency is displayed.
・The registered maximum frequency is displayed.
・The registered maximum frequency is used as the allowed input ceiling.

If the CPU cannot be verified in the database, Extreme does not guess its
maximum frequency.

In that case, use:

0 MHz = Unlimited

If a value above the verified maximum is entered, the input field is corrected
to the verified maximum, but Windows settings are not changed at that moment.
Review the corrected value and apply again.

A valid database copy may be cached locally for offline reuse.


■ 2500 MHz Safety Redirect

For this project, 2500 MHz is treated as a value that should be avoided based
on hardware testing.

If 2500 MHz is entered, Extreme automatically redirects it to:

2400 MHz


■ Boost Mode

Processor Performance Boost Mode uses the Windows values 0 through 6.

The default value is:

1 (Enabled)

The exact effect of each boost mode may vary depending on the CPU and
Windows implementation.


■ Presets

Extreme provides tray presets including:

・Normal Mode (Unlimited)
・Medium Silent
・Extreme Low Power

Preset application also uses the 15-second safety check.


■ Restore Original and Full Reset

Open:

Menu -> Restore Original / Full Reset

[Restore Original]
Restores the saved CPU power settings and Processor-menu visibility from
before Astra CPU Silencer Extreme changed them.

Use this when you want to return the PC to its previous state.

[Full Reset]
Restores Astra baseline CPU settings, reorganizes the Processor menu to the
Astra Clean Baseline, and resets application settings.

If an Extreme temporary setting is still pending during the 15-second
confirmation period, it is reverted before Restore Original or Full Reset
continues.

Restore Original and Full Reset are intentionally different operations.


■ 60-Minute Trial

Without a registered Extreme license, Astra CPU Silencer Extreme can be used
in a 60-minute trial mode.

Trial usage is accumulated.

Ending the test manually does not consume the remaining time.
The remaining trial time continues on the next launch.

When the trial expires, Extreme attempts to restore the saved pre-change CPU
power settings before displaying the Extreme license-registration screen.


■ License Activation

Open:

Menu -> Register Extreme License Key

The application displays a Machine ID used for license issuance.

Support / license requests:
masatech.dev.apps@gmail.com

BOOTH:
https://masatech.booth.pm/


■ Diagnostic Log

Astra CPU Silencer Extreme stores a diagnostic log for support and
troubleshooting.

Location:

%AppData%\Astra_CPU_Silencer_Extreme\Astra_Extreme_Diagnostic_Log.txt

The diagnostic log is stored inside AppData.
It is not normally created beside the distributed EXE.

The log may contain information about the CPU, Windows power plans,
detected settings, safety-check processing, and power-setting operations
required for troubleshooting.


■ Updates

Use:

Help -> Check for Updates

Astra CPU Silencer Extreme checks the latest GitHub Release.

GitHub:
https://github.com/Masa-Tech-777/Astra-CPU-Silencer-Extreme-Edition


■ Uninstalling

Astra CPU Silencer Extreme does not use a dedicated uninstaller.

Before deleting the application, use [Restore Original] or [Full Reset]
if needed.

Then exit Astra CPU Silencer Extreme and delete the executable.

If Startup registration is enabled, the restore/reset process removes the
related Startup entry.


■ Important Notes

Extreme provides a wider adjustment range than the Standard edition.

It does not directly modify CPU voltage or BIOS settings, but it does change
Windows CPU power-management settings.

When using very low values, confirm that the PC remains stable during the
15-second safety period.

Actual CPU frequency is affected by many factors, including:

・CPU architecture
・Windows power management
・Current workload
・Temperature
・BIOS settings
・Manufacturer-specific firmware and power controls

The entered MHz value does not guarantee that the CPU will operate at exactly
that frequency at all times.


============================================================
Astra CPU Silencer Extreme v2.5.0
Support: masatech.dev.apps@gmail.com
============================================================
