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


