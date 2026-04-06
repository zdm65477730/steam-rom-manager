# 标题 from 自定义 变量

Allows one to 覆盖 the extracted 标题 with a 自定义 变量, pulled from the `json` files described below. This happens right after 标题 extraction, meaning that the new 标题 can be used for 模糊 matching and so on. Groups and variables themselves are **区分大小写**, unless case-insesitive 变量 选项 is enabled.

标题 matching is limited to specific groups of 自定义 variables. For 示例, this is how you specify groups "FBN" and "PSN":

```
${RPCS3}${PSN}
```

# How it works

There are two 变量 files, `customVariables.json` which is maintained by SRM (don't change this one, your changes will be overwritten every time SRM restarts) and `userVariables.json` which is where you should put your own variables. Both files are located in SRM's `Config 目录`.

Both `customVariables.json` and `userVariables.json` have the same JSON structure. SRM will throw an 错误 unless the following JSON structure is used:

```
{
    "Group1": {
        "NPUB30698": "Catherine",
        "NPUB30024": "1942: Joint Strike",
        ...
    },
    "Group2": {
        "The Legend Of Zelda": "The Legend Of Link",
        ...
    },
    ...
}
```

Then if your 用户 通配符 were `romsdir/${标题}.wad` and you had a `The Legend of Zelda.wad` located in `romsdir`, you would set the 标题 from 自定义 变量 字段 to `${Group2}` to obtain a 标题 of "The Legend of Link".

## 不区分大小写 variables

If enabled, 不区分大小写 matching will be done and first matched 自定义 变量 will be used.

## Skip 文件 if 变量 not found

If enabled, titles that don't 匹配 a 变量 will be excluded.
