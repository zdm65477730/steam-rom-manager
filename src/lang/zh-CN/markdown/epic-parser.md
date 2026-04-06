# Epic Games 解析器

此解析器从[Epic Games Store](https://store.epicgames.com/en-US/)导入游戏，以便可以为它们选择艺术作品并将其添加到Steam中。

如果它无法工作，那是因为Epic更改了他们的游戏清单结构，在这种情况下请通知SRM的开发者，我们会解决问题。

为了让此解析器能与开源的Epic替代品[Legendary](https://github.com/derrod/legendary)一起工作，[必须在Legendary中启用EGL同步](https://github.com/derrod/legendary/discussions/276#discussioncomment-709748)（这将创建解析器读取的适当文件，并且不需要安装`Epic Games Store`）。

也就是说，SRM中还有一个`Legendary`解析器，它可以开箱即用。

## 兼容性

此解析器目前仅在`Windows`和`Mac OS`系统上可用。在`Mac OS`上无法从Epic商店启动，因此该切换开关应保持禁用状态。