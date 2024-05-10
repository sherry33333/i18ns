---
sidebar_position: 9
---

# 常见问题

## 如何支持 [ollama](https://github.com/ollama/ollama)
Ollama 默认允许来自 127.0.0.1 和 0.0.0.0 的跨域请求。

所以配置该地址到插件会导致403 错误

- 解决方案

OLLAMA_ORIGINS="*" ollama serve 来开启
- 更多参考

[ollama / Setting OLLAMA_ORIGINS #2335](https://github.com/ollama/ollama/issues/2335)

## 如何关闭自动翻译

- 在 Popup 面板或者设置页面取消。

- 或者通过设置页面修改：

## 暂无权限翻译当前页面

- 浏览器默认页(地址栏无地址)
- 第三方插件页面
- 谷歌插件禁止了谷歌商店页面

## 如何不显示原文？

点击沉浸式翻译图标，打开扩展面板，点击【更多】，【切换到仅译文模式】

## 页面出现感叹号

页面出现感叹号，说明翻译服务遇到问题，返回了错误，可以将鼠标移动到感叹号上查看具体错误。

### 429 错误

这是最常见的错误之一，429 表示请求的频率过快。网页翻译中有非常多的段落需要翻译，尽管我们已经做了极大的优化，包括合并段落，频率控制等等，但是有的时候依然有一些翻译服务不堪重负，返回 429 频率限制的错误，这种时候一般可以暂时切换到其他翻译服务，或者等一会儿再试。

如果你是 Google 服务遇到的 429，一般来说是谷歌针对你的节点做了限流，建议切换节点。

## 翻译本地文件

如果你需要翻译本地的 HTML 文件，txt 文件或者 PDF 文件，你可以点击沉浸式翻译扩展图标，然后点击【更多】，点击【翻译 PDF 文件】或【翻译 HTML/txt】文件，进行本地文件的翻译。

如果你使用的是类 Chrome 浏览器，如（Chrome，Arc，Edge 浏览器），还有另一种办法，就是在浏览器中打开扩展管理页面`chrome://extensions`,找到【沉浸式翻译】插件，【允许该扩展访问本地文件】，之后直接在浏览器中打开本地的 HTML 或本地的 PDF 文件，就可以直接右键【翻译】了。

![](https://s.immersivetranslate.com/assets/allow-local-file-1.png)

![](https://s.immersivetranslate.com/assets/allow-pdf-2.png)

## 如何更新扩展？

一般来说，在浏览器商店安装的扩展，浏览器都会自动进行更新，一般情况会在扩展更新之后的一天内进行自动更新，如果你想立刻更新到最新版本的话，可以在浏览器的【扩展管理】页面，打开【开发者模式】，然后点击最上面的【更新】，即可立即更新到商店的最新版本。

![](/assets/docs/doc-assets/update-extension.png)

## Youtube 字幕设置样式

可以直接点击Youtube 自带的字幕设置，[Options], 然后就可以调整大小，颜色等。

![](https://s.immersivetranslate.com/assets/youtube-subtitle-options.jpeg)

## 沉浸式翻译油猴脚本支持的浏览器

桌面端 Chrome, Firefox 推荐使用的油猴扩展：

- [Tamper Monkey](https://www.tampermonkey.net/)

Safari 推荐使用的油猴扩展：

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

> 如果在 Safari 里使用 [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171)的话，请直接在 Stay 自带的商店里搜索沉浸式翻译优化脚本下载（针对 Stay 做了特殊优化）

安卓推荐使用的油猴扩展：

1. 你可以使用 [Firefox 最新版本](https://www.firefox.com.cn/download/#product-android-release)安装 [Tamper Monkey](https://www.tampermonkey.net/) 扩展。

2. 你也可以直接使用 [X 浏览器](https://www.xbext.com/?ref=immersive-translate)，安装后，直接打开[沉浸式翻译油猴脚本地址](https://download.immersivetranslate.com/immersive-translate.user.js) 即可安装

已知不支持的油猴扩展：

- 安卓 Via 浏览器
- iOS Alook 浏览器

（由于这类浏览器并没有实现所需的油猴 API）

## 谷歌翻译接口被墙问题

请将`translate.googleapis.com` 域名加入到代理规则中

## 如何更新最新规则

扩展本身会在使用的时候定时同步官方最新对网站适配的规则，你也可以手动同步最新的规则，点击浏览器的沉浸式翻译扩展图标，打开弹窗后扩展会会自动检测最新适配规则并同步，油猴脚本同理。

## 网页翻译有问题，如何保存网页反馈？

需要在网页中右键点击“存储为” 或者 ctrl+s 快捷键，保存选项选择单个文件，最后文件格式为.mht/.mhtml。 然后将文件发送至 support@immersivetranslate.com

![save mht](/assets/save_mht.png)

## 彩云翻译报错

点开？号的报错信息显示"Unsupported trans_type"。可以手段选择自动检测语言为指定语言

## 微信读书无法翻译

因为微信读书针对内容做了特殊处理，防止通过第三方手段获取内容，所以无法翻译。

## 网页部分内容未翻译
一般是网站管理者通过 translate="no" 或者 notranslate class 来约定翻译插件不然以这块区域

- 启用鼠标悬停功能
- 通过鼠标悬停来强制翻译该区域段落内容

## 触发翻译不生效

其他网站能翻译，就某个网站不能翻译

- 如果这个网站访问人比较少
  - 建议通过鼠标悬停来翻译段落
  - 如果需要翻译整篇网站可以通过[用户规则](/docs/advanced/#用户规则合并增强)适配
- 如果这个网站有很多人用
  - 可以先通过鼠标悬停翻译使用
  - 在群里呼叫，会稍后安排适配

## 输入框增强不生效

- 浏览器主页 Google 搜索

谷歌搜索框一定是在[Google](https://www.google.com/)网址的网页，而不能在浏览器主页，地址栏空白的地方使用

## 反馈调试日志

- 开启调试日志
  打开面板 -> 设置 -> 开发者设置 -> 启用”在控制台打印调试日志“
- 打开网站的控制台
  右键打开审查 -> 右边栏目顶部切换到控制台 -> 执行操作就可以看到日志

## 如何关闭悬浮球

- 在当前页隐藏

设置为 【永不翻译该网站】 即可

- 在所有页面隐藏

打开【设置页】-【界面设置】，关闭【在页面上显示悬浮球】即可

## 在 chrome 上安装插件安装包报错

- invalid value for web_accessible_resource[0]

  需要 Chromium 版本大于 88 才能支持 manifest_version 3

## 360 浏览器如何安装

只支持 360 极速浏览器 x，记住是带 x 的。如果可以访问谷歌扩展商店，直接可以去那里装。如果访问不了就[手动安装](/docs/installation/#%E6%89%8B%E5%8A%A8%E5%AE%89%E8%A3%85-%E8%BF%BD%E8%B8%AA%E6%9C%80%E6%96%B0%E5%BC%80%E5%8F%91%E7%89%B9%E6%80%A7)

## Opera 浏览器不生效

- 在 google.com 等搜索页面不生效，插件显示`请先刷新当前页面，再开始翻译`且刷新页面仍提示该信息

需要在 Opera 插件设置中找到【沉浸式翻译】，开启【允许访问搜索页面结果】选项

![](/assets/opera-allow-search.png)

## YouTube 双语字幕繁体中文不显示

YouTube 自带机翻字幕，繁体中文会出现格式错误，导致所有字幕在开始的时候弹出一大段字幕，基于此场景建议在【设置】【视频字幕】中开启​​【使用沉浸式翻译来翻译字幕】选项。

## 鼠标悬停+快捷键翻译功能无效

要启用鼠标悬停加快捷键的翻译功能，页面必须首先获得焦点。如果您发现该功能未能触发，请尝试以下步骤：

- 在页面任意位置点击一次，以确保页面获得焦点。
- 再次尝试同时使用鼠标悬停和快捷键进行翻译。

如果翻译功能仍然不响应，请确认您的快捷键设置是否正确。


## 在 iOS 设备上无法启用扩展

如果您在 iOS 设备上无法启用扩展，请按照以下步骤操作：

1. 打开【设置】应用。
2. 滑动并点击【屏幕使用时间】。
3. 选择【内容和隐私访问限制】。
4. 点击进入【内容访问限制】。
5. 选择【网页内容】，并将其设置为【无限制】。

如果您不需要使用内容和隐私访问限制的其他功能，您也可以选择直接关闭内容和隐私访问限制：

1. 打开【设置】应用。
2. 选择【屏幕使用时间】。
3. 禁用【内容和隐私访问限制】。

## Safari 打开设置页面 一直loading

- iOS
系统设置 -> safari浏览器-> 高级 -> 网站数据 -> 编辑 找到 immersivetranslate.com 删除


## 更多问题（非常见）

<details>
<summary>油猴脚本如何清空缓存？</summary>
<p>
由于油猴脚本的API限制，沉浸式翻译油猴脚本的缓存会保存在对应网站的缓存里，所以如果要清除的话，可以在浏览器打开相应网站的开发者工具面板，然后清空该网站的缓存。
</p>
</details>

<details>
<summary>油猴脚本自定义接口地址请求失败？</summary>
<p>
油猴脚本要求脚本的所有请求都需要在脚本的开头声明权限，比如：`@connect api.google.com`，所以，如果你需要新增一个非默认的域名，请在油猴脚本开头仿照其他域名进行声明。
</p>
</details>