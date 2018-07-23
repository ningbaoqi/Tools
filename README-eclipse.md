### Eclipse快捷键

|功能|快捷键|
|------|------|
|选择重写的父类方法|Alt+Shift+s|
|提示补全代码|Alt+/|
|搜索当前所选内容下一次出现的地方|Ctrl+K|
|搜索当前所选内容上一次出现的位置|Ctrl+Shift+K|
|搜索编辑器中的内容片段，并根据需要替换新的内容|Ctrl+F|
|打开所选元素的属性对话框|Alt+Enter|
|使用代码模版包围所选语句|Alt+Shift+Z|
|直接插入局部变量、方法或常量|Alt+Shift+I|
|创建为当前所选表达式指定的新变量，并将选择替换为对新变量的引用|Alt+Shift+L|
|创建一个包含当前所选语句或表达式的新方法，并相关的引用|Alt+Shift+M|
|移动所选择的java元素|Alt+Shift+V|
|重命名所选择的java元素|Alt+Shift+ R|
|导入当前类所使用的类包|Ctrl+Shift+O|
|使用代码格式化程序来格式化当前java代码|Ctrl+Shift+F|
|更正当前选择的代码行的缩进|Ctrl+i|
|从当前选择的多行代码中除去块注释|Ctrl+Shift+`\`|
|在当前选择的多行代码周围添加多行注释|Ctrl+Shift+`/`|
|如果光标位于问题代码附近，则打开一个解决方案对话框|Ctrl+1|
|保存当前编辑器的内容|Ctrl+S|
|关闭所有编辑器|Ctrl+Shift+W|
|关闭当前编辑器|Ctrl+W|
|查看某对象所对应类的定义文件|Ctrl+Shift+T|
|显示所在文件中的数据类型和函数列表|Ctrl+O|
|跳转到指定文件名的文件|Ctrl+Shift+R|
|查找所选元素的对应调用位置|Ctrl+Shift+G|
|快速转到类的定义位置|F3|
|查看某个类的数据结构和函数|Ctrl+F3|
|跳转到指定的行数|Ctrl+L|
|为项目中存在但是不能解析的类型添加import导入|Ctrl+Shift+M|
|显示工作空间可用的任何类型名|Ctrl+Shift+H|
|显示数据类型和函数的定义位置（有分层结构）|Ctrl+T|
|在WEB浏览器中打开这个库条目的完整Javadoc HTML文档（把光标定位在编辑器中的一个类名或方法名上，必须配置存放HTML文件的URL或目录）|Shift+F2|
|进行重命名操作|Alt+Shift+R|
|添加代码javadoc注释|Alt+Shift+J|
|查看Eclipse支持的快捷方式|Ctrl+Shift+L|
|在Eclipse中添加注释或取消注释|Ctrl+'/'或Ctrl+7|
|在Eclipse中自动快捷的补全之前出现的代码|Alt+Ctrl+'/'|

### 在IDE中导入Android源代码
+ 在导入代码之前一定要将`project/build automatically`解勾选；`window/preferences/java/code Style/formatter/import/MT6757/development/ide/eclipse/android-formatting.xml`为了保证代码格式；`window/preferences/java/code Style/organize imports/import/MT6757/development/ide/eclipse/android.importorder`为了加快导入速度；需要将`development/ide/eclipse/.classpath`文件复制到源代码的根目录下，根据需要修改`.classpath`文件之后，进入eclipse下的菜单，选择`file->mew->java project`然后进行导入，在导入源代码时必须在编译完整的android源代码以后执行；
### Eclipse其他技巧
#### 一、程序调试
+ 使用eclipse内置的调试器，该调试器可以进行设置程序的断点，实现程序单步执行，在调试过程中查看变量和表达式的值等调试操作，这样可以避免在程序中编写大量的输出语句；使用eclipse的java调试器需要设置程序断点，然后使用单步调试分别执行程序代码的每一行；java调试器每次遇到断点时都会将当前线程挂起，即暂停当前程序的运行；可以在java编辑器中显示代码行号的位置双击添加或删除当前行的断点，或者在当前行号的位置单机鼠标右键，在弹出的快捷菜单中选择切换断点命令来实现断点的添加与删除；使用爬虫的图标实现debug，单步跳过：即运行单独的一行程序代码，但是不进入调用方法的内部，然后调到下一个可执行点并暂停线程；单步跳入：执行该操作将跳入调用方法或对象的内部单步执行程序并暂挂线程；
