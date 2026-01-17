# Wordle 猜单词游戏

Forked from [astrbot_plugin_wordle](https://github.com/Raven95676/astrbot_plugin_wordle)

> [!important]
> 猜单词时，直接对 Bot 说出单词即可。
>
> 你可以使用这些指令：
> 
> ```
> 开始游戏：/猜单词 (单词长度)
> 例如：/猜单词 6
> ```
> ```
> 获取提示：/猜单词 提示
> ```
> ```
> 结束游戏：/猜单词 结束
> ```
> 
> 这个版本响应聊天中的指令。
> 
> 如果你需要响应聊天中普通消息的版本，请前往 [astrbot_plugin_wordle_2_msg](https://github.com/whzcc/astrbot_plugin_wordle_2_msg) （即将弃用）。
>

<img width="1175" height="623" alt="image" src="https://github.com/user-attachments/assets/9ce8f08b-b61d-4dec-9135-0518434df450" />

Astrbot Wordle 游戏，支持指定位数——只需要单词表中存在该长度的单词。

**自定义词库和释义功能**。（修改在 ```.xxx.../wordlist``` 目录下的 json 文件。这里使用了 [nonebot-plugin-wordle](https://github.com/noneplugin/nonebot-plugin-wordle) 的单词表。）

**自定义显示字体**。（在 ```main.py``` 里替换 ```MinecraftAE.ttf``` 为所需字体，字体的大小和位置可能也需要调整。）

加入了**单词拼写检查**，用户的输入的单词不存在时则不会进行下一步。（通过 spellchecker 库和自定词库之一即可。）

与原版相比，还优化了 “**猜单词提示**”的功能。现在用户获取提示时，如果一个正确字母都没有猜出来，插件会告诉其随机位置上的字母；如果猜出了部分字母，则插件会告知其顺序。

原版似乎有一个无法向 QQ 平台发图片的 Bug（可能是因为试图发送 png 格式），这个项目换用 jpg，解决了这个 Bug。

增加了**随机提示词**。

添加了**防重复猜测**功能。

优化了一些细节。

启动时，插件会自动尝试安装 “pyspellchecker” 库。

2.2.2: 优化两个可能引发错误的全局变量，修改正则表达式检查可能产生的 Bug。
2.2.1：支持配置自定义拼写检查（支持正则表达式）
