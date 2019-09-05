# 远程shell使用

### 文件列表
```
ls -la
```
启动后默认是根目录。


### 包名称列表

```
pm list packages
```
列出安装的应用程序的包装名称。

当只记住了一部分包装名时`pm list packages [包名]`一样可以过滤。


### 包删除

```
pm uninstall [包名]
```

更多相关 [ADB pm | Android Developers](http://developer.android.com/tools/help/adb.html#pm) 参考。


### 文件内容

```
cat /sdcard/hoge.txt
```
在确认有读取权限的文件内容时使用。


### 启动应用程序

**Activity启动 (ACTION_VIEW + URL)**

```
am start -a android.intent.action.VIEW -d http://google.com
```

**Activity启动(指定Activity类名)**

```
am start -n com.hoge.app/.FugaActivity
```

**启动服务**

```
am startservice ... # Intent的指定方法和Activity相同
```

**发送广播**

```
am broadcast ... # Intent的指定方法和Activity相同
```


### 发送键盘事件

```
input keyevent 3 # HOME键
```
用数字指定键码。

更多相关[KeyEvent | Android Developers](http://developer.android.com/reference/android/view/KeyEvent.html)参照。

### 操作录像

最多可以录制3分钟操作信息

```
pre screenrecord [options] <filename>
```

[options]は[ADB screenrecord | Android Developers](http://developer.android.com/tools/help/adb.html#screenrecord)参照。

`filename`指定终端侧的路径。

```
screenrecord /sdcard/movie/sample.mp4
```

### 内存使用状况

```
dumpsys procstats [包名]
```

例： `dumpsys procstats com.android.chrome`

---


### 其他命令
执行以下命令以获得可执行的shell命令列表：

```
ls /system/bin
```


更多相关[这里](https://github.com/jackpal/Android-Terminal-Emulator/wiki/Android-Shell-Command-Reference)。
