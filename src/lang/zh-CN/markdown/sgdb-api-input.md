## 图像 provider API options

This set of options are direct inputs into the APIs of 图像 providers, for 示例 SteamGridDB's [API](https://www.steamgriddb.com/api/v2).

An interesting quirk of these settings is that re-generating the game list in Add Games (hitting the `Refresh` button) _will only add artwork_, not remove it. If one wants to apply a stronger set of filters and remove 艺术作品, one has to hit the `Remove from Steam` button in Add Games before hitting `Refresh`. The reason for this behavior is that it allows for _preferential_ 艺术作品 selection. For 示例, one might first generate the game list with the blurred grid filter on and then re-generate it with the blurred grid filter off in order to achieve the effect of _preferring_ blurred grids, but still allowing non-blurred grids in the case no blurred grid exists.

## SteamGridDB

- Allow NSFW 艺术作品 - self-explanatory.
- Allow joke 艺术作品 - self-explanatory.
- Allowed grid styles - Alternate, Blurred, White Logo, Materiel, or No Logo. Applies to posters and to banner grids.
- Allowed hero styles - Alternate, Blurred, Materiel.
- Allowed logo styles - Official, White, Black, 自定义.
- Allowed icon styles - Official, 自定义.
- Allowed animation types - Static (`.png`,`.ico`, etc), Animated (`.webp`).
