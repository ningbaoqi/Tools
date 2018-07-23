### 用例图
+ 用例图主要描述用户、需求、系统功能单元之间的关系。它展示了一个外部用户能够观察到的系统功能模型图，从而帮助开发团队以一种可视化的方式理解系统的功能需求；

#### 一、参与者Actor
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-20.jpg)
+ 表示与您的应用程序或系统进行交互的用户、组织或外部系统，用一个小人表示；
#### 二、子系统SubSystem
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-21.jpg)
+ 用来展示系统的一部分功能，这部分功能联系紧密；
#### 三、关系
+ 关联Association：表示参与者与用例之间的通信，任何一方都可以发送或者接收消息；
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-22.jpg)
+ 泛化Inheritance：继承关系，子用例和父用例相似，但是表现出更特别的行为。子用例将继承父用例的所有结构、行为和关系。子用例可以使用父用例的一段行为，也可以重载它，父用例通常是抽象的；
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-23.jpg)
+ 包含Include：包含关系用来把一个较复杂用例所表示的功能分解成较小的步骤；
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-24.jpg)
+ 依赖Dependency：表示原用例依赖于目标用例；

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-25.jpg)

#### 四、项目Artifact

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-26.jpg)

+ 可以在用例图中链接一个普通文档；
#### 五、注释
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-27.jpg)
#### 六、用例UseCase
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-28.jpg)
+ 用例就是外部可见的系统功能，对系统提供的服务进行描述；
