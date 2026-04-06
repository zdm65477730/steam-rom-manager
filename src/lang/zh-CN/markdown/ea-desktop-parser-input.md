# EA Desktop 解析器 Specific Inputs

## EA Games 目录 Override

By 默认 Steam ROM Manager assumes your `EA Desktop` games are installed at `C:\Program Files\EA Games\`. This 字段 allows you to change that to wherever your games are installed, e.g. `D:\Games\EA Games`.

## Launch Games Via EA Desktop

If enabled SRM will add a shortcut to `origin2://game/launch/?offerIds=${gameid}` instead of just the game's executable. This ensures the game launches via EA and will have access to 在线 services.

`This is 必需 to add EA Play games. EA Play games will not be detected if this is not toggled on.`
