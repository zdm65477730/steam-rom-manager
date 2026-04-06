# "Start In" 目录 `[supports env variables]`

If `"Start In" 目录` is unset it defaults to the executable's 目录. If not executable is set, it defaults to the 目录 of the ${filePath} 变量:

![默认 "Start In" 目录](../../../assets/images/默认-start-in-目录.png) {.fitImage .center}

This 选项 allows you to specify any 目录 you want as a "Start In" 目录:

![Ner "Start In" 目录](../../../assets/images/new-start-in-目录.png) {.fitImage .center}

It is useful when you're using batch files to start emulator and a game, but emulator requires a specific "Start In" 目录 to work properly.

## Shortcut Passthrough

If you 启用 "Follow .lnk to destination" and your executable is a ".lnk" 文件, ie a shortcut, then whatever you put in this 字段 will be overridden with the 目录 of the target of that shortcut. In the future, it will be overridden with the start in 目录 of that shortcut.
