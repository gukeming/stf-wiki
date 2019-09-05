# 远程调试

## 在开始之前

为了能够在本地使用该设备，您需要安装[Android SDK Tools](https://developer.android.com/sdk/index.html).


## 调试

为了能够在本地计算机上调试远程设备，您需要执行以下操作：

1. 在MoTeL上，在控制设备后，转到 **Dashboard** 选项卡 -> **Remote Debug** 面板.

2. 将有一个内容类似的文本字段 `adb connect ...`。单击并复制该文本。

3. 粘贴它并运行它的命令行。

这将在本地连接设备。

您可以通过转到命令行并键入以下内容来检查它是否有效：
```bash
adb devices
```


### Android Studio

您应该能够调试设备，但是在使用调试器时IDE仍然存在一些错误。


### Eclipse

您应该能够按原样调试设备。



### Chrome

#### 在设备上

在Chrome 32及更高版本上，您无需在设备上执行任何操作。

在Chrome 32及更早版本中，您需要在Chrome设置中启用USB远程调试：

1. 打开 **Chrome**.
2. 转到 **设置** -> **开发人员工具**.
3. 启用 **USB调试。**.

#### 在桌面浏览器上

1. 打开一个新标签
2. 转到 `chrome://inspect/#devices` 地址栏。
3. 单击复选框启用 **发现USB设备** 。

它应该显示在设备的Chrome浏览器和WebViews中打开的页面列表。

现在，您可以通过单击**inspect**来调试任何页面。

更多相关 [在Chrome中Android上的远程调试](https://developer.chrome.com/devtools/docs/remote-debugging) docs.


### Opera

#### 在设备上

1. 打开 **Opera**.
2. 键入 `opera:debug` 地址栏。


#### 在您的命令行上

转到您的命令行，然后键入：

```
adb forward tcp:9222 localabstract:opera_devtools_remote
```


#### 在桌面浏览器上

您可以使用Opera，Chrome或任何其他基于Chromium的浏览器。

1. 打开一个新标签。
2. 转到 `localhost:9222` 地址栏。

它应该显示可检查选项卡的列表。

现在您可以调试任何页面。

更多相关 [在Opera中Android上的远程调试](https://dev.opera.com/articles/remotely-debugging-opera-for-android/) docs.


### Firefox

#### 在设备上

1. 打开 **Firefox**。
2. 转到 **Settings** -> **Developer tools**。
3. 开启 **Remote debugging**.

#### 在您的命令行上

转到您的命令行，然后键入：

```
adb forward tcp:6000 tcp:6000
```

如果您使用的是Firefox OS，请键入：

```
adb forward tcp:6000 localfilesystem:/data/local/debugger-socket
```


#### 在桌面浏览器上

1. 在**Web Developer** 菜单上, 选择 **Connect**.
2. 将会跳转到 `chrome://browser/content/devtools/connect.xhtml`.
3. 点击按钮 **Connect** .
4. 在设备上，它会要求您接受 **Incoming Connection**, 点击 **OK**.

这应该显示在Device的Firefox浏览器和WebViews中打开的页面列表。

更多相关[在Firefox中Android上的远程调试](https://developer.mozilla.org/docs/Tools/Remote_Debugging/Firefox_for_Android) docs.
