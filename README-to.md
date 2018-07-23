### 从Eclipse ADT项目迁移到AndroidStudio
#### 一、从Eclipse ADT项目迁移到AndroidStudio的两种方法

|从Eclipse ADT项目迁移到AndroidStudio的两种方法|
|------|
|直接把Eclipse项目导入AndroidStudio中|
|从Eclipse导出Gradle项目，然后在AndroidStudio中可以直接打开导出的项目|

#### 二、Eclipse与AndroidStudio项目结构对应的关系

|Eclipse ADT|AndroidStudio|
|------|------|
|Workspace|Project|
|Project|Module|
|Project-specific JRE|Module JDK|
|Classpath variable|Path variable|
|Project dependency|Module dependency|
|Library Module|Library|
|AndroidManifest.xml|app/src/main/AndroidManifest.xml|
|assets/|app/src/main/assets|
|res/|app/src/main/res|
|src/|app/src/main/java/|
|tests/src/|app/src/androidTest/java|

#### 三、Eclipse与AndroidStudio不同的项目构建工具

+  AndroidStudio使用了Gradle项目构建工具，而Eclipse使用Ant构建项目，如果不习惯这种结构，可以通过Gradle设置与Eclipse相同的目录结构；Gradle是一种依赖管理工具，基于Groovy语言，抛弃了基于XML的各种繁琐配置，取而代之的是一种基于Groovy的内部领域特定语言（DSL），掌握Gradle脚本的编辑和打包是应用开发非常必要的；

#### 四AndroidStudio快速导入Eclipse项目的方法

+ 该方法可以将Eclipse和Ant构建脚本快速转换到AndroidStudio上；

#### 导入步骤

#### 一、在AndroidStudio菜单栏选择`File->New->Import Project`，如果是首次使用，在欢迎页面可直接选择`Import Project`

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-53.jpg)

#### 二、选择需要导入的Eclipse工程目录，AndroidManifest.xml必须在根目录下

#### 三、在导入过程中会提示是否重新配置Eclipse中的第三方库和项目依赖关系

+ 如果勾选，就会重新生成新的第三方管理库和依赖关系，依赖关系和第三方库也可以在build.gradle文件上修改；如图所示：

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-54.jpg)

+ 有三个选项可以选择，前两个选项是jar包的引用规则，建议勾选，这样就不用管理这些jar包了，第三项是指是否需要把Module名创建为camelCase风格（首字母小写的命名规则）；

#### 四Finish按钮，完成后会生成一个import-summary.txt文件

+ 该文件是导入过程中产生的日志，这个文件比较重要，如果项目比较大，导入过程不一定顺利，可以通过该文件来发现导入过程中出现的问题；

|import-summary.txt文件的内容|
|------|
|Ignore Files：描述在导入过程中忽略的文件，这些文件是没有拷贝过来的，如果有需要，就要手动添加过来，一般会忽略EclipseADT相关的配置文件和一些自定义的文件/文件夹|
|Replaced Jars with Dependencies和Replaced Libraries with dependencies：列出哪些替换的Jar包，在AndroidStudio中，如果在仓库中有这个库或者SDK，就会被替换|
|Moved Files：文件移动路径列表|
|Next Steps：接下来需要做些什么，如果没有问题，一般会告诉你可以编译了|
|Bugs：如果不能编译，就会列出当前项目存在的问题|

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-55.jpg)

+ 这样导入的项目还是会保留Eclipse的构建方式，比如在Eclipse上使用Ant构建，迁移后还是会使用Ant构建，如果先从Eclipse导出成Gradle项目就使用Gradle构建，当然也可以手动修改构建方式；更多关于EclipseADT迁移到AndroidStudio的方法可以查看：http://developer.android.com/intl/zh-cn/sdk/installing/migrate.html#prerequisites ;
