# 本地 images `[支持变量]`{.noWrap}

Allows one to use images stored locally. A [special 通配符 输入](#special-通配符-输入) string is used to retrieve images, so for 示例 you might do `/路径/to/heroes/${标题}.@(png|jpg)`. Backslashes can be used to escape characters, so that if your images live in `艺术作品 [portraits]` you might do `/路径/to/艺术作品 \[portraits\]/${标题}.@(png|jpg)`. A good idea is to set your 艺术作品 目录 globally and then use the `${localimages}` dir environment 变量 in this 字段: `${localimagesdir}/emuname/heroes/${标题}.@(png|jpg)` for 示例.

Any 变量 you use in this 字段 that contains special 通配符 characters will have those characters escaped.

## Allowed 图像 extensions

Only `JPEG`{.noWrap}, `JPG`{.noWrap}, `PNG`{.noWrap} and `TGA`{.noWrap} 文件 extensions are supported. Even if 解析器 finds files with other extensions, they are not included into the final list.

## Can you move the 目录 of 本地 images after saving app list?

Yes, once the list is saved, 本地 images are copied to a Steam 目录 where they are renamed to 匹配 Steam's APP ID.
