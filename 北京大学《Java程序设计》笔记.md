# 北京大学《Java程序设计》笔记

# 数组

声明：

```java
data[] name = new data[length];
```

数组是引用类型

**数组的下标的合法取值范围为0~n-1**

每个数组都有一个属性**length**指明长度

**System.arraycopy提供了元素复制功能**

```java
//源数组
int[] source = {1, 2, 3, 4, 5, 6}; //目的数组
int [Jdest = { 10, 9, 8, 7, 6, 5, 4, 3, 2, 1};
//复制源数缓中从下标0开始的source.length个元素到//目的数组，从下标0的位置开始存储。
System.arraycopy( source, 0, dest, 0, source.Length);
```

## 增强的for语句

```java
int[] ages = new int[10]
for(int age:ages){
//实现只读式的遍历
}
```

# 类,包和接口

## 类,字段和方法

类包含字段,构造方法和方法

构造方法和类同名,无返回类型

作用是初始化类的新对象

访问对象的字段或方法需要算符"."

### 方法重载(overload)

多个方法有相同的名字

这些方法的签名不同(参数个数和类型不同)

**通过方法重载可以实现多态**

### this的使用

在方法或构造方法中使用this来访问字段及方法

**使用this解决局部变量和域同名的问题**

使用this还可以解决局部变量（方法中的变量）或参数变量与域变量同名的问题。如，在构造方法中，经常这样用：

```java
Person( int age, String name ){
	this.age = age;
	this.name = name;
}
```

**构造方法中，用this调用另一构造方法**

构造方法中，还可以用this来调用另一构造方法。如：

```java
**Person(){
	this(0,""); 
}**
```

在构造方法中调用另一构造方法，则这条调用语句必须放在第一句。

## 类的继承

一个类只能有一个父类

子类继承父类的状态和行为

可以修改父类的状态

可以重载父类的行为

可以添加新的状态和行为

好处

提高程序的抽象程度

**实现代码重用,提高开发效率和可维护性**

Java的子类是通过extends关键字来实现的

```java
class Student extends Person{

}
```

如果没有extends子句,则默认为java.lang.Object的子类

所有的类都是通过直接或间接继承java.lang.Object得到的

父类的非私有方法可以被子类继承

子类可以重新定义与父类同名的方法,实现对父类的覆盖

**覆盖可以用@Override注解表示**

## 包

用于解决名字空间和名字冲突,与继承无关,子类与父类可以在不同包中

**含义**

1. 名字空间,存储路径
2. 可访问性,同一包中的各个类默认可以互相访问

用import语句导入需要的类

```java
import java.util.Date;
//这样，程序中java.util.Date可以简写为Date

import java.awt.*;
import java.awt.event.*;
//注意：使用星号（＊）只能表示本层次的所有类，不包括子层次下的类。
```

## 访问控制符

![Untitled](%E5%8C%97%E4%BA%AC%E5%A4%A7%E5%AD%A6%E3%80%8AJava%E7%A8%8B%E5%BA%8F%E8%AE%BE%E8%AE%A1%E3%80%8B%E7%AC%94%E8%AE%B0%20b8510b7871064737a8c26df4a27cf5ed/Untitled.png)

### setter和getter

将字段用private修饰可以更好的对信息进行封装和隐藏

用set和get方法对类的属性进行存取

**优点** 

1. 属性用private更好地封装和隐藏，外部类不能随意存取和修改。
2. 提供方法来存取对象的属性，在方法中可以对给定的参数的合法性进行检验。方法可以用来给出计算后的值。
3. 方法可以完成其他必要的工作（如清理资源、设定状态，等等）。
4. 只提供getXXXX方法，而不提供setXXXX方法，可以保证属性是只读的。

```java
class Person2{
	private int age;
	public void setAge( int age ){
		if (age>0 && age<200){
			this.age = age; 
	}
	public int getAge(){
		return age; 
	}
}
```

## 其它修饰符

![Untitled](%E5%8C%97%E4%BA%AC%E5%A4%A7%E5%AD%A6%E3%80%8AJava%E7%A8%8B%E5%BA%8F%E8%AE%BE%E8%AE%A1%E3%80%8B%E7%AC%94%E8%AE%B0%20b8510b7871064737a8c26df4a27cf5ed/Untitled%201.png)

### static

**类属性被static修饰,那么它会被当做GC的一个root根节点,作为根节点也就意味着它基本上不会被回收,因此容易造成内存泄漏问题**

