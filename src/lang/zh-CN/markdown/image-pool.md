# 艺术作品 pool `[支持变量]`{.noWrap}

Defaults to `${fuzzyTitle}`{.noWrap} if 字段 is unset.

This 字段 is used to allow games from different parsers to share the same images (i.e. the same "图像 pool") if they have the same 标题.
If you want different parsers not to share images for games with the same 标题, just set this 字段 to something unique, for 示例 `${fuzzyTitle} SNES`{.noWrap} or `${fuzzyTitle} ${parserTitle}`{.noWrap}.
