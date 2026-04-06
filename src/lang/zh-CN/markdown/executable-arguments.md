# 命令行参数 `[支持变量]`{.noWrap}

附加到可执行文件以生成最终快捷方式的参数。大多数情况下，您需要使用提供的解析器变量来设置它。

## 按系统示例

### RetroArch

```
-L cores${/}YOUR_CORE.dll "${filePath}"
```

### Cemu (WiiU)

```
-f -g "${filePath}"
```

### Dolphin Emu (Gamecube和Wii)

```
--exec="${filePath}" --batch --confirm=false
```

### Project64 2.3+ (N64)

```
"${filePath}"
```

### Mupen64+ (N64)

```
--fullscreen "${filePath}"
```

### DeSmuME (Nintendo DS)

```
"${filePath}"
```

### mGBA (Gameboy, Gameboy Color,和Gameboy Advance)

```
-f "${filePath}"
```

### Nestopia (NES/Famicom)

```
"${filePath}" -video fullscreen bpp : 16 -video fullscreen width : 1024 -video fullscreen height : 768 -preferences fullscreen on start : yes -view size fullscreen : stretched
```

### higan (NES/Famicom, SNES/Famicom, Gameboy, Gameboy Color, Gameboy Advance)

```
"${filePath}"
```

### nullDC (Sega Dreamcast)

```
-config nullDC_GUI:Fullscreen=1 -config ImageReader:DefaultImage="${filePath}"
```

### Kega Fusion (Sega Genesis和Sega 32X)

```
"${filePath}" -gen -auto -fullscreen
```

### RPCS3 (Sony Playstation 3)

```
"${filePath}"
```

### PCSX2 (Sony Playstation 2)

```
--fullscreen --nogui "${filePath}"
```

### PCSX-R (Sony Playstation 1)

```
-nogui -cdfile "${filePath}"
```

### ePSXe (Sony Playstation 1)

```
-f -nogui -loadbin "${filePath}"
```

### Xebra (Sony Playstation 1)

```
-IMAGE "${filePath}" -RUN1 -FULL
```

### Mednafen (Sony Playstation 1, NES/Famicom, SNES/Super Famicom等)

```
"${filePath}"
```

### PPSSPP (Sony Playstation Portable)

```
"${filePath}"
```

## "将参数附加到可执行文件"有什么作用？

不是将参数添加到Steam的启动选项：

![未附加参数](../../../assets/images/cmd-not-appended.png) {.fitImage .center}

而是如下所示将参数附加到目标：

![附加参数](../../../assets/images/cmd-appended.png) {.fitImage .center}

此设置用于影响Steam的APP ID。

## 目录变量

| 变量（不区分大小写） | 对应值 |
| --------------------------: | :---------------------------------------- |
|                 `${exeDir}` | 可执行文件目录 |
|                 `${romDir}` | ROM目录 |
|               `${steamDir}` | Steam目录 |
|             `${startInDir}` | "启动于"目录 |
|                `${fileDir}` | 解析器返回的文件或目录 |

如果可执行文件目录输入留空，`${exeDir}`{.noWrap} 等同于 `${fileDir}`{.noWrap}。此外，如果"启动于"目录留空，`${startInDir}`{.noWrap} 等同于 `${exeDir}`{.noWrap}。

## 名称变量

| 变量（不区分大小写） | 对应值 |
| --------------------------: | :-------------------------------------------------------------- |
|                `${exeName}` | 可执行文件名称（不含扩展名） |
|               `${fileName}` | 解析器返回的文件名称（不含扩展名） |

如果可执行文件目录输入留空，`${exeName}`{.noWrap} 等同于 `${fileName}`{.noWrap}。

## 扩展名变量

| 变量（不区分大小写） | 对应值 |
| --------------------------: | :------------------------------------------------------------ |
|                 `${exeExt}` | 可执行文件扩展名（带点） |
|                `${fileExt}` | 解析器返回的文件扩展名（带点） |

如果可执行文件目录输入留空，`${exeExt}`{.noWrap} 等同于 `${fileExt}`{.noWrap}。

## 路径变量

| 变量（不区分大小写） | 对应值 |
| --------------------------: | :------------------------------------------------- |
|                `${exePath}` | 可执行文件的完整路径 |
|               `${filePath}` | 解析器返回的文件的完整路径 |

如果可执行文件目录输入留空，`${exePath}`{.noWrap} 等同于 `${filePath}`{.noWrap}。

## 解析器变量

| 变量（不区分大小写） | 对应值 |
| --------------------------: | :----------------------------------------------- |
|                  `${title}` | 提取的标题 |
|             `${fuzzyTitle}` | 模糊匹配的标题 |
|             `${finalTitle}` | 标题修饰符的最终结果标题 |

如果模糊匹配失败或被禁用，`${fuzzyTitle}`{.noWrap} 等同于 `${title}`{.noWrap}。

## 函数变量

| 变量（不区分大小写） | 对应函数 |
| ------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------- |
|               `${regex\|input\|substitution(optional)}` | 在输入上执行正则表达式。支持 `u`、`g` 和 `i` 标志（捕获组被连接，除非提供了替代内容） |
|                                          `${uc\|input}` | 大写变量。将输入转换为大写 |
|                                          `${lc\|input}` | 小写变量。将输入转换为小写 |
|                                    `${cv:group\|input}` | 用匹配的自定义变量更改输入（组是可选的） |
|                                         `${rdc\|input}` | 用拉丁字母等价物替换变音符号输入字符 |
| `${os:[win\|mac\|linux]\|on match\|no match(optional)}` | 如果操作系统匹配，则使用 `on match` 值，否则使用 `no match` |

### 函数变量示例

假设 `${title}` 变量等于 `Pokémon (USA) (Disc 1).iso`。那么这些变量：

```
${/.*/|${title}}                           //匹配所有内容
${/(.*)/|${title}}                         //捕获所有内容
${/(\(.*?\))/|${title}|}                   //捕获所有括号并替换为空
${/(\(Disc\s?[0-9]\))/|${title}}           //捕获"Disc..."部分
${uc|${/(\(Disc\s?[0-9]\))/|${title}}}     //捕获"Disc..."部分并转换为大写
${rdc|${title}}                            //替换变音符号字符（在这种情况下：é -> e）
file${os:linux|.so|${os:win|.dll}}         //为操作系统选择正确的文件扩展名
```

将被替换为这些：

```
Pokémon (USA) (Disc 1).iso
Pokémon (USA) (Disc 1).iso
Pokémon.iso
(Disc 1)
(DISC 1)
Pokemon (USA) (Disc 1).iso

--在Linux上:
file.so
--在Windows上:
file.dll
--在Mac OS上:
file
```
