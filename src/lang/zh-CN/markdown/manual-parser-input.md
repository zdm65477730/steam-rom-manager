# 手动解析器特定输入

## Manifests 目录 `[支持环境变量]`{.noWrap}

您希望转换为 steam 快捷方式的 json 文件的位置。`Manifests 目录` 应该是以下形式：

```
/路径/to/manifests
--manifest1.json
--manifest2.json
--manifest3.json
...
```

文件的名称无关紧要。重要的是每个 `manifest.json` 文件要么是单个标题，如下所示：

```json
{
  "title": "gameTitle",
  "target": "game/路径/target.sh",
  "startIn": "game/路径",
  "launchOptions": "--args",
  "appendArgsToExecutable": false
}
```

或者是一系列标题，如下所示：

```json
[
  {
    "title": "gameTitle",
    "target": "game/路径/target.sh",
    "startIn": "game/路径",
    "launchOptions": "--args",
    "appendArgsToExecutable": true
  },
  {
    "title": "gameTitle2",
    "target": "game2/路径/target.sh",
    "startIn": "game2/路径",
    "launchOptions": "--args2",
    "appendArgsToExecutable": false
  }
]
```

一个典型的用例是为每种游戏类型或每年使用单个 json 文件等。

与 ROM 解析器一样，`appendArgsToExecutable` 决定 `launchOptions` 是附加到快捷方式 `target` 还是在 steam 中作为启动选项单独出现。
