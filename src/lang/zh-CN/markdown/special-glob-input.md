# Special 通配符 输入

## How does it work?

图像 paths are resolved in 4 step process:

1. String is evaluated to see if a 通配符 based 解析器 is used. Depending on the result, further parsing may continue with `2` 通配符 sets.
1. All provided variables are replaced with their corresponding values.
1. New string(s) is/are resolved against root 目录 (root 目录 is always a configuration's ROMs 目录).
1. Final string(s) is/are passed to 通配符 解析器 which then returns a list of available files.

## Usage 示例

### Absolute paths

Let's say that the extracted 标题 is `Metroid Fusion [USA]` and 模糊 标题 is `Metroid Fusion`. You can then construct an 图像 路径 like this:

- `C:/路径/to/images/${标题}.*`
- `C:/路径/to/images/${fuzzyTitle}.*`

which will be resolved to this:

- `C:/路径/to/images/Metroid Fusion [USA].png`
- `C:/路径/to/images/Metroid Fusion.jpg`

### Relative paths

For this 示例, let's say that ROMs 目录 is `C:/ROMS/GBA` and rom itself is `C:/ROMS/GBA/Metroid Fusion [USA].gba`. Set up a relative 路径, using `${filePath}`{.noWrap} or `${dir}`{.noWrap} variables, for 示例:

- `${filePath}/../../../路径/to/images/${标题}.*`
- `${dir}/../../路径/to/images/${标题}.*`

will be replaced like this:

- `C:/ROMS/GBA/Metroid Fusion [USA].gba/../../../路径/to/images/Metroid Fusion.*`
- `C:/ROMS/GBA/../../路径/to/images/Metroid Fusion.*`

Here `..` means "traverse back" and it allows to go back to previous 目录:

- `C:/ROMS/GBA/Metroid Fusion [USA].gba/../../../路径/to/images/Metroid Fusion.*`
  - `C:/ROMS/GBA/../../路径/to/images/Metroid Fusion.*`
    - `C:/ROMS/../路径/to/images/Metroid Fusion.*`
      - `C:/路径/to/images/Metroid Fusion.*`
- `C:/ROMS/GBA/../../路径/to/images/Metroid Fusion.*`
  - `C:/ROMS/../路径/to/images/Metroid Fusion.*`
    - `C:/路径/to/images/Metroid Fusion.*`