static只能用于修饰内部类

一个内部类没有用static修饰的时候不能直接用内部类创建对象

要先用外部对象 new内部对象

static修饰的方法内部不能够调用非静态方法, 反之非静态方法可以调用静态方法

类变量可以通过类名直接访问,也可以通过实例对象来访问

### final

 修饰类表示不能被继承,不可能有子类

修饰变量表示变量是只读变量

**一个字段被static和final修饰后可以表示常量**

### abstract

abstract修饰的类不能被实例化

abstract修饰的方法叫抽象方法

抽象方法的作用在为所有子类定义一个统一的接口

只需声明,不需要实现,

可以包含抽象或不抽象方法,但是包含抽象方法的类必须声明为abstract

抽象方法在子类中必须被实现,否则子类仍然是abstract

## 接口

某种特征的约定,也是引用类型

定义接口用interface关键词

所有方法都是自动为public abstract的

实现接口用implements关键词

class A implements B{ }

可以实现多继承

与类的继承关系无关

面向接口编程,而不是面向实现

### 作用

1.  通过接口可以实现不相关类的相同行为，而不需要考虑这些类之间的层次关系。从而在一定意义上实现了多重继承。
2. 通过接口可以指明多个类需要实现的方法。
3. 通过接口可以了解对象的交互界面，而不需了解对象所对应的类。

一个接口可以有多个接口

接口可以作为一种数据结构来使用,任何实现该接口的类的实例都可以存储在接口类型的变量中,通过这些变量可以访问类实现的接口中的方法.

把接口作为一种数据类型可以不需要了解对象所对应的具体的类

# 深入理解Java语言

## 多态及虚方法调用

**上溯造型：把派生类当成基本类型处理**

多态指的是相同的名字表示不同含义的情况

两种情形

- 编译时多态
    - 重载
- 运行时多态
    - 覆盖
    - 动态绑定
        - 虚方法调用

多态的特点大大提高了程序的抽象程度和简洁性

所有的非final方法都会自动进行动态绑定

Java中普通的方法是虚方法

但private, static方法不是虚方法调用，与虚方法编译后的指令是不同的

**三种非虚的方法**

1. static的方法以声明的类型为准，与实例类型无关
2. private方法子类看不见，不会被虚化
3. final方法子类无法覆盖，不存在虚化问题

## 对象构造和初始化

```java
p = new Person(){{age=18;name="Ted"}};
```

双括号可以针对没有相应构造函数但要对字段赋值的情况

## 对象清除与垃圾回收

用new创建对象

java中对象能自己清除，不需要delete

垃圾回收是由java虚拟机的垃圾回收线程来完成的

系统判别对象是否为垃圾的依据：任何对象都有一个引用计数器，值为0时说明可以回收

**System.gc()方法**

是System类的static方法，可以要求系统进行垃圾回收，**但只是建议！**

**finalize()方法**

Java中没有构析方法，但finalize()有类似功能

系统在回收时会自动调用这个方法

子类的finalize方法：可以在子类的这个方法释放系统资源，子类这个方法中应该调用父类的finalize()方法，以保证父类的清理工作能正常进行

此方法的调用时机不确定，所以一般不用

关闭打开的文件，清除一些非内存资源等工作需要进行处理，可以使用try-with-resources语句

对于实现了java.lang.AutoCloseable的对象会自动调用其Close方法

## 匿名类和内部类

### 内部类

定义：将类的定义置入一个类的内部即可

内部类不可与外部类重名

使用

在封装它的类的内部使用内部类与使用普通类的方式相同

在其他地方使用内部类需要在类名前加上外部类的名字

在用new创建内部类时也要在new前面冠以对象变量

外部对象名.内部对象名(参数)

内部类可以直接访问外部类的字段和方法，private也可以

内部类可以用public, private, protected修饰（或者默认）（外部类只能用public或者默认），也可以用final和abstract。

用static修饰内部类表面内部类实际上是一种外部类，因为它与外部类的实例无关。

有人认为static的类是嵌套类，不是内部类

static类在使用时

1. 实例化时在new前面不需要用对象实例变量
2. 不能访问其外部类的非static的字段或方法，只能访问static成员
3. 不能访问非static的域和方法，不能不带前缀地new一个非static的内部类

### 局部类

在一个方法中定义类，这种类称为方法的内部类，或者叫局部类

### 匿名类

是一种特殊的内部类

没有类名，在定义类的同时生成该对象的一个实例

