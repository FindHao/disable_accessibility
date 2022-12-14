# 屏蔽网站的无障碍设计
非常开心看到很多网站都开启了无障碍模式，这是一个很大的进步！但是目前很多网站的无障碍模式都无法永久关闭，且其快捷键容易与其他应用或者系统冲突，比如`alt+number`在Linux下的Chrome中是切换标签页，而它会自动触发无障碍模式。这对于一些不需要无障碍模式的用户来说是很不方便的。本项目就是为了解决这个问题而诞生的。

将本项目中的`disable_accessibility.text`文件添加到你的广告屏蔽插件中，即可屏蔽网站的无障碍模式。比如在uBlock Origin中，可以在规则列表中添加如下url
```
https://raw.githubusercontent.com/findhao/disable_accessibility/main/disable_accessibility.txt
```

## 屏蔽的网站
- 百度
- 淘宝
- 新浪微博
- 知乎

## 贡献
欢迎大家贡献屏蔽无障碍模式的网站，只需要在`disable_accessibility.txt`中添加一行即可，形如：
```
a.sinaimg.cn/mintra/pic/*/wza/_aria.js
```
### 如何找到应该屏蔽的文件
Chrome打开网站，按下`F12`，找到`Network(网络)`标签页。回到网页，按下`Ctrl+~`触发网站的无障碍模式，观察`Network(网络)`标签页中底部因为按键触发而加载的文件，找到js文件，点击查看其请求地址。提交issue或者PR到本项目。
