# Android Killer

> [!CAUTION] Windows Defender 报毒问题
> 
>  介是一个已知的由 Android Killer 自己 & Windows Defender 的检测策略导致的问题。
>
> Android Killer 是由 [legend_brother](https://www.52pojie.cn/home.php?mod=space&uid=366193) 开发并发布在 [52pojie](https://www.52pojie.cn/thread-319641-1-1.html) 和 [pd521](https://www.pd521.com/thread-136-1-1.html) 于 2014 ~ 2015，年久失修，也许在开发之初留下了一些现在可能会被检测为病毒的特性。
> 
> Windows Defender 的检测规则对软件逆向工具有些太严格了。推荐使用 [Kaspersky](https://www.kaspersky.com/) 或 [火绒](https://www.huorong.cn/) 代替 Windows Defender（如果你有经常使用逆向、注册机等工具但又想保持一定的系统安全性的话）
> 
> 这是 [VirusTotal](https://www.virustotal.com/gui/file/93816beef6269be75cc78f8c056cc4345e8e1263df2b34d65539d1650eb1e6cf) 的检测结果，仅有两家供应商显示 Android Killer 是“可能涉嫌恶意”和“潜在的危险”。
> 
> 这是 [微步云沙箱](https://s.threatbook.com/report/file/93816beef6269be75cc78f8c056cc4345e8e1263df2b34d65539d1650eb1e6cf) 的检测结果，表面 Android Killer 不是病毒。
> 
> 如果你担心使用 Android Killer 会给你带来危害，你可以前往 [52pojie](https://www.52pojie.cn/forum.php) 社区（Android Killer 诞生的地方之一）寻找其它软件逆向工具。

> 注意：出于兼容性原因，本项目使用 GB2312 字符集。

整合并更新最最最最经典的 Android 反编译工具 —— Android Killer，让它再战 20 年！

思路和方法来自大佬[昨夜星辰 2012](https://www.52pojie.cn/home.php?mod=space&uid=571540&do=profile&from=space) 的 [AndroidKiller 安装、设置及使用教程](https://www.52pojie.cn/thread-726176-1-1.html)。

工具毕竟很老了，无论是界面还是功能上都不尽人意，小的在此还是推荐客官尝试 JEB Decompiler 3 等仍在维护的 Android 反编译工具。

## 使用

点击[此处](../../archive/refs/heads/main.zip)下载最新压缩包，解压后打开目录，双击启动 AndroidKiller.exe 即可。

Android Killer 的详细使用教程请[参考此文](https://blog.csdn.net/yiran1919/article/details/132760445)或自行搜索。

**注意事项：使用本工具前，您需要在电脑配置好 Java 运行环境。**

## 更新内容

- `bin/`
  - 更新 adb 和 busybox，版本忘了（能用就行，不能再说 ?）
  - 更新 apktool.jar 至 v2.11.1
  - 更新 dex2jar 至 v2.4
  - 弃用 Android Killer 内置的 jd-gui，使用自己编写的中间程序 [android-killer-jadx-gui-support](../../../android-killer-jadx-gui-support) 将操作转发至 jadx-gui
- `tools/`
  - 添加 [ApkScan PKID](http://www.legendsec.org/1888.html) 查壳工具（工具年代久远，效果无法保证，建议寻找替代方案）
  - 添加 [InjectLog](https://www.52pojie.cn/thread-743758-1-1.html) 日志工具，又见 [Android 应用逆向——分析反编译代码之大神器](https://blog.csdn.net/charlessimonyi/article/details/52027563)
  - 添加 jadx-gui 无捆绑 jre 版本，更新至 v1.4.7（GitHub 上传单文件体积限制 100MB，v1.5.0+ 版本超限，如您有更新需要，请尝试[自行更新](#jadx-gui-更新方法)）

## 自行更新

### apktool 更新方法

1. 从 [apktool 下载页面](https://github.com/iBotPeaches/Apktool/releases) 下载最新版的 `apktool_x.x.x.jar`
2. 放置在 `bin/apktool/apktool/` 目录下，打开 **Android Killer** 首页的 **Android** 菜单并打开 **APKTOOL 管理器**，添加下载的版本并设置为默认

   ![展示](docs/images/image1.png)
   ![展示](docs/images/image2.png)

### dex2jar 更新方法

1. 从 [dex2jar 下载页面](https://github.com/pxb1988/dex2jar/releases) 下载最新版的 `dex-tools-xxx.zip`（旧版名为 `dex2jar-xxx.zip`）
2. 清空 `bin/dex2jar/` 目录下文件，将下载得到的压缩包内容全部解压缩至该目录

### jadx-gui 更新方法

1. 从 [jadx 下载界面](https://github.com/skylot/jadx/releases) 下载最新版的 `jadx-gui-x.x.x-win.zip`（旧版为 `jadx-gui-x.x.x-no-jre.exe`）
2. 将压缩包内容解压至 `tools/JadxGui/` 目录下，重命名 `jadx-gui-x.x.x.exe` 为 `jadx-gui.exe`，覆盖旧版（旧版直接重命名可执行程序，后覆盖即可）

## 注意事项 & 一些问题

- 编译应用时请勾选 AndroidKiller 签名，否则编译出的 apk 文件概率不能正常使用
- 编译后安装报错 "Failure [INSTALL_FAILED_INVALID_APK: Failed to extract native libraries, res=-2]"？ 请将 `AndroidManifest.xml` 文件中的 `extractNativeLibs=false` 修改为 `extractNativeLibs=true`，再次尝试
