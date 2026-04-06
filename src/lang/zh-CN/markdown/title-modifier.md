# 标题 modifier `[支持变量]`{.noWrap}

Defaults to `${fuzzyTitle}`{.noWrap} if 字段 is unset. This 设置 can be used to prepend or append desired characters to a Steam shortcut's `标题`. For 示例, given that `${fuzzyTitle}`{.noWrap} is `Zelda 2`, you can add ` (1.7.5)` to it by 设置 值 to:

```
${fuzzyTitle} (1.7.5)
```

You can use `${标题}`{.noWrap} or any other 变量 to construct the final 标题.

This 设置 influences Steam's APP ID.
