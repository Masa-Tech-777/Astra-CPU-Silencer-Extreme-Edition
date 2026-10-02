Astra CPU Silencer Extreme v2.0.0
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
Astra CPU Silencer Extreme v2.0.0
Support: masatech.dev.apps@gmail.com
============================================================


============================================================
Astra CPU Silencer Extreme v2.0.0
README日本語 / 配布用説明書
============================================================

■ はじめに

Astra CPU Silencer Extreme は、Windows 標準の CPU 電源管理機能を利用して、
CPU の最大周波数、最小性能状態、ブースト動作をより広い範囲で調整するための
Astra CPU Silencer Extreme Edition です。

独自のカーネルドライバや CPU 電圧の直接制御は使用しません。
設定変更には Windows 標準の電源管理機能（powercfg 等）を使用します。


■ 対応環境

・Windows 11 64bit
・Intel CPU / AMD Ryzen CPU
・管理者権限が必要です

※ Windows 10 でも動作する可能性がありますが、正式サポート対象は Windows 11 です。
※ PC・CPU・BIOS・メーカー独自電源管理機能などの違いにより、動作結果は異なる場合があります。


■ Extreme 版について

Extreme 版では、最大 / 最小周波数を 10 MHz 刻みで入力できます。

最小入力値：
10 MHz

初期設定：
最大 0 MHz（制限なし）
最小 1400 MHz

0 MHz は「最大周波数の制限なし」です。
CPU をオーバークロックする設定ではありません。

最小周波数の MHz 入力は、Windows の「最小のプロセッサの状態（%）」へ換算して適用されます。
そのため、入力した MHz が実際の CPU クロックとして常時固定されるわけではありません。


■ 15秒安全確認

Extreme 版では、設定を適用する直前に
現在の Windows CPU 電源設定を取得して保存します。

設定は最初に一時適用されます。

15 秒以内に
［この設定を維持］
を押した場合のみ、その設定を採用します。

確認しなかった場合、確認画面を閉じた場合、
または［直前の設定に戻す］を選択した場合は、
適用直前に取得した Windows の設定へ自動的に戻します。

安全確認に必要な直前設定を取得できなかった場合は、
Extreme 設定そのものを適用しません。


■ CPU 仕様データベース

最大周波数は、CPU 型番が CPU 仕様データベースと完全一致した場合のみ、
登録済みのメーカー仕様最大値を入力上限として使用します。

CPU がデータベースで確認できない場合、最大値を推測しません。
その場合は 0 MHz（制限なし）をご利用ください。

データベース確認済み上限を超える値を入力した場合は、
入力欄だけを確認済み最大値へ修正し、その時点では Windows へ書き込みません。
表示された値を確認して、もう一度設定を適用してください。

一度取得した有効なデータベースはローカルへキャッシュされます。


■ 2500 MHz について

本プロジェクトの実機検証で安全上避けるべき値と判断したため、
Extreme 版でも 2500 MHz が入力された場合は 2400 MHz へ自動的に変更します。


■ ブーストモード

Windows の Processor Performance Boost Mode に対応した 0～6 の値を使用します。
標準値は 1（Enabled）です。

Windows や CPU により、各モードの実際の挙動は異なる場合があります。


■ プリセット

タスクトレイから、用途に応じたプリセットを選択できます。

・通常モード（制限解除）
・中速サイレント
・極限超省エネ

Extreme のプリセット適用時も 15 秒安全確認が行われます。


■ 「変更前へ復元」と「完全初期化」

メニューまたはタスクトレイから
［変更前へ復元 / 完全初期化］を選択できます。

【変更前へ復元】
Astra CPU Silencer Extreme が変更する前に保存した CPU 電源設定と
Processor メニューの表示状態へ戻します。

【完全初期化】
CPU 設定を Astra の基準初期値へ戻し、
Processor メニューを Clean Baseline へ整理して、
アプリ設定も初期化します。

15 秒確認中の一時設定がある場合は、
復元 / 完全初期化処理の前に直前の設定へ戻します。

通常、元の環境へ戻したい場合は「変更前へ復元」を使用してください。


■ 60分無料体験

ライセンス未登録時は 60 分間の Extreme 無料体験が可能です。

体験時間は累積で管理されます。
手動でテストを終了した場合、残り時間は次回起動時へ引き継がれます。

体験時間が終了した場合は、
保存済みの変更前設定への復元を試みた後、
Extreme 製品版ライセンス登録画面を表示します。


■ ライセンス登録

メニューの
［Extremeライセンスキーの登録］
から登録できます。

画面に表示されるマシン ID を開発者へお知らせください。

サポート / ライセンス申請：
masatech.dev.apps@gmail.com

BOOTH：
https://masatech.booth.pm/


■ 診断ログ

サポートや不具合調査のため、診断ログを保存します。

保存先：
%AppData%\Astra_CPU_Silencer_Extreme\Astra_Extreme_Diagnostic_Log.txt

配布フォルダや EXE と同じ場所へ診断ログを作成する仕様ではありません。

ログには CPU、Windows 電源プラン、設定処理、安全確認など、
不具合調査に必要な情報が記録されます。


■ アップデート

アプリ内の
［ヘルプ］→［最新版の確認］
から GitHub Releases の最新版を確認できます。

GitHub：
https://github.com/Masa-Tech-777/Astra-CPU-Silencer-Extreme-Edition


■ アンインストールについて

専用アンインストーラーはありません。

削除する前に、必要に応じて
［変更前へ復元］または［完全初期化］を実行してください。

その後 Astra CPU Silencer Extreme を終了し、
実行ファイルを削除してください。

スタートアップ登録を使用している場合は、
復元 / 完全初期化処理によって解除されます。


■ ご注意

Extreme 版は Standard 版より広い設定範囲を扱います。

本ソフトは CPU の電圧や BIOS 設定を直接操作するものではありませんが、
Windows の CPU 電源設定を変更します。

特に低い値を使用する場合は、
15 秒安全確認中に PC の動作を確認してください。

CPU クロックの実際の動作は、
CPU、Windows、電源プラン、負荷、温度、BIOS、メーカー独自制御などの影響を受けます。
入力した MHz と実クロックが常に一致することを保証するものではありません。

==================================================
【免責事項・ご注意点】
・本ソフトウェアはWindows標準APIのみを使用する安全設計ですが、CPUの動作周波数を変更する特性上、お使いのPC環境や設定値によってはOSの動作低下や一時的なフリーズが発生する可能性がございます。
・本ソフトウェアの使用、または使用不能によって生じた直接的・間接的な損害（ハードウェアの故障、データの消失、事業の中断、機会損失等）について、開発者（Masa Tech!! / イタチ）は一切の責任を負いかねます。
・必ずお使いの環境にて「無料お試し版（Trial）」で動作確認を行った上で、ご自身の責任においてご利用・ご購入ください。
==================================================


============================================================
Astra CPU Silencer Extreme v2.0.0
Support: masatech.dev.apps@gmail.com
============================================================
