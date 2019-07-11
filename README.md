#Flutter学习

##Flutter环境安装
####1、下载Flutter环境（Mac环境下）
通过[Flutter官网](https://flutter.dev/docs/development/tools/sdk/releases?tab=macos#macos)，找到对应的下载包点击下载，只不过这个下载过程缓慢，可以找到下载包，然后右键获取下载地址，通过工具去下载，如`迅雷`或者是[Motrix神器](https://motrix.app/)

下载好后，需要配置环境变量，使用终端输入命令`open ~/.bash_profile`，打开后，配置如下：

```
# 此处的路径为flutter的安装路径，也就是上面下载后存放的位置，此处我放置与根目录下
export PATH="/Library/flutter/bin:${PATH}"
export FLUTTER_ROOT="/Library/flutter"

export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```
####2、App Store下载Xcode

####3、下载Android Studio
[下载地址](https://developer.android.com/studio/index.html)，并安装相应的Android-SDK，下载好后，安装Flutter插件，步骤：打开Android Studio，按`command+,`,找到`Plugins`并搜索`Flutter`，然后安装

####4、下载Visual Studio Code

[下载地址](https://code.visualstudio.com/)，下载后，同样需要安装`Flutter`插件，打开软件点击左侧`Extensions`，搜索并下载Flutter插件

####5、以上配置完成之后，执行`flutter doctor`
`flutter doctor`是检测环境是否安装成功，一般会有报错如图：![错误示例.png](https://upload-images.jianshu.io/upload_images/1840399-30efaeae1dc60b24.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

>flutter doctor 检测失败的原因会有很多，例如以下
>
>* 没有安装 Android Studio。
>* Android Studio 配置有问题。
>* Android Studio 没有安装Flutter插件。
>* 没有安装Xcode，或Xcode版本过低。
>* 没有安装CocoaPods
>* 没有安装 libimobiledevice
>* 没有安装 ideviceinstaller
>* 没有安装 ios-deploy

一步一步按照提示进行修复问题

安装或修改需要的地方，直到 `flutter doctor` 没有错误提示为止


##创建工程
####1、配置Xcode模拟器
```
#终端敲入以下命令：
open -a Simulator
```
####2、安装到iOS设备
```
brew update
brew install --HEAD libimobiledevice
brew install ideviceinstaller ios-deploy cocoapods
pod setup
```
####3、创建新工程
>* 启动 VS Code
>* 调用 View>Command Palette…
>* 输入 ‘flutter’, 然后选择 ‘Flutter: New Project’ action
>* 输入 Project 名称 (如myapp), 然后按回车键
>* 指定放置项目的位置，然后按蓝色的确定按钮
>* 等待项目创建继续，并显示main.dart文件
>* 上述命令创建一个Flutter项目，项目名为myapp，其中包含一个使用Material 组件的简单的演示应用程序。

> 在项目目录中，您的应用程序的代码位于 lib/main.dart.

####运行应用程序
>* 确保在VS Code的右下角选择了目标设备
>* 按 F5 键或调用Debug>Start Debugging
>* 等待应用程序启动
>* 如果一切正常，在应用程序建成功后，您应该在您的设备或模拟器上看到应用程序:

![效果图](https://flutterchina.club/images/flutter-starter-app-android.png)