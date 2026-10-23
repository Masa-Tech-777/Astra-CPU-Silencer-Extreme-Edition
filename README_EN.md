Astra CPU Silencer Extreme Edition v2.5.1
README / English
============================================================

## 🌙 MasaTech Weekend Night Sale / 週末ナイトタイムセール

🎉 **October 23–25, 2026 | 2026年10月23日（金）～25日（日）**

**Every night 20:00–05:59 JST (UTC+9)**  
**毎晩20:00～翌朝5:59（日本時間）**

- ⚡ Astra CPU Silencer Standard Edition：**¥150**
- ⚡ Astra CPU Silencer Extreme Edition：**¥300**

Intel・AMD対応。CPU周波数の設定に加えて、ターボブーストの動作モードも調整できます。

Supports Intel and AMD processors, with configurable CPU frequency limits and Turbo Boost modes.

🛒 **BOOTH:** https://masatech.booth.pm/

*3夜限定の特別価格です。 / Special prices available during the three scheduled sale periods.*

==========================================================

■ Introduction

Astra CPU Silencer Extreme Edition is the extended edition of Astra CPU Silencer.

It uses standard Windows CPU power-management controls to provide a wider
adjustment range for maximum frequency, minimum processor performance,
and boost behavior.

It does not use a custom kernel driver and does not directly modify CPU voltage.



■ What Is Astra CPU Silencer Extreme Edition?

Astra CPU Silencer Extreme Edition is a Windows utility for configuring CPU frequency limits
and turbo boost behavior using numerical inputs and a selection of boost modes.
It supports Intel CPUs and AMD Ryzen CPUs, automatically identifies the CPU model,
and checks it against an embedded specification database. For an exact, verified match,
the registered maximum frequency is used as the input ceiling.

Extreme Edition accepts maximum and minimum frequency settings in 10 MHz steps.
You can set a maximum-frequency limit within the CPU's turbo-boost range and select
one of Windows' Processor Performance Boost Mode policies (values 0 through 6).

Silencer does not continuously adjust the CPU clock itself.
It applies configuration to Windows power management; Windows and the CPU then manage
actual frequency changes and boost operation. No custom kernel driver or direct CPU
voltage changes are used.

For example, on a test system with an Intel Core i7-10510U (maximum boost frequency
4900 MHz), a configured 3800 MHz ceiling resulted in an observed frequency of up to
3798 MHz. This is a measurement on one development system, not a guarantee for other PCs.

Extreme settings are applied temporarily and require confirmation within 15 seconds.
Without confirmation, the application restores the Windows settings saved immediately
before the change. See the sections below for model verification, input correction,
safety confirmation, and recovery details.

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
or choose [Revert Settings], Astra CPU Silencer Extreme Edition restores the
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

The CPU specification database is embedded in the application.
CPU lookup does not require Internet access or a downloaded cache.


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


■ Boost Mode Options and Behavior

Extreme Edition offers seven Windows boost policies, rather than just an on/off switch.
The descriptions below summarize the intended policy. Actual behavior depends on
the CPU, Windows processor power-management implementation, BIOS, and other conditions.
Not every system will exhibit a distinct or identical effect for every mode.

0: Disabled
   Disables requests for performance above the processor's guaranteed level.

1: Enabled
   Uses the standard Windows boost policy. This is Extreme's default setting.

2: Aggressive
   Requests higher performance more aggressively; it does not mean the CPU
   continuously runs at its highest clock frequency.

3: Efficient Enabled
   Allows boost while emphasizing energy efficiency.

4: Efficient Aggressive
   Uses a more performance-oriented policy while taking energy efficiency into account.

5: Aggressive At Guaranteed
   Requests additional performance aggressively relative to the guaranteed
   performance level.

6: Efficient Aggressive At Guaranteed
   Requests additional performance relative to the guaranteed level while
   taking energy efficiency into account.

A maximum-frequency setting is a limit, not a fixed-clock command.
Even with boost enabled, the observed frequency varies with workload, temperature,
power conditions, Windows, and CPU implementation.


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
before Astra CPU Silencer Extreme Edition changed them.

Use this when you want to return the PC to its previous state.

[Full Reset]
Restores Astra baseline CPU settings, reorganizes the Processor menu to the
Astra Clean Baseline, and resets application settings.

If an Extreme temporary setting is still pending during the 15-second
confirmation period, it is reverted before Restore Original or Full Reset
continues.

Restore Original and Full Reset are intentionally different operations.


■ 60-Minute Trial

Without a registered Extreme license, Astra CPU Silencer Extreme Edition can be used
in a 60-minute trial mode.

Trial usage is accumulated.

Time already used is counted; unused trial time is retained when you exit.
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

Use Help -> Save diagnostic log… to copy the log to a location you select.
You do not need to attach license keys or configuration files manually.
Review the log before sending it for support.

Astra CPU Silencer Extreme Edition stores a diagnostic log for support and
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

Astra CPU Silencer Extreme Edition checks the latest GitHub Release.

GitHub:
https://github.com/Masa-Tech-777/Astra-CPU-Silencer-Extreme-Edition


■ Uninstalling

Astra CPU Silencer Extreme Edition does not use a dedicated uninstaller.

Before deleting the application, use [Restore Original] or [Full Reset]
if needed.

Then exit Astra CPU Silencer Extreme Edition and delete the executable.

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
Astra CPU Silencer Extreme Edition v2.5.1
Support: masatech.dev.apps@gmail.com
============================================================

■ Disclaimer and Compatibility

Although the software uses standard Windows APIs, changes to CPU power settings may reduce responsiveness or temporarily freeze the system, depending on the PC and selected values.
Masa Tech!! / イタチ disclaims responsibility for direct or indirect losses arising from use or inability to use the software, including hardware damage, data loss, business interruption and lost opportunities, to the extent permitted by applicable law.
Please test compatibility using the free trial before purchasing and use the software at your own responsibility.
Some manufacturer-specific motherboard or BIOS configurations may prevent control from working.
Applicable third-party license rights and their warranty terms are not restricted by this product notice; see THIRD-PARTY-RIGHTS.txt.

■ Distribution Files and Third-party Software

Extract the entire ZIP before launching the EXE.
README_JP.txt / README_EN.txt contain the Japanese and English instructions.
THIRD_PARTY_NOTICES.txt lists components and acknowledgements; THIRD-PARTY-RIGHTS.txt explains third-party rights.
licenses/ contains full license texts, component notices and the ScriptGuard author's permission record.
source/ contains the official AutoHotkey 2.0.29 and Ahk2Exe/BinMod source archives, runtime modification notes and build/apply instructions.
See source/BUILD-INFO.txt for this executable's build evidence and source/PROTECTED-RUNTIME-STATUS.txt for the supplied materials and verification limits.
Example.ahk is a harmless example of the third-party protection workflow. It is not required to run the product.
MasaTech's proprietary application source and license-issuing tools are not included.

Product terms do not restrict copying, modification or redistribution rights granted by applicable third-party licenses.
Third-party rights and warranty disclaimers are governed by their original license texts.

Help -> About -> Third-party software and licenses displays the basic embedded notices.
Those embedded documents can be viewed with the EXE alone. Consult the accompanying files for the newly supplied material and detailed build evidence.
Editing accompanying files does not automatically change the embedded display in this version.
When distributing this package, retain the complete set including licenses/ and source/ rather than distributing the EXE alone.

We sincerely thank the authors and developers of AutoHotkey and TAC109, the author of ScriptGuard.
