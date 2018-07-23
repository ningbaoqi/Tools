### SmallQuestion
#### 一、找不到R文件
+ 可能是因为`draw-9-patch`图片不规范造成；
#### 二、在AndroidStudio中导入Jar包

+ 在`Module`的根目录下创建`libs`文件夹，将下载的`jar包`复制到`libs`目录下，然后右键单击`jar包`选择`add as library`之后就是自动进行的了，在添加完成后会在配置文件中出现`compile files("......")`的字样；

#### 三、自动导包

+ 进入    `Setting->Editor->General->Auto Import `   设置页面，选中    `Show import popup 、Show import popup、Optimized imports ob the fly、Add unambiguous imports on the fly`    ，就可以自动导包；

#### 四、显示插件加载失败问题

+ 需要点击`file->settings->plugins`，有错误的时候将会显示为红色；勾选需要的插件，然后点击`Apply->ok`会提示重启，然后重启，就会恢复正常；
