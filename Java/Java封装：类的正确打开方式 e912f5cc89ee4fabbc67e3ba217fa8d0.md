# Java封装：类的正确打开方式

作用

```
 * 减少耦合
 * 内部结构可修改
 * 可对成员变量精确控制
 * 隐藏信息，实现细节
```

# **步骤**

修改属性的可见性来限制对属性的访问（一般限制为private）

对每个值属性提供对外的公共方法访问，也就是创建一对赋取值方法，用于对私有属性的访问

```
 public class Person{
     private String name;
     private int age;
 •
     public int getAge(){
       return age;
     }
 •
     public String getName(){
       return name;
     }
 •
     public void setAge(int age){
       this.age = age;
     }
 •
     public void setName(String name){
       this.name = name;
     }
 }
```