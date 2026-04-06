# Epic Games 解析器

This 解析器 imports games from the [Epic Games Store](https://store.epicgames.com/en-US/) so that 艺术作品 can be chosen for them and they can be added into Steam.

If it doesn't work it is because Epic has altered the structure of their game manifests, 在这种情况下 please let the developers of SRM know and we will resolve the issue.

In order for this 解析器 to work with the open source Epic alternative [Legendary](https://github.com/derrod/legendary), [EGL sync must be enabled in Legendary](https://github.com/derrod/legendary/discussions/276#discussioncomment-709748) (this creates the appropriate files for the 解析器 to read, and does not require the `Epic Games Store` to be installed).

That said, there is also a `Legendary` 解析器 in SRM which works right out of the box.

## Compatibility

This 解析器 is currently functional on `Windows` and `Mac OS` systems only. On `Mac OS` it is not possible to launch from the Epic Store, so that toggle should remain disabled.
