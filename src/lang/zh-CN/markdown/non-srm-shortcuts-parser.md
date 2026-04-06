# 非SRM快捷方式解析器

此解析器将非SRM的steam快捷方式导入SRM，以便管理它们的艺术作品。它不会添加快捷方式，因此是一个`仅艺术作品`解析器。此解析器需要设置`用户账户`字段。

## 用户账户

用于限制配置到特定用户账户。要设置用户账户，必须使用以下语法：

```
${...}
```

如果启用了[使用账户凭据](#what-does-use-账户-credentials-do)，您**必须**使用您**登录**Steam时使用的用户名：

![账户示例](../../../assets/images/user-account-example.png) {.fitImage .center}

例如，这是为"Banana"和"Apple"指定账户的方法：

```
${Banana}${Apple}
```

您也可以通过直接指定ID来限制账户。例如：

```
${56489124}${21987424}
```

这将把搜索限制在`steam/userdata/56489124`和`steam/userdata/21987424`。
