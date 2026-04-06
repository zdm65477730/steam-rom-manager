# EA Desktop 解析器特定输入

## EA Games 目录覆盖

默认情况下，Steam ROM Manager 假定您的 `EA Desktop` 游戏安装在 `C:\Program Files\EA Games\`。此字段允许您将其更改为您的游戏安装位置，例如 `D:\Games\EA Games`。

## 通过 EA Desktop 启动游戏

如果启用，SRM 将添加一个指向 `origin2://game/launch/?offerIds=${gameid}` 的快捷方式，而不是仅使用游戏的可执行文件。这确保游戏通过 EA 启动并能访问在线服务。

`添加 EA Play 游戏时这是必需的。如果不开启此选项，EA Play 游戏将不会被检测到。`
