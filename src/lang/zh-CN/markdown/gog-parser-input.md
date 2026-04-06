# GOG Galaxy 解析器 Specific Inputs

## Galaxy 路径 Override

By 默认 Steam ROM Manager assumes your GOG Galaxy executable is located at `C:\Program Files (x86)\GOG Galaxy\GalaxyClient.exe` on Windows and `/Applications/GOG Galaxy.app/Contents/MacOS/GOG Galaxy` on Mac. This 字段 allows you to override that 路径 if your GOG Galaxy executable is elsewhere.

Specifying the correct location of GOG Galaxy's executable is only necessary if you 启用 launch via GOG Galaxy (see below), as 否则 SRM has no need of the location of GOG Galaxy's executable.

## Launch via GOG Galaxy `[Recommend disabled]`

What it sounds like, this toggle determines whether games launch via GOG Galaxy or directly. For some games launching from GOG Galaxy may fail, and the Steam overlay will most likely not work.

## Parse Linked Executables from GOG Galaxy

If enabled, SRM will pull in not only GOG games aquired from GOG Galaxy's store, but also those you have manually linked executables for in GOG Galaxy. This is desirable if those games are not being parsed into SRM elsewhere.

A caveat is that because GOG Galaxy does not store the names linked executables in its database, SRM will use the 目录 名称 of the executable on Windows (e.g. `C:\\路径\\to\\Hoa\\LaunchHoa.exe` would be assigned the 标题 `Hoa`) and the executable 名称 on Mac (e.g. `/Applications/Symphonia.app` would be assigned the 标题 `Symphonia`).

## Parse using Registry instead of Galaxy DB `[Windows only] [Recommend disabled]`

This 选项 will parse the Windows Registry for installed GOG games instead of GOG Galaxy's SQL database, allowing the 解析器 to work even if GOG Galaxy is not installed. If this is enabled, `Parse Linked Executables` will of have no effect, but `Launch via GOG Galaxy` will work as normal.
