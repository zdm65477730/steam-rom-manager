# itch.io 解析器 Specific Inputs

## itch.io AppData 路径 Override

By 默认 Steam ROM Manager assumes your itch.io app data is located at `%APPDATA%\itch` on windows `$HOME/.config/itch` on linux and `$HOME/Library/Application Support/itch` on macos.
This 字段 allows you to override that 路径 if your itch.io 用户 data is elsewhere.

## itch.io Windows-on-Linux Install Drive Redirect

On Linux, Windows app locations are recorded with Windows paths, even if running via Proton/Wine. If set, this 字段 replaces the root of game paths.
For 示例, this would change a `C:\\路径\To\Game.exe` to `<字段 值>/路径/To/Game.exe`.

This 字段 only has an effect on Linux systems.
