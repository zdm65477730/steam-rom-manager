# 通配符-正则表达式 解析器 Specific Inputs

## 用户's 通配符-正则表达式

This is where you create your 通配符 for extracting 标题 from 文件 路径. Please read all of [special 通配符 characters](#special-通配符-characters) if you don't know how to construct a 通配符.

## How does it work?

In addition to special 通配符 characters, 通配符 解析器 requires you to enter `${/.../}`{.noWrap} 变量. 解析器 will locate it's position inside your 通配符, for 示例:

| 用户's 通配符           | Position                    |
| --------------------- | --------------------------- |
| `${/.+/}/*/*.txt`     | First level from the left   |
| `{*,*/*}/${/.+/}.txt` | First level from the right  |
| `**/${/.+/}/*.txt`    | Second level from the right |

After acquiring `${/.../}`{.noWrap} position, `${/.../}`{.noWrap} will be replaced with a wildcard `*`.

## 正则表达式 post-processing

After 标题 extraction, 标题 will be processed by a regular expression. There are 3 ways you can write a regular expression.

### Regular expression with no capture: `${/.+/}`{.noWrap}

This is practically identical to "通配符" 解析器 -- every piece of extracted 标题 will be used.

### Regular expression with capture brackets: `${/(.+)/}`{.noWrap}

Multiple matches and capture groups are allowed. For 示例, here we have 2 匹配 groups with multiple capture groups:

```
${/(.*?)\s*\[USA\]\s*(.+)|(.*)/}
```

First 匹配 group (from left to right) with all correct captures will be used. Furthermore, all capture groups will be **joined**.

### Regular expression with capture brackets and replacement text: `${/(.+)/|...}`{.noWrap}

Similar to [regular expression with capture brackets](#regular-expression-with-capture-brackets) 除了 how it handles 捕获组. Replacement text can be used to move around 捕获组. For 示例:

```
${/(.*?)\s*\[USA\]\s*(.+)/|Second capture group: "$2" precedes the first one, which is "$1" }
```

If our first capture group is `Legend of Zelda` and second one is `SUPER EDITION`, then we will get the following (not very useful) 标题:

`Second capture group: "SUPER EDITION" precedes the first one, which is "Legend of Zelda"`

Untouched text will remain by 默认, so if you see some trailing characters be sure to add `.*` at the end or `.*?` at the begging of regular expression.

### Supported 标志

Allowed 标志 are `i`, `g` and `u`.

## Limitations

Position extraction comes with some limitations -- 通配符 is invalid if position can not be extracted. Most of the time you will be warned about what you can't do, however, if you find a combination that is allowed, but produces incorrect titles please make an issue at [github](https://github.com/FrogTheFrog/Steam-rom-manager/issues).
