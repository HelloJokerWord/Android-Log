# Android日志捕获 

## 1、http请求日志  2、socket日志 3、奔溃日志 4、无线调试app

### 1、环境准备
- 1、win7/win10  (系统环境)
- 2、jdk 1.8 （java环境）
- 3、platform-tools windows (android环境)
- 4、logview-0.21 (抓取日志工具)

### 2、JDK安装与环境变量配置
[Java环境安装与配置教程](https://jingyan.baidu.com/article/6dad5075d1dc40a123e36ea3.html "Java环境安装与配置教程")

[JDK官方下载地址](https://www.oracle.com/java/technologies/downloads/#jdk17-windows "JDK官方下载地址")


### 3、Android ADB环境配置
[ADB环境变量配置教程](https://jingyan.baidu.com/article/2f9b480de62ab741cb6cc225.html "ADB环境变量配置教程")

[ADB官方下载地址](https://developer.android.com/studio/releases/platform-tools "ADB官方下载地址")

### 4、logView工具
[logView官方下载地址](https://bitbucket.org/mlopatkin/android-log-viewer/downloads/ "logView官方下载地址")

### 5、ADB命令简单介绍
```shell
//查看当前连接设备
adb devices
```
1、检查当前已连接设备，若未查询到，尝试有USB线链接 以及打开手机ADB调试

![](https://github.com/HelloJokerWord/Android-Log/blob/main/check_devices.png)


2、开始连接手机
```shell
// 手机的IP地址可在设置 -> 关于手机 -> 状态信息 中找到IP地址
adb connect 192.168.22.46:5555

//如果链接拒绝则获取权限打开端口链接
adb tcpip 5555

//如果有多台设备，输入以下命令
adb -s xxx tcpip 5555 //xxx是指定的设备id
```
![](https://github.com/HelloJokerWord/Android-Log/blob/main/support_devices.png)


3、重复执行 adb connect 手机IP地址:5555  即可链接成功 ， 以及打开APP showLog

![](https://github.com/HelloJokerWord/Android-Log/blob/main/connect_devices.png)

![](https://github.com/HelloJokerWord/Android-Log/blob/main/show_logger.png)

4、断开链接，链接其他设备
```shell
 //先断开
adb disconnect 当前手机IP地址

//再重连
adb connect 新的手机IP地址:5555

```

### 5、AndLogView简单介绍
- 1、打开安装好的 andlogview-0.21-SNAPSHOT\lib 目录下 andlogview-0.21-SNAPSHOT-all.jar
- 2、工具菜单介绍

![](https://github.com/HelloJokerWord/Android-Log/blob/main/log_menu_adb.png)

![](https://github.com/HelloJokerWord/Android-Log/blob/main/log_menu_select_adb.png)

![](https://github.com/HelloJokerWord/Android-Log/blob/main/log_menu_select_device.png)

![](https://github.com/HelloJokerWord/Android-Log/blob/main/log_menu_filter_config.png)

![](https://github.com/HelloJokerWord/Android-Log/blob/main/log_menu_select_process.png)

![](https://github.com/HelloJokerWord/Android-Log/blob/main/log_http_catch.png)

![](https://github.com/HelloJokerWord/Android-Log/blob/main/log_socket_catch.png)


