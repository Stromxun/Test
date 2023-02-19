
# Problem Set

### 1 . 简述Java技术体系的组成
 $1.$ Java Platform Standard Edition——**Java SE**
 $2.$ Java Platform Enterprise Edition——**Java EE**
 $3.$ Java Platform Micro Edition——**Java ME**
---
 ### 2 .Java的语言特征有哪些?简述这些特征的含义。

$1.$简单性
~~~
    Java的语法和语义比较单纯，容易学习和使用。Java对C++中容易引起错误的成分进行了相当成功的改造。Java还提供大量
功能丰富的可重用类库，简化了编程工作量
~~~
$2.$ 面向对象(OOP) 
~~~
    Java是一种面向对象语言，它对面向对象方法学的支持也最为全面。
    封装：Java具有模块化性质和信息隐藏能力
    继承：Java支持面对对象的继承性
    多态：Java通过抽象类和接口(interface)支持面对对象的多态性
~~~
$3.$分布式特征
~~~
    Java支持分布式计算的特征。
    “分布”具有两层含义：数据分布和操作分布
    数据分布：应用系统所操作的数据可以分散存储在不同的网络节点上；
    操作分布：应用系统可由不同的网络节点完成
~~~
$4.$半编译、半解释特征 
~~~
    Java应用程序的执行过程具有半编译、半解释的特征。即编译器将源码编译成中性字节码，再通过解释器将字节码进行输入
    优点：1、提高了Java的可移植性 2、兼具编译执行的效率优势和解释执行的灵活性
~~~
$5.$ 强壮性 
~~~
    Java提供自动垃圾收集来进行内存管理，防止程序员在管理内存时容易产生的错误。此外，Java程序在编译时要经过严格的
类型检查，防止程序运行时出现内存不匹配等问题
~~~
$6.$ 安全性
~~~
    Java的主要安全机制如下两种：1、内存分配及布局由Java运行系统规定 
    2、运行系统执行基于数字签名技术的代码认证、字节码验证与代码访问权限控制的安全控制模型
    编译时字节码验证器会保证下列问题正确：
    1、不存在伪造的指针
    2、未违反访问权限
    3、严格遵循对象访问规范来访问对象
    4、用合格的参数调用方法
    5、没有栈溢出等
~~~
$7.$ 体系结构中立
~~~
    Java语言的设计不是针对某种具体平台结构的。生成字节码和可扩展类库促成这个特性
~~~
$8.$ 可移植性
~~~
    任何机器只要配备了Java解释器，便可运行Java程序。特征4和特征7为此特性提供基础
~~~
$9.$ 高性能
~~~
    字节码与机器码十分接近，使得字节码到机器码的转换十分快捷。Java提供及时编译技术，将字节码转换成机器码后，
    将全速运行
~~~
$10.$ 多线程
~~~
    线程是比进程更小开销更少的并发执行单位。线程机制在操作系统(Operating System)领域广泛使用，并且改善系统
    运行效率方面取得明显的效果。如果OS支持多线程，Java的线程通常被映射到实际的操作系统线程中。
    这意味着在多机环境下，用Java写的程序可以并行执行
~~~
$11.$动态特性
~~~
    Java的动态特性是面对对象设计的延伸。使得Java的类又是运行时动态装载的，使得Java能动态地维护应用程序及其支持类
    之间的一种性
~~~
---
### 3 .Java语言的语法机制与C/C++有何异同
类中的访问权限修饰符
~~~
    同：Java和C/C++都支持 public、protected和private
    异：Java还支持final和abstract
~~~
引入库限定符
~~~
    同：Java和C/C++都支持引入库限定符
    异：Java通过 import 语句 C/C++是通过 #include<> 预命令
~~~
面向对象三大特性之一：多态
~~~
    同：Java和C++都支持多态这一特性
    异：Java通过接口(interface)来实现多态  C++通过 virtual 关键字构建虚函数来实现
~~~
指针(pointer)
~~~
    异：Java取消了指针语法，动态内存分配改为通过引用的方式进行 
    C++还进一步延伸了指针：智能指针(模板类) shared_ptr、unique_ptr和weak_ptr 预防内存泄漏
~~~
---
### 4 .Java运行系统由哪些部分组成？Java程序的运行过程是怎样的 
    Java的运行系统：类装配器、字节码验证器、解释器、代码生成器和运行支持库。
    Java的运行过程：代码的装入->代码的验证->代码的执行
---
### 5 . 什么是JVM
Java的目标代码在执行时需要有Java运行系统的支持。Java运行系统是建立在各种不同的平台上，与具体平台有关。为了做到Java的可移植性，各个平台上的Java运行系统的功能是要求统一的。为此Java引入了JVM

---
### 6 .下载并安装Java SE8以及Java API 文档，编译并运行例1-1.
  [Java下载](https://download.oracle.com/java/19/latest/jdk-19_windows-x64_bin.exe)Java8下载不了就只能下Java19喽
  [Java API 文档下载](https://download.oracle.com/otn_software/java/jdk/19.0.2+7/fdb695a9d9064ad6b064dc6df578380c/jdk-19.0.2_doc-all.zip)
  >例1.1
  ```java
  public class HelloWorld{
    public static void main(String args[]){
        System.out.println("Hello World!");
    }
  }
  ```
---
  ### 7 .编写一个Java程序，在屏幕上输出“欢迎学习Java语言！”的字符串。
  ```java
  public class HelloWorld{
    public static void main(String args[]){
        System.out.println("欢迎学习Java语言！");
    }
  }
  ```
---
  date:2/19/2023     writer:**Xun**
