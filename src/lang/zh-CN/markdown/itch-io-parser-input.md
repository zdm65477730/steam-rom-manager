# itch.io 解析器特定输入

## itch.io AppData 路径覆盖

默认情况下，Steam ROM Manager 假定您的 itch.io 应用数据在 Windows 上位于 `%APPDATA%\itch`，在 Linux 上位于 `$HOME/.config/itch`，在 macOS 上位于 `$HOME/Library/Application Support/itch`。
如果您的 itch.io 用户数据在其他位置，此字段允许您覆盖该路径。

## itch.io Linux 上 Windows 游戏安装驱动器重定向

在 Linux 上，即使通过 Proton/Wine 运行，Windows 应用位置也会使用 Windows 路径记录。如果设置，此字段将替换游戏路径的根目录。
例如，这会将 `C:\\Path\To\Game.exe` 更改为 `<字段值>/Path/To/Game.exe`。

此字段仅在 Linux 系统上生效。
