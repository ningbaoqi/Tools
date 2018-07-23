### AndroidStudio调试技巧
#### 一、条件断点

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-41.jpg)

+ 调试中非常有用的方式，可以自己直接赋值，减小调试时间，通过右键断点（也可以在Debug视图上的BreakPoint列表上）对一个断点加入条件，即填写Condition中的条件，只有当满足条件时，才会进入断点中；
#### 二、分析传入/传出数据流

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-42.jpg)

+ Analyze->Analyze Data Flow to Here这个操作将会根据当前选中的变量、参数或字段，分析出其传递到此处的路径，如果你想知道某个参数是怎么传递到一段陌生的代码时，这是非常好用的操作，传出数据流(Analyze data Flow from Here)则会分析当前选中的变量往下传递的路径，直到结束；
#### 三、日志断点（Logging BreadPoint）

+ 一种不是暂停的断点，只是打印日志，当想打印一些日志信息，但是不想添加log代码后重新部署时，则可以在断点上单击鼠标右键，取消选中Suspend，然后勾选Log evaluated Expression，并在输入框中输入要打印的日志信息；

#### 四、改变变量值

+ 在调试过程中，修改变量值可以快速调试各个Case，提高异常处理的调试效率，在调试时进入断点后，如果需要修改变量的值，右键单击变量名，在弹出的菜单中选择Set Value或者使用F2，就可以修改成需要的值，并且该值只对当次有效；
