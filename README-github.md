### 使用AndroidStudio把本地代码托管到Github上的流程
#### 一、在本地安装Git
+ 可以从官网上下载安装包；https://git-scm.com/downloads；
#### 二、配置File->Settings->Version Control
+ 分别配置Git目录（安装路径下Bin目录的Git.exe文件）和GitHub帐号；

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-48.jpg)

+ 配置完成之后可以单击test按钮，配置没有问题就会弹出测试成功提示框；
#### 三、初始化Git项目
+ 选择菜单栏->CVS->Enable Version Control Integration...，在弹出的配置对话框中选择Git，完成后工具栏会新增如下快捷工具；

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-49.jpg)

#### 四、过滤掉不需要上传的文件或者目录
+ 可以在File->Settings->VersionControl->Ignore Files中选择不需要同步的文件或文件夹；如下图所示：

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-50.jpg)

+ 也可以修改项目目录下的.gitIgnore文件来实现，建议使用前者，因为根据作者实际的使用经验，修改.gitIgnore文件有时会失败，而且管理也没有前者方便；可以通过选择VCS->Git->Compare With Branch指定分支和本地代码作比较，提交前可以双击需要提交的文件来对比改动代码行；

#### 五、同步代码到Github
+ 选择VCS->Import into Version Control->Share Project on Github；第一次使用需要登陆Github，输入用户名、按钮、和URL；

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-51.jpg)

+ 单击Share按钮，弹出提交文件列表（可以看到前面过滤的文件不在列表中），同步完成后就可以在Github上看到我们同步的项目了；

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-52.jpg)

+ 后面需要提交代码，首先提交，然后选择VCS->Git->Push即可同步代码到Github上；
