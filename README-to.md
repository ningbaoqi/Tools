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
