# Executable `[supports env variables]`

路径 to emulator's executable. Can be a 文件 or any valid system 路径.

## Why 可选?

In some cases you might want to run game from a some kind batch 文件 which will also automatically run the emulator itself. If that is the case, then providing executable is unnecessary.

The final shortcut will just be `"${filePath}" --command-line-args`.

### So, how do I add files to Steam without 默认 executable?

All files retrieved by a 解析器 will be treated as executables instead.
