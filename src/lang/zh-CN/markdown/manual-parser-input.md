# Manual 解析器 Specific Inputs

## Manifests 目录 `[支持 Environment Variables]`{.noWrap}

The location of the json files you want to turn into Steam shortcuts. `Manifests 目录` is expected to be of the form:

```
/路径/to/manifests
--manifest1.json
--manifest2.json
--manifest3.json
...
```

The names of the files do not matter. 有什么作用 matter is that each `manifest.json` 文件 is either a single 标题, like so:

```json
{
  "标题": "gameTitle",
  "target": "game/路径/target.sh",
  "startIn": "game/路径",
  "launchOptions": "--args",
  "appendArgsToExecutable": false
}
```

Or a list of titles, like so:

```json
[
  {
    "标题": "gameTitle",
    "target": "game/路径/target.sh",
    "startIn": "game/路径",
    "launchOptions": "--args".
    "appendArgsToExecutable": true
  },
  {
    "标题": "gameTitle2",
    "target": "game2/路径/target.sh",
    "startIn": "game2/路径",
    "launchOptions": "--args2",
    "appendArgsToExecutable": false
  }
]
```

A typical use case would be to use a single json 文件 per game 类型, or per year, etc.

Just like for ROM parsers, `appendArgsToExecutable` determines whether `launchOptions` are appended to the shortcut `target` or appear separately as 启动选项 in Steam.
