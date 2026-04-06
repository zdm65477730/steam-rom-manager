## Environment variables

These variables are pre parsed and can be used even in the Rom 目录, Steam 目录, Executable Location, and Start In Dir 字段s.
|变量 (不区分大小写)|Corresponding 值|
|---:|:---|
|`${/}`|System specific 目录 separator: `\` or `/`|
|`${srmdir}`|目录 of portable SRM executable|
|`${steamdirglobal}`|全局 Steam 目录, specified in `Settings`|
|`${accountsglobal}`|全局 用户 accounts, specified in `Settings`|
|`${romsdirglobal}`|全局 ROMs 目录, specified in `Settings`|
|`${retroarchpath}`|路径 to Retroarch executable, specified in `Settings`|
|`${racores}`|目录 of retroarch cores, specified in `Settings`|
|`${localimagesdir}`|目录 of your 本地 images, specified in `Settings`|

The utility of the environment 变量 `${srmdir}` is to make SRM fully portable, eg if you wanted to have the 目录 layout `D:\Games\Roms` and `D:\Games\PortableSRM\SRM.exe` then 设置 the 字段 Roms 目录 to be `${srmdir}${/}..${/}Roms` would allow you to move the Games 目录 somewhere else without breaking your setup.

函数 variables can also be used in 字段s that permit environment variables (e.g. `${os:win|C:\路径\to\startdir|${os:linux|/路径/to/startdir}}`)
