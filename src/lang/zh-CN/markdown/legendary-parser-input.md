# Legendary 解析器 Specific Inputs

## Legendary 路径 Override

By 默认 Steam ROM Manager uses `(Get-Command legendary).路径` on Windows and `which legendary` on Linux and Mac to determine the location of your Legendary executable. This 字段 allows you to override that 路径.

Specifying the correct location of the Legendary executable is only necessary if you 启用 launch via Legendary (see below), as 否则 SRM has no need of the location of Legendary's executable.

## Legendary `installed.json` 路径 Override

Most users shouldn't use this, as they use the standard `Legendary` installation where installed games manifest will be located at `~/.config/legendary/installed.json`.

If, however, for some reason your installed games manifest is located in a non-typical location then you can specify the correct manifest 路径 here.

## Launch via Legendary `[Recommend enabled]`

What it sounds like, this toggle determines whether games launch via Legendary or directly. Launching via Legendary provides access to Epic's 在线 services.
