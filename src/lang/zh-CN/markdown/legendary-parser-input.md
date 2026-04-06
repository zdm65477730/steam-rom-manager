# Legendary 解析器特定输入

## Legendary 路径覆盖

默认情况下，Steam ROM Manager 在 Windows 上使用 `(Get-Command legendary).Path`，在 Linux 和 Mac 上使用 `which legendary` 来确定您的 Legendary 可执行文件的位置。此字段允许您覆盖该路径。

只有在您启用通过 Legendary 启动（见下文）时才需要指定 Legendary 可执行文件的正确位置，否则 SRM 不需要知道 Legendary 可执行文件的位置。

## Legendary `installed.json` 路径覆盖

大多数用户不应该使用此功能，因为他们使用标准的 `Legendary` 安装，已安装的游戏清单将位于 `~/.config/legendary/installed.json`。

然而，如果由于某种原因您的已安装游戏清单位于非典型位置，则可以在此处指定正确的清单路径。

## 通过 Legendary 启动 `[建议启用]`

顾名思义，此切换选项决定游戏是通过 Legendary 还是直接启动。通过 Legendary 启动可访问 Epic 的在线服务。
