
# ADB Keys

通过向MoTeL提供您的公共**Public ADB Key***，您可以随时使用任何设备`adb connect`，甚至无需打开MoTeL。

这对于自动化任务非常有用（例如在多个Android设备上运行功能测试）。

This is very useful for **automation tasks** (like running *functional tests over multiple Android devices*).

## 在开始之前

为了能够在本地使用该设备，您需要安装[Android SDK Tools](https://developer.android.com/sdk/index.html)。

## 第1步: 检查您的ADB密钥

```shell
ls ~/.android/adbkey.pub
```

应列出您的 **Public ADB Key**.

**注意:** 如果您从未 `adb` 在计算机上运行过, 则可能没有 `.android` 目录。它将在您运行任何ADB命令时创建 `adb devices`.

## 第2步：将ADB密钥复制到剪贴板

运行此命令将密钥复制到剪贴板：

```shell
pbcopy < ~/.android/adbkey.pub
```

它应该将文件的内容复制 `adbkey.pub` 到剪贴板。

**注意:** 您也可以使用文本编辑器打开 `~/.android/adbkey.pub` 文件并复制文件内容。


## 第3步：将您的ADB密钥添加到MoTeL

现在密钥在剪贴板中，将其添加到MoTeL中：

1. 转到 **Settings**.
2. 单击 **Keys** 选项卡。
3. 在 **ADB Keys**中, 按 `+ (Add)` 按钮.
4. 在 **Key** 中, 粘贴密钥并按 **Enter**.

现在，您应该能够在MoTeL中更自由地使用任何设备。
