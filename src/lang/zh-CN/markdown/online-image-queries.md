# 在线 图像 query `[支持变量]`{.noWrap}

Queries that are used to search for images. In order to set 图像 query, the following syntax must be used:

```
${...}
```

For 示例, images for "Legend of Zelda" and "The Legend of Zelda: A Link to the Past" can be queried like this:

```
${The Legend of Zelda}${The Legend of Zelda: A Link to the Past}
```

You will most likely want to use 解析器 variables for queries. Which will look like this (also the **默认** 值):

```
${${fuzzyTitle}}
```

The legacy **greedy** mode can be enabled by 设置 query to:

```
${${fuzzyTitle}}${${标题}}
```
