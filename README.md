学习目的~~~///(^v^)\\\~~~

访问 [releases 页面](https://github.com/ludoux/LrcHelper/releases/latest) 来获得最新的发布版本。

-----
yu修改自用版
修改了 LrcHelper/SharedFramework.cs 中355行之后以适配我的mp3
其中出现了点小问题（.............连续出现太多会把设备卡死，奇怪的bug增加了！ ![Snipaste_2021-04-17_22-22-03](https://user-images.githubusercontent.com/44089074/115116305-71b81900-9fcb-11eb-9cf6-122fb1e098b8.png)）


-----

**运行要 .NET Framework 4.7.2 的支持**

针对网易云音乐开发，根据提供的歌曲/歌单/专辑 ID，自动下载整理歌词（含翻译）的功能。

## 不同之处

- [x] 可以将原文歌词和翻译分离，套用不同的时间轴
- [x] 特别为 SONY®WALKMAN® A25 系列屏幕适配，可以尽量将歌词同屏显示
- [x] 可以人工修正上游源歌词的错误

## Screenshots

![LrcDownloader](https://raw.githubusercontent.com/Ludoux/LrcHelper/master/Pic/LrcDownloader.png)

## 基本操作方法

浏览 [wiki](https://github.com/Ludoux/LrcHelper/wiki) 页面了解更多

`AUTO-SET`开启时，复制链接（网页端见地址栏，桌面应用轻敲分享-复制链接）后将软件切入前台，软件将自动填充信息。当然也可以自行填充 ID 并选择对应的类型。

如有需要可以勾选高级设置（AdvancedSettings）来启用更多功能（请浏览 wiki）。

然后点击按钮“下载”。

1. 若为是音乐 ID，.lrc 文件（UTF-8）会在软件所处目录下生成，结束时会在 Status 处显示详情。
2. 若为是歌单/专辑 ID，.lrc 文件（UTF-8）会在软件所处目录的以歌单名命名的文件夹中生成，结束时会在 状态处显示详情，更具体信息请查看生成的 Log.txt 文件。

## Tips

1. 翻译比外文歌词默认慢一秒，可以在高级设置中更改。
2. 目前歌词歌单仅支持网易云。~~在很久远的未来会以附加组件的方式进行弥补。~~

## Known Bugs

1. 稳定性。

## TODO


1. ~~增加歌曲信息，歌词信息等，Tag 更多方法。~~
2. ~~写其它的歌词文件处理方法。~~
3. ~~继续封装，完善代码安全性和可维护性。~~

（半弃坑，小修小补，sorry 啦）

## License

在 MIT 协议下发布。

## 参考&感谢

感谢 [@stevennight](https://github.com/stevennight) 的帮助！让本来没有时间维护（因为暂时没有电脑和捡到了一个女朋友）的工具起死回生……

获取外文歌词的代码基于 ituff 的 [163lyric项目](https://github.com/ituff/163lyric) 的实现思路，进行了修改。（但是 ituff 并没有指定那个项目的开源协议）

感谢 Moonlib.com 的所有人 Moon 在这个博客上发表了 [自己整理的API](http://moonlib.com/606.html) 。

## 更新信息（最近在上）

* 2020.11.26 [#14](https://github.com/ludoux/LrcHelper/issues/14)
* 2019.07.29 [#3](https://github.com/ludoux/LrcHelper/issues/3) 试图“修复”一个远古 bug：现在最新的桌面版用英文半角`,`来在文件名区分不同歌手，但好像 UWP 版本只默认取第一个，这里软件遵循桌面版的逻辑。把提示一些文本改中文了。(v2.1.1 #Release)
* 2019.07.29 更改了歌单 API 接口以支持1k+歌曲的歌单。微调了界面。(v2.1.0 #Release)
* 2019.06.17 修正获取歌曲信息时的错误。界面中文化。切换更新渠道。(v2.0.13 #Release)
* 2018.05.13 修正获取歌曲信息时的错误。 修正长ID产生的错误。 修正原文翻译之间的延迟设置为负数时，不能正确从配置读入的问题。 (v1.0.12 #Release)
* 2017.11.11 支持人工介入修正上游源文本错误（ReviseRaw）。修改了邮箱地址和部分措辞。（v1.0.11 #Release）
* 2017.10.13 （v1.0.10 #Release）
* 2017.9.30 延时填负数可以让翻译先显示，原文后显示。
* 2017.8.22 增加 “Save” 以保存高级设置。（v1.0.9 #Release）
* 2017.8.18 微小的优化；增加 “Need Help?” 导向 wiki 页面。
* 2017.8.14 移除了 Newtonsoft.json；修正了对非法字符的处理逻辑。
* 2017.8.8  允许多个 tag 值。（v1.0.8 #Release）
* 2017.8.6  增加了 FilenamePattern 功能，背后是重新实现了写文本文件的逻辑，还有对网易云音乐上歌曲歌手专辑等的获取；各种大大小小的优化。
* 2017.7.12 优化了下代码，使用枚举。（v1.0.7 #Release）
* 2017.7.11 修 bugs；更改了新的功能（case 1）中部分符号的大小（倍率？），增加了新的符号；更改了关键函数的实现，部分更改为属性；写了点注释。
* 2017.7.10 新的功能正式提供了，可以在高级设置中启用（填 1）；高级设置也支持调整延时。（v1.0.6 #Release）
* 2017.7.6  或许支持了新的翻译歌词显示形式：尽可能地同屏显示原文和翻译。
* 2017.6.7  （v1.0.5 #Release）
* 2017.6.5  功能增加：支持了直接从专辑（album）链接下载歌词，不用再保存为歌单。近一个月的时间在修 bug：tag 采用白名单模式，不符合的 pass 掉以免进入时轴处理。对并行处理有了错误捕获。采用 https 链接。使用 int64 存储 ID 因为测试时遇到了长 ID 直接爆掉……（#Weekly）
* 2017.5.1  支持 offset ，稳定性提升。（#Weekly）（v1.0.4 #Release）
* 2017.4.29 软件支持检查更新，修上次更新出现的 bug ，升级框架到4.6.2。（#Weekly）（v1.0.3 #Release）
* 2017.4.14 修 Bug，清理无用代码。支持同行多个时间轴，支持排序。（#Weekly）
* 2017.4.2  日常修 bug，Json.NET 升为 10.0.2，更改核心代码，将时间轴以 int 方式存储方便以后排序，更改了翻译延时处理的方法，清理了原本的过时的时轴规范方法。（换用最新的 Visual Studio 2017 而且升级过程异常顺利）（#Weekly）
* 2017.3.12 可以取消（Cancel）操作了（#Weekly）（v1.0.2 #Release）
* 2017.3.11 更改了核心代码——允许空白歌词（含翻译）存在，对翻译处理更大度，更改了对于翻译是否存在的实现，修复了一个经常发生关于延迟修复的bug。注意 cancel 仍有问题。（#Weekly）
* 2017.2.17 删除一无用方法，进入代码优化阶段。（#Weekly）
* 2017.2.12 新增了 Auto-Set 功能，使用更方便。（#Weekly）
* 2017.2.5  允许取消操作，有 BUG，使用 Task 实现 UI 和下载线程分离，修复 LICENSE 编码错误，不稳定的代码版本。
* 2017.2.4  使用了 TPL 类库实现了并行循环下载 @Playlist 模式，速度较原先提高了（效果因设备而异）；优化代码，Fix Bugs。（v1.0.1 #Release）
* 2017.1.25 粗略的代码重构，重写了实现。未广泛测试。（v1.0.0 #Release）
* 2016.9.2  Fix Bugs。（v0.0.0-beta #Release）
* 2016.8.30 Log 文件内容实现对齐，AUTO 实现执行线程与 UI 线程分离，可实时看进度与错误数。
* 2016.8.29 初版。