一次性使用的类

**匿名类的使用**

1. 不取名字，直接用父类的名字或者接口的名字
2. 定义的同时就创建实例，类定义前面有一个new
    1. new类名或接口名(){......}
    2. 不用关键词class，不用extends和implements
3. 在构造对象时使用父类构造方法

**应用**

注册事件监听器

```java
btnNew.addActionListener(new ActionListener()){
	public void actionPerformed(ActionEvent event){
		btnNew_ActionPerformed(event);
	}
}
```

作为方法的参数

```java
//排序，给一个比较大小的接口
Arrays.<Book>sort{books,new Comparator<Book>(){
	public int compare(Book b1,Book b2){
		return b1.getPrice()-b2.getPrice();
	}
}
```

## Lambda表达式

基本写法：

(参数)→结果

是接口的简写

## 指针在Java中的体现

引用实际上就是指针

但是受控，安全

- 会检查空指引
- 没有指针运算
- 不能访问没有引用到的内存
- 自动回收垃圾

1. 传地址→对象，引用类型本身相当于指针
2. 指针运算→数组
3. 函数指针→接口、lambda表达式
4. 指向结点的指针→对象引用
5. JNI和其它语言进行交互

## 是否相等

基本类型的相等是值相等，引用类型是引用相等

基本类型

- 数值类型：转换后比较
- 浮点数：最好不直接用==（因为有误差）
- Boolean无法和int比较

枚举类型内部进行了唯一的实例化，可以直接判断

引用对象

- 看两个引用是否一样
- 要判断内容是否一样需要重写equals方法
- 如果要重写equals方法则最好重写hashCode方法

String对象判断相等一定要用equals。但是字符串常量会进行内部化，相同的字符串常量是==的

## 其它几个高级语法

### 基本类型的包装类

可以将基本类型包装成引用类型

如int→Integer

共8类：

1. Boolean
2. Byte
3. Short
4. Character
5. Integer
6. Long
7. Float
8. Double

```java
Integer I=new Integer(10);
```

装箱与拆箱

```java
//装箱
Integer I=10;
//拆箱
int i=I;
```

主要方便用于集合中

### 枚举

简单情况中和其它语言的枚举一样

可以在enum定义体中添加字段，方法，构造方法

### 注解

是在各种语法要素上加上附加信息以供编译器和其它程序使用

所有的注解都是java.lang.annotation.Annotation的子类

**常用的注解**

@Override 表示覆盖父类的方法

@Deprecated 表示过时的方法

@SuppressWarnings 表示让编译器不产生警告

自定义注解比较复杂

# 异常处理

## 相关语句

抛出异常

throw 异常对象;

捕获异常

```java
try{

}catch(){

}catch(){

}
finally{

}
```

可以没有catch和finally，但是catch无上限，finally最多一个

**异常的分类**

- throwable
    - error：jvm虚拟机的错误
    - exception：一般所说的异常都指exception及其子类

**exception类**

构造方法

- public Exception();
- public Exception(String message);
- Exception(String message, Throwable cause);

方法

- getMessage()
- getCause
- printStackTrace()

多异常的处理

子类通常排在父类异常的前面

finally语句

无论是否异常都要执行

即使其中有break，return等语句

在编译时，finally部分代码生成了很多遍

### 受检的异常

Exception分两种

- runtime及其子类，可以不明确处理
- 否则称为受检的异常

受检的异常要求明确进行语法处理

- 要么捕
- 要么抛：在方法的前面后用throws xxx来声明
  
    在子类中，如果要覆盖父类的一个方法，若父类的方法声明了throws异常，则子类的方法也可以throws异常
    
    可以抛出子类异常（更具体的异常），但不能抛出更一般的异常
    

---

try with resource

```java
try(类型 变量名 = new 类型()){

}
```

自动添加了finally{ 变量.close(); }

## 自定义异常

创建用户自定义异常时

1. 继承自Exception类或某个子Exception类
2. 定义属性和方法，或重载父类的方法

**重抛异常及异常链接**

对于异常不仅要捕获，也要进一步传递给调用者

1. 将当前捕获的异常再次抛出
2. 重新生成一个异常并抛出
3. 重新生成一个新异常并抛出，包含当前异常的信息
   
    ```java
    throw new Exception("some message", e);
    ```
    
    可用e.getCause()来得到内部异常
    

## 断言及程序的调试

### 断言

assert的格式是：

assert表达式;

assert表达式:信息;

