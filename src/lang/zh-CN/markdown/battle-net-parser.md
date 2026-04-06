# Battle.net 解析器

此解析器从`Battle.net`应用程序导入游戏，以便可以为它们选择艺术作品并将其添加到Steam中。如果它无法工作，那是因为暴雪更改了他们的数据库文件结构，在这种情况下请通知SRM的开发者，我们会解决问题。

`Battle.net`解析器有些特别，它使用位于`${srmDir}/scripts/bnet.ps1`的shell脚本来启动`Battle.net`，等待适当的时间，然后再启动实际的游戏标题。
