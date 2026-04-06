# What is Steam's APP ID?

Steam uses APP ID to identify games. For non-Steam games they are generated using:

- Executable;
- Final app 标题.

If you use `RetroArch` or similar emulators to add the same game, but on different consoles, you will encounter a problem where only **one** 标题 is added and others just disappear. This is due to duplicate APP IDs.

## Adding identical titles from different consoles

Steam APP ID must not be identical. This can be achieved by changing **标题 modifier** 值 or enabling **将参数附加到可执行文件**. Second 选项 adds a third 变量 to APP ID:

- Executable;
- Final app 标题;
- 命令行参数.

Most of the time command line will contain unique game 路径 which should allow to generate unique APP IDs.
