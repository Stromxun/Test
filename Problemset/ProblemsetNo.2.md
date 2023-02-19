 # Promblem Set $2$
 ### 1、什么是对象？什么是类？什么是实体？他们之间的相互关系是怎样的？试举例说明。

 **对象** : 是现实世界实体或概念在计算机世界中的抽象表示，是具有唯一对象名、固定对外接口的一组变量/属性的方法集合，是用来模拟组成或影响现实世界问题的一个或一组因素。
 
 **类**：是一种模板或原型，它定义了某种类型所有对象都具有的变量和方法。
 
**实体**：是被对象进行抽象化的现实世界存在的事物。

关系：  $实体-抽象化->对象类型-转换->类$
   $~~~~~~~~~~$   $类是对象的抽象化$   $~~~~对象是类的实例化$

 ---
 ### 2、什么是对象的状态与行为？设有对象“学生”，试给出这个对象的状态和行为。
   **状态**：对象专用的内部变量。
   
   **行为**：对对象的操作。
   
   描述学生类：
   ```java
class Student{
    public Student(String Name,double Age,char Sex,String i,String A){
        this.Name=Name;
        this.Age=Age;
        this.Sex=Sex;
        this.id_of_Student=i;
        this.Address_of_home=A;
    }
    public void ShowTime(){
        System.out.println("大家好！我是来自"+this.Address_of_home+'的'+this.Name+"，我鸡年"+this.Age+"岁了"+"，我喜欢"+this.id_of_Student+",Music!");
    }
    private String Name;//学生的名字
    private char Sex;//学生的性别
    private double Age;//学生的年龄
    private String id_of_Student;//学生的学号
    private String Address_of_home;//学生的家庭住址
}
public class ConstructStudent{
    public static void main(String args[]){
        Student student=new Student("蔡徐坤",2.5,'男',"唱、跳、Rap篮球","偶像练习生");
        student.ShowTime();
    }
}
   ```

 ---
 ### 3、什么是封装数据与隐藏？
**封装**：将对象的变量与实现构成了对象的内核，对象的方法包裹着对象的内核，使对象的内核能够对程序中其他对象隐藏。通俗一点就是：使用对象的方法将对象的变量与实现保护起来被称为 _封装_。

**隐藏**：通过对象的接口封装，使得私有变量和私有实现被有效保护。

 ---
 ### 4、什么是上溯造型？什么是晚联编？多态的含义是什么？
 **上溯造型**：子类沿着类型继承体系向上，将其类型塑造为父类类型就是把子类当做父类处理的过程。(原理类似于C++中的动态绑定)

**晚联编**：当向一个对象发消息时，直到代码运行时才会确定需要执行准确代码。

**多态**：简而言之就是“对外一个接口，内部多种形态”。

 --- 
 ### 5、怎样理解面向对象程序设计方法的内涵？
   面向对象程序设计的目的，就是要定义或重用能够提供解决问题所需要服务的一系列对象。

 ---
 ### 6、面向对象程序设计有哪些优点？
 * **代码重用**：拥有大量类库，提高开发效率，缩短开发周期，降低开发成本，提高程序代码的可靠性，减少了程序的维护工作量，提高了程序的标准化程度。

* **可扩展性**
 
 * **可管理与维护性**

 ---
 
date:2/19/2023     writer: **Xun**
