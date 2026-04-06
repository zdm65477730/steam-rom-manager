# 通配符 解析器 Specific Inputs

## 用户's 通配符

This is where you create your 通配符 for extracting 标题 from 文件 路径. Please read all of [special 通配符 characters](#special-通配符-characters) if you don't know how to construct a 通配符.

## How does it work?

In addition to special 通配符 characters, 通配符 解析器 requires you to enter `${标题}`{.noWrap} 变量. 解析器 will locate it's position inside your **通配符**, for 示例:

| 用户's 通配符            | Position                    |
| ---------------------- | --------------------------- |
| `${标题}/*/*.txt`     | First level from the left   |
| `{*,*/*}/${标题}.txt` | First level from the right  |
| `**/${标题}/*.txt`    | Second level from the right |

After acquiring `${标题}`{.noWrap} position, `${标题}`{.noWrap} will be replaced with a wildcard `*`.

## Limitations

Position extraction comes with some limitations -- 通配符 is invalid if position can not be extracted. Most of the time you will be warned about what you can't do, however, if you find a combination that is allowed, but produces incorrect titles please make an issue at [github](https://github.com/FrogTheFrog/Steam-rom-manager/issues).
