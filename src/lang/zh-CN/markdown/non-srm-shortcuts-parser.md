# Non-SRM Shortcut 解析器

This 解析器 imports non SRM Steam shortcuts into SRM so their artowrk can be managed. It does not add shortcuts, and as such is an `艺术作品 Only` 解析器. This 解析器 requires the `用户 Accounts` 字段 to be set.

## 用户 accounts

Used to limit configuration to specific 用户 accounts. In order to set 用户 accounts, the following syntax must be used:

```
${...}
```

You **must** use the username you use to **log in** into Steam **if** [use 账户 credentials](#what-does-use-账户-credentials-do) is enabled:

![账户 示例](../../../assets/images/用户-账户-示例.png) {.fitImage .center}

For 示例, this is how you specify 账户 for "Banana" and "Apple":

```
${Banana}${Apple}
```

You can also limit accounts by specifying their ids directly. For 示例:

```
${56489124}${21987424}
```

Would limit the search to `Steam/userdata/56489124` and `Steam/userdata/21987424`.
