### 序列图
+ 序列图将交互关系表示为一个二维图，纵向为时间轴，时间沿竖直向下延伸、横向轴代表了在协作中各个独立对象；
#### 一、生命线
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-10.jpg)
+ 生命线名称可以带下划线，当使用下划线时，意味着序列图中的生命线代表一个类的特定实体；
#### 二、同步消息
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-11.jpg)
+ 发送人在它继续之前，将等待同步消息响应；
#### 三、异步消息
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-12.jpg)
+ 在发送方继续之前，无需等待响应的消息；
#### 四、注释
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-13.jpg)
#### 五、约束
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-14.jpg)
+ 格式是`[Boolean Test]`；
#### 六、组合片段
+ 组合片段用来解决交互执行的条件及方式。它允许在序列图中直接表示逻辑组件，用于通过指定条件或者子进程的应用区域，为任何生命线的任何部分定义特殊条件和子进程；

![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-15.jpg)

+ 抉择Alt：抉择用来指明在两个或者更多的消息序列之间的互斥的选择，相当于if...else...；
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-16.jpg)
+ 选项Opt：包含一个可能发生或不可能发生的序列，可以在临界中指定序列发生的条件；
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-17.jpg)
+ 循环Loop：片段重复一定次数，可以在临界中指示片段重复的条件；
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-18.jpg)
+ 并行Par：并行处理，片段中的事件可以交错；中断break：如果执行此片段，则放弃序列的其余部分，可以使用临界来指示发生中断的条件；关键Critical：用在Par或Seq片段中，指示此片段中的消息不得与其他消息交错；弱顺序Seq：有两个或者更多操作数片段，涉及同一生命线的消息必须以片段的顺序发生，如果消息涉及的生命线不同，来自不同片段的消息可能会并行交错；强顺序Strict：有两个或者多个操作数片段，这些片段必须按照给定顺序发生；
