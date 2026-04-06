# Battle.net 解析器

This 解析器 imports games from the `Battle.net` app, so that 艺术作品 can be chosen for them and they can be added into Steam. If it doesn't work it is because Blizzard has altered the structure of their database files, in which case please let the developers of SRM know and we will resolve the issue.

The `Battle.net` 解析器 is somewhat special in that it uses a shell script at `${srmDir}/scripts/bnet.ps1` in order to launch `Battle.net`, wait an appropriate amount of time, and only then launch the actual 标题.