在调试程序时

如果表达式不为true，则程序产生异常，并输出相关的错误信息

### 程序的测试及JUnit

编写程序代码的同时还要编写测试代码来判断这些程序是否正确，这个过程称为测试驱动的开发过程

在Java的测试过程中经常使用JUnit框架，现在大多数工具都提供支持

## 程序的调试

程序中的错误一般分三大类

- 语法错误
    - 编辑器发现
    - 编译器发现
- 运行错误
    - 异常处理机制
- 逻辑错误
    - 调试
    - 单元测试

调试的三种手段

- 断点
- 跟踪
- 监视

监视

即时监视

鼠标指向变量

快速监视

右键Inspector

添加监视

右键Watch

# 工具类以及常用算法

## Java语言基础类

### Java基础类库

- java.lang：核心类库
- java.util：实用工具
- java.io：标准输入输出
- java.awt javax.swing：图形用户界面
- java.net：网络功能
- java.sql：数据库访问

![Untitled](%E5%8C%97%E4%BA%AC%E5%A4%A7%E5%AD%A6%E3%80%8AJava%E7%A8%8B%E5%BA%8F%E8%AE%BE%E8%AE%A1%E3%80%8B%E7%AC%94%E8%AE%B0%20b8510b7871064737a8c26df4a27cf5ed/Untitled%202.png)

### Object类

是所有类的直接或间接父类，让所有的类有一致性

**equals()**

==与equals的区别

==判断的是引用是否相等，equals可以判断内容相等

如果要覆盖equals，那么一般也要覆盖hashCode()方法

**getClass()**

是一个final方法，不能被重载

返回一个对象在运行时所对应的类的表示

**toString()**

用来返回对象的字符串表示

常用于显示

```java
System.out.println();
```

通过重载toString方法可以适当的显示对象的信息进行调试

**finalize()**

用于在垃圾收集前清除对象

### 基本数据类型的包装类

特点

1. 都提供了一些常数
2. 提供了valveOf(String)，toString()
   
    用于从字符串转换或转换成字符串
    
3. 通过xxxValue()方法可以得到所包装的值
   
    如Integer对象的intValue()方法
    
4. 对象中包装的值是不可改变的，要改变只能生成新的对象
5. toString()，equals()等方法进行了覆盖
6. 有些类还提供了一些实用的方法以方便操作
   
    如Double类提供了parseDouble()，max，min方法等
    

### 包装与拆包

jdk1.5以上有包装和拆包

### Maths类

用来完成一些常用的数学运算

### System类

## 字符串以及日期

### 字符串

可以分为两大类

- String类
    - 创建之后不会再修改和变动，即immutable
- StringBuffer, StringBuilder类
    - 允许再做修改和变化
    - 其中StringBuilder是Jdk1.5后增加的，是非线程安全的

注意：在循环中使用String的+=可能带来效率问题

**String类**

String类对象保存不可修改的Unicode字符序列

查找：endsWith, startsWith, indexOf, lastIndexOf

比较：equals, equalsIgnoreCase

字符及长度：charAt, length

Jdk1.5增加了Format函数

**字符串常量**

除了immutable特点外，还要注意String常量的内部化问题

相同的字符串常量是指向同一个引用的，可以用==比较

**StringBuffer类**

保存可修改的Unicode字符序列

StringBuilder类似，但是效率更高，不考虑线程安全性

构造方法

- StringBuffer()
- StringBuffer(int capacity)
- StringBuffer(String initialString)

实现修改操作的方式：

append, insert, reverse, setCharAt, setLength

### 字符串的分割

java.util.StringToken提供对字符串进行分割的功能

构造

StringTokenizer(String str, String delim);

该类的重要方法有

- pubic int countTokens(); //分割串的个数
- public boolean hasMoreTokens(); //是否还有分割串
- public String nextToken(); //得到下一分割串

### 日期类

- Calendar
    - 得到一个实例 Calendar.getInstance()
    - .get(DAY_OF_MONTH) .getDisplayName(DAY_OF_WEEK)
    - .set .add(HOUR,1) .roll(MONTH,5)
    - .setTime(date), .getTime()
- Date
    - new Date(), new Date(System.currentTimeMills())
    - .setTime(long), .getTime()
- SimpleDateFormat("yyyy-MM-dd HH:mm:ss")
    - .format
    - .parse

### Java中的time api

