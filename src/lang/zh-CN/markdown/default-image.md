# 默认 图像 `[支持变量]`{.noWrap}

Allows one to use an 图像, stored locally, as a 默认/fallback 图像. A [special 通配符 输入](#special-通配符-输入) string is used to retrieve images. Only the first retrieved 图像 is used.

This 图像 will be shown **only** if there are no other images available. If Steam 图像 is available, you will be able to choose from Steam and this 图像.

## Allowed 图像 extensions

Only `JPEG`{.noWrap}, `JPG`{.noWrap}, `PNG`{.noWrap} and `TGA`{.noWrap} 文件 extensions are supported. Even if 解析器 finds files with other extensions, they are not included into the final list.

## Can you move the 目录 of 默认 图像 after saving app list?

Yes, once the list is saved, 默认 图像 is copied to a Steam 目录 where they are renamed to 匹配 Steam's APP ID.
