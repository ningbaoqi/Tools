### 类图
#### 一、泛化Generalization
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-3.jpg)
+ 带空心箭头的实线表示；泛化表示一个更泛化的元素和一个更具体的元素之间的关系。泛化是用于对继承建模的UML元素，在JAVA中，用`extends`关键字来直接表示这种关系；
#### 二、实现Realization
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-4.jpg)
+ 空心箭头和虚线表示；实现是一种类和接口的关系，在JAVA中可以使用`implements`关键字来表示；
#### 三、聚合Aggregation
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-5.jpg)
+ 带空心菱形箭头表示；聚合关系是关联关系的一种，是强的关联关系，聚合是整体和部分之间的关系，例如汽车由引擎、轮胎以及其他零件组成，关联关系所涉及的两个类处于同一个层次，而聚合关系中，两个类处于不同的层次上，一个代表整体，一个代表部分，从语法上看不出来，必须看类之间的逻辑关系；
#### 四、关联Association
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-6.jpg)
+ 实线箭头表示；关联关系是类与类之间的联结，它使一个类知道另一个类的属性和方法，关联可以是双向的也可以是单向的。双向的关联可以有两个箭头或者没有箭头，单向的关联有箭头；
#### 五、组合Composition
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-7.jpg)
+ 带实心菱形箭头的实线表示；组合关系是关联关系的一种，是比聚合关系还要强的关系，它要求普通的聚合关系中代表整体的对象负责代表部分的对象的生命周期；
#### 六、依赖Dependency
![image](https://github.com/ningbaoqi/Tools/blob/master/gif/pic-8.jpg)
+ 虚线箭头表示；依赖总是单向的（一般来说，不应该存在双向的依赖），在JAVA中体现局部变量、方法的参数或者静态方法的调用；
