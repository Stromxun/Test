# ProblemSet 3

### 1、下列标识符哪些是合法的？

    $88,#67,num,applet,Applet,7#T,b++,--b

合法：
``` 
    $88 Java中美元符号 '\$'可以放标识符首位
    num、applet和Applet 全由字母组成且不是保留字或者关键字
```

不合法：

```
   7#t、b++和--b 当中均具有Java命名准则中不允许出现的字符
```

### 2、Java有哪些基本数据类型？什么是复合数据类型？对于这两种类型的变量，系统的处理有什么不同？

基本数据类型：

逻辑型：**boolean** 

文本型：**char**

整型：**byte、short、int**和**long**

浮点型：**double**和**float**

复合数据类型： **类**和**接口**

不同：
```
    Java中，基本数据类型定义的基本类型变量(primitive type)声明将会被系统直接分配空间，使得程序可以直接进行操作。而
    复合数据类型所定义的引用类型(reference type)，系统只会给该变量分配引用空间，数据空间为分配，以至于引用型变量声明后不能
    直接引用。
```

### 3、设变量i和j的定义如下，试分别计算下列表达式的值
```cpp
    int i=1;double d=1.0;
    (1) 35/4  //value=8
    (2) 46%9+4*4-2  //value=15
    (3) 45+43%5*(23*3%2)  //value=48
    (4) 45+45*50%i--  //value=45
    (5) 45+45*50%(--i)  //该表达式抛出异常(mod 0 是未定义行为)
    (6) 1.5*3+(++d)  //value=6.5
    (7) 1.5*3+d++  //value=5.5
    (8) i+=3/i+3  //value=7
```

### 4、计算下列逻辑运算表达式的值。 

```cpp
    (1) (true)&&(3>4);   //value=0
    (2) !(x>0) &&(x>0);  //value=0
    (3) (x>0)||(x<0);    //当x==0时该表达式的值是0，其他为1
    (4) (x!=0)||(x==0);  //value=1
    (5) (x>=0)||(x<0);   //value=1
    (6) (x!=1)==!(x==1); //value=1
```

### 5、Java中有哪些类型的程序流控制语句？

**循环语句**： while、do while 和 for

**分支语句**： if 和 switch

**跳转语句**:  break、continue、lable 和 return

**异常处理语句**： try catch finally 和 throw

### 6、switch语句与if语句可以相互转换吗？使用switch语句的优点是什么？

switch语句的结构功能可以用if else iuf 结构来实现。
优点：switch结构更简单，可读性更强，而且程序的执行效率更高

### 7、试写出下列循环的运行结构。

```java
    int i=1;
    while(i<10){
        if((i++)%2==0){
            System.out.println(i);
        }
    }
```
ans:
>3
5
7
9

### 8、while循环和do while循环有什么区别？

**while**: 先判断逻辑表达式，再执行语句块中的代码

**do while**: 先执行语句块中的代码，再进行逻辑表达式的判断

### 9、循环跳转语句break的作用是什么？试给出下列程序的运行结果。

**break的作用**：可以结束流控制语句中的 _循环语句_ 和 _分支语句中的switch_ 。

```java
    int i=1000;
    while(true){
        if(i<10){
            break;
        }
        i=i-10;
    }
    System.out.println("This value of i is "+i);
```
ans:
>This value of i is 0

### 10、循环语句 continue 的作用是什么？试给出下列程序的运行结果

**continue的作用**：跳过循环体的剩余语句，开始执行下一次循环
```java
    int i=1000;
    while(true){
        if(i<10){
            continue;
        }
        i=i-10;
    }
```
ans:该程序因不存在循环终点，无法跳出循环，会无限循环下去。

### 11、编写程序输出1000以内的所有奇数。
```java
    public class OutputOddNum{
        public static void main(String args[]){
            for(int i=1;i<=1000;i++){
                if(i%2)
                    System.out.println(i);
            }
        }
    }
```

### 12、编写程序输出下列结果。
```
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
1 2 3 4 5 6
```

```java
//介绍两种方法
public class OutpuAns{
    public static void main(String args[]){
        System.out.println("1");
        System.out.println("1 2");
        System.out.println("1 2 3");
        System.out.println("1 2 3 4");
        System.out.println("1 2 3 4 5");
        System.out.println("1 2 3 4 5 6");
    } 
}

public class OutpuAns{
    public static void main(String args[]){
         for(int i=1;i<=6;i++){
            for(int j=1;j<=i;j++){
                System.out.print(j+" ");//记住输出空格
            }
            System.out.println();
        }
    } 
}
```

### 13、下列数组声明哪些是合法的？

```cpp
    (1) int i=new int(30);              //不合法，i不是个数组
    (2) double d[]=new double[30];      //合法
    (3) Integer[] r=new Integer(1..3);  //不合法
    (4) int i[]=(3,4,3,2);              //不合法，数组还没有分配存储数据的内存空间，无法存储数据
    (5) float f[]={2.3,4.5,5.6};        //不合法，数组还没有分配存储数据的内存空间，无法存储数据
    (6) char[] c=new char();            //不合法，new char()是未定义的行为，应该用[]并且在当中填上适当的参数
    (7) Integer[][] r=new Integer[2];   //不合法，参数不足
```

### 14、数组变量是基本类型变量还是引用型变量？数组的内存时什么时候分配的？

>数组变量是引用型变量，数组的内存通过new运算符或通过数组初始化分配的

### 15、编写程序，创建一个整形的 $5X5$ 的矩阵，并将其输出显示。

```java
    public class OutputMatrix{
        public static void main(String args[]){
        int k=1;
        for(int i=1;i<=5;i++){
            for(int j=1;j<=5;j++){
                    if(k<10)
                        System.out.print(" ");
                    System.out.print(k+++" ");
                }
                System.out.println();
            }
        }
    }
```

---

date:2/21/2023     writer: **Xun**
