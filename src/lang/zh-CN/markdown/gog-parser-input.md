# GOG Galaxy 解析器特定输入

## Galaxy 路径覆盖

默认情况下，Steam ROM Manager 假定您的 GOG Galaxy 可执行文件在 Windows 上位于 `C:\Program Files (x86)\GOG Galaxy\GalaxyClient.exe`，在 Mac 上位于 `/Applications/GOG Galaxy.app/Contents/MacOS/GOG Galaxy`。如果您的 GOG Galaxy 可执行文件在其他位置，此字段允许您覆盖该路径。

只有在您启用通过 GOG Galaxy 启动（见下文）时才需要指定 GOG Galaxy 可执行文件的正确位置，否则 SRM 不需要知道 GOG Galaxy 可执行文件的位置。

## 通过 GOG Galaxy 启动 `[建议禁用]`

顾名思义，此切换选项决定游戏是通过 GOG Galaxy 还是直接启动。对于某些游戏，从 GOG Galaxy 启动可能会失败，并且 Steam 覆盖层很可能无法工作。

## 从 GOG Galaxy 解析链接的可执行文件

如果启用，SRM 不仅会拉取从 GOG Galaxy 商店获取的 GOG 游戏，还会拉取您在 GOG Galaxy 中手动链接可执行文件的那些游戏。如果您在其他地方没有将这些游戏解析到 SRM 中，这是可取的。

需要注意的是，由于 GOG Galaxy 不在其数据库中存储链接可执行文件的名称，SRM 将在 Windows 上使用可执行文件的目录名称（例如 `C:\\path\\to\\Hoa\\LaunchHoa.exe` 将被分配标题 `Hoa`）和在 Mac 上使用可执行文件名称（例如 `/Applications/Symphonia.app` 将被分配标题 `Symphonia`）。

## 使用注册表而不是 Galaxy 数据库进行解析 `[仅限 Windows] [建议禁用]`

此选项将解析 Windows 注册表中的已安装 GOG 游戏，而不是 GOG Galaxy 的 SQL 数据库，从而允许解析器即使在未安装 GOG Galaxy 的情况下也能工作。如果启用此选项，`解析链接的可执行文件` 将不起作用，但 `通过 GOG Galaxy 启动` 将正常工作。