- java.time.*
- java.time.format.*
- 主要的类
    - Instant 时刻 Clock 时区 Duration 时间段
    - 常用的类 LocalDateTime LocalDate LocalTime
        - .of .parse .format .plus .minus
    - DateTimeFormatter

## 集合

Collection API提供集合 收集 的功能，包含一系列的接口和类

### 包含三大类

- Collection接口：有两个子接口
    - List：记录元素的保存顺序，允许有重复元素
    - Set：不记录保存顺序，不允许有重复元素
- Map接口：映射
    - 键值对的集合

![Untitled](%E5%8C%97%E4%BA%AC%E5%A4%A7%E5%AD%A6%E3%80%8AJava%E7%A8%8B%E5%BA%8F%E8%AE%BE%E8%AE%A1%E3%80%8B%E7%AC%94%E8%AE%B0%20b8510b7871064737a8c26df4a27cf5ed/Untitled%203.png)

![Untitled](%E5%8C%97%E4%BA%AC%E5%A4%A7%E5%AD%A6%E3%80%8AJava%E7%A8%8B%E5%BA%8F%E8%AE%BE%E8%AE%A1%E3%80%8B%E7%AC%94%E8%AE%B0%20b8510b7871064737a8c26df4a27cf5ed/Untitled%204.png)

### List

主要的实现类是ArrayList.LinkedList以及早期的Vector

List接口

### 迭代器

Iterator，所有的Collection都能产生

```java
Iterator iterator = iterable.iterator();
while(iterator.hasNext()) doSomething(iterator.next());
```

### 增强的for语句

```java
for(Element e : list) doSomething(e);
```

### Stack 栈

遵循后进先出（Last In First Out, LIFO）原则

重要线性数据结构

包含三个方法

```java
public Object push(Object item)//将指定对象压入栈中
public Object pop()//将栈最上面的元素从栈中取出，并返回这个对象
public boolean empty()//判断栈中没有对象元素
```

### 队列 Queue

- 遵循先进先出（First In First Out, FIFO）的原则
- 固定一端输入数据（入队），另一端输出数据（出队）
- 重要的实现是LinkedList类

### Set 集

- 两个重要的实现HashSet以及TreeSet
- 其中TreeSet的底层使用TreeMap来实现的

Set中对象不重复，即：

- hashCode()不等
- 如果hashCode()相等，再看equals或==是否为false

Hashtable的实现

String对象的哈希码根据一

s[0]*31^(n-1) + s[1]*31^(n-2)+ ...+ s[n-1]

使用int算法，这里s[i]是字符串的第i个字符，n是字符串的长度，^表示求幂。

（空字符串的哈希值为0。)

### Map

map是键值对的集合

- 其中可以取到entrySet()、keySet()、values()
- Map.Entry是一个嵌套接口

Map类的重要实现

- HashMap类
- TreeMap类：用红黑树的算法

## 排序与查找

- 自编程序
- 系统已有的排序与查找
    - 如Arrays类及Collections类

### Arrays类

# 多线程

## 创建

### 线程体

通过run()方法实现，线程启动后自动调用run()方法，通常执行一个时间较长的操作

```java
//1.通过继承Thread类创建
class MyThread extends Thread{
    public void run(){
        for(int i=0;i<100;i++){
            System.out.print(" "+i);
        }
    }
}
//2.通过Thread()构造方法传递Runnable对象创建
class MyTask implements Runnable{
    public void run(){...}
}
Thread thread = new Thread(mytask);
thread.start();
```

## 控制

![线程的状态与生命周期_1](D:\Github笔记\图床\线程的状态与生命周期_1.png)

### 对线程的基本控制

- 启动
  - start
- 结束
  - 设定一个标记变量，以及结束相应的循环、方法
- 暂时阻止线程的执行
  - ` try{Thread.sleep(1000);}catch(InterruptedException e){}`

设定线程的优先级

- `setPriority(int priority)方法`
  - MIN_PRIORITY
  - MAX_PRIORITY
  - NORM_PRIORITY

### 后台线程

线程有两种

- 一类是普通线程
  - 程序中如果还有普通线程则整个程序就不会结束
- 一类是Daemon线程（守护线程，后台线程）
  - 普通线程结束了后台线程自动停止
  - 垃圾回收线程是后台线程

使用`setDaemon(true);`

# 流、文件及基于文本的应用

## 输入输出流

把不同类型的输入输出称为流，按流的方向分为输入和输出流

通过java.io包实现，从java4加入ava.nio包，jdk1.7做了改进称为nio2