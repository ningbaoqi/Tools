#### 一、查看adb版本：adb version
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-60.jpg)
#### 二、查看手机分辨率：adb shell wm size
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-61.jpg)
#### 三、重新启动adbd守护进程并带有root权限；原型：adb root
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-62.jpg)
#### 四、重新启动adbd守护进程并监听USB；原型：adb usb
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-63.jpg)
#### 五、查看手机属性：adb shell getprop
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-64.jpg)
#### 六、安装apk
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-65.jpg)
+ 将指定的`apk`文件安装到设备上：原型：`adb install [-l] [-r] [-s] [--algo <algorithm name> --key <hex-encoded key> --iv <hex-encoded iv>] <file>`；`L`表示正向锁定应用程序；`r`表示重新安装应用程序，保存数据；`S`表示安装SD卡而不是内部存储；`--algo`， `--key`， 和 `--iv`意味着文件已加密；如：`adb install apk路径`；
#### 七、以交互式方式运行远程shell；即进入设备或者虚拟机的shell环境：adb shell
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-66.jpg)
#### 八、查看连接设备和模拟器
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-67.jpg)
+ 列出所有连接的设备与模拟器`-l`选项将会列出设备限定符；原型：`devices [-l]`；如：`adb devices -l`；
#### 九、将本机电脑上的文件或文件夹复制到设备；原型：`adb push <local> <remote>`；如`adb push ./a /sdcard/`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-68.jpg)
#### 十、将设备上的文件或文件夹复制到本地电脑上；原型：`adb pull <remote> [<local>]`，如果没有指定本地目录，将放在默认目录下；如：`adb pull /sdcard/aaaa`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-69.jpg)
#### 十一、查看当前手机处于Resume状态的activity；如：`dumpsys activity|grep Resume`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-70.jpg)
#### 十二、打印设备序列号；原型：`adb get-serialno`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-71.jpg)
#### 十三、查看设备日志：原型：`adb logcat [ <filter-spec> ]`；如：`adb logcat -s 标签名`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-72.jpg)

|adb查看log方法|说明|
|------|------|
|adb logcat > log.txt| 将log重定向到文件中|
|adb logcat -vtime|按时间顺序打印所有log|
|adb logcat -vtime \|grep -i com.*setting |按时间顺序打印log并且不分大小写进行过滤|
|adb logcat -vtime \|grep -iE "com.*setting\|key.*value"|按时间顺序打印log并且不分大小写进行过滤|
|adb logcat -vtime \|grep -iv SecuritySetting\|grep -iE "com.*setting\|key.*value"|按时间顺序打印log并且不分大小写进行过滤|

#### 十四、显示帮助消息；原型：`adb help`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-73.jpg)
#### 十五、阻塞直到设备联机；原型：`adb wait-for-device`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-74.jpg)
#### 十六、如果服务运行，杀死服务；原型：`adb kill-server`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-75.jpg)
#### 十七、确保有服务器正在运行；原型：`adb start-server`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-76.jpg)
#### 十八、打印设备路径；原型：`adb get-devpath`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-77.jpg)
#### 十九、为指定设备连续打印设备状态；原型：`adb status-window`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-78.jpg)
#### 二十、返回所有设备的消息，会包含bug报告；原型：`adb bugreport`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-79.jpg)

#### 二十一、打印`offline | bootloader | device`状态；原型；`adb get-state`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-80.jpg)
#### 二十二、列出设备上的进程ID；原型：`adb jdwp`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-81.jpg)
#### 二十三、重新挂载设备上的读写分区；原型：`adb remount`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-82.jpg)
#### 二十四、查看手机中的所有包名：`pm list packages`
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-83.jpg)
#### 二十五、卸载apk
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-84.jpg)
 + 将设备上的app包删除；原型：`adb uninstall [-k] <package>`；`-k`意味着保持数据和缓冲区目录；不加该选项将直接卸载应用；如：`adb uninstall 包名`；
#### 二十六、运行远程shell命令
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-85.jpg)
+ 运行远程shell命令；原型：`adb shell <command>`；如：一、可以查看开机动画：`adb shell setprop ctl.start bootanim`；二、查看系统环境变量：`adb shell export -p`；三、使手机关机：`adb shell reboot -p`；
#### 二十七、通过`TCP/IP`连接到设备
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-86.jpg)
+ 如果没有指定端口号，默认情况下使用端口`5555`；原型：`connect <host>[:<port>]`；如：`adb connect 192.168.1.220`；
####二十八、通过`TCP/IP`设备断开连接
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-87.jpg)
+ 如果没有指定端口号，默认情况下使用端口5555；使用此命令没有附加参数；将从所有连接的TCP/IP设备断开连接；原型：`disconnect [<host>[:<port>]]`；

#### 二十九、恢复设备内容从备份存档；原型：`adb restore <file>`

#### 三十、套接字连接；原型：`adb forward <local> <remote>`

#### 三十一、重启设备并进入到`bootloader`模式；原型为：`adb reboot-bootloader`

#### 三十二、重启adbd守护进程通过TCP监听，并且监听指定端口；原型：`adb tcpip <port>`

#### 三十三、将设备数据的存档写入到文件；原型：`adb backup [-f <file>] [-apk|-noapk] [-shared|-noshared] [-all] [-system|-nosystem] [<packages...>]`；如果没有`-f`选项，数据将会被写入到当前目录下的`backup.ab`文件中；`[-apk|-noapk]`能否保存apk文件在存档中，默认情况下是不能的；`[-shared|-noshared]`能否保存设备的分享存储或SD卡内容，默认情况下不分享；` [-all] `意味着备份所有安装的应用；`[-system|-nosystem]`切换是否`-all`自动包含系统应用，默认情况下包含系统应用；` [<packages...>]`需要被备份的应用列表；如果`-all`或者`-shared`有shared标签，包列表是可选的；`-nosystem`选项将会被覆盖掉



