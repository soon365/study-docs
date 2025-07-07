

# 计算机的体系结构

计算机由硬件和软件两个部分组成。

硬件是实体的设备，软件是可下载的应用app。

硬件：cpu、内存、硬盘、显卡、键盘、显示器、鼠标。

重点讲三个

|                       cpu                       | 内存                                                    | 硬盘                                       |
| :---------------------------------------------: | ------------------------------------------------------- | ------------------------------------------ |
| 定义-是中央处理器也是计算机最核心的部件（人脑） | 定义-是计算机的存储部件。（记忆功能）                   | 定义-是计算机的存储部件。（记忆功能）      |
|          作用-主要用于处理指令以及数据          | 作用-主要用于临时存放cpu访问的数据，cpu直接访问且效率高 | 缺点-cup不能直接访问硬盘的数据，所以效率低 |
|    应用-在手机上的高通 晓龙，电脑上的i7、i9     | 缺点-容量小，一旦断电会造成数据的丢失 要时刻记的要保存  | 优点-容量大，若断电不会造成数据丢失        |

``

> [!TIP]
>
> 拓展：1tb=1024gb
>
> ​	   1gb=1024mb
>
> ​	  1mb=1024kb
>
> ​	  1kb=1024byte（字节）一个英文字母占一个字节，一个汉字占两个字节
>
> ​	  1byte=8bit（二进制位）在计算机的0、1组成的二进制序列
>
> ​          其中键盘叫做标准输入设备，显示器叫做标准输出设备。
>
> ​	  硬件厂商是采用1000作为进率 计算机是采用1024作为进率。

``

[^Tip]: 硬件设备-&gt;系统软件-&gt;应用软件-&gt;用户（其中系统软件分为内核和外壳）



# Java语音的概述

Java SE Java平台标准版 主要学习Java语言的语法规范和常见类

Java EE Java平台企业版 主要学习Java后台开发技术，编写B\S架构项目。

Java MEJava平台微型版 快被淘汰了

##  开发环境的搭建和使用

jdk的下载和安装

下载地址：oracle.com

jdk安装路径里不能有中文

| jdk                                            | jre                                                  | jvm                                          | javac.exe                                              | java.exe                                                     |
| ---------------------------------------------- | ---------------------------------------------------- | -------------------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------ |
| Java开发工具包，只要做Java开发就需要下载和安装 | Java运行时环境信息，只要运行Java程序就需要下载和安装 | Java虚拟机，是Java与计算机操作系统之间的桥梁 | Java语言的编译器，主要用于Java源代码进行生成字节码文件 | Java语言的解释器，主要用于Java虚拟机对字节码文件进行解释执行 |

## Java程序的编写流程

1. 新建文本文档，将文件名改成xxx.Java；

2. 使用记事本打开文件，编写Java代码后进行保存；

3. 启动cmd窗口，切换到xxx.Java文件的路径；

4. 使用javac.exe进行编译，生成xxx.class的字节码文件；

5. 使用java xxx进行解释执行，打印最终结果；

   

## 配置环境变量

```java
/*
*项目名称：编写第一个Java程序
*项目功能：打印一句话
*作    者：简之航
*版    本：v1.0
*所 有 者：简之航
*备    注：测试
*/
public class HelloWorld/*类名*/
{
    /*类体*/
    public static void main/*主方法，是程序入口*/(String[] args)
    {
    /*方法体*/ 
    System.out.println("我就不打印Hello World!");
    }
}
```

## -更改path

(1)基本概念：

通常情况下可执行文件只能在该文件所在的路径中访问，若希望该可执行文件可以在任意路径中使用 则需要将该可执行文件的路径信息配置到环境变量path中。

(2)实现方式：

此电脑⇒高级属性⇒环境变量⇒系统变量⇒path⇒第一行填写⇒jdk的bin文件的路径

配置完了要重启命令提示符

## 跨平台原理

由于不同的操作系统中都提供了Java虚拟机经行翻译，因此Java字节码可以通过jvm翻译为具体平台能够执行的机器指令。【一次编译，到处运行】

# Java语言的基本语法格式

## 变量和注释

当需要在Java程序中记录单个数据内容时，则声明一个变量，而变量的本质就是在内存空间中申请一块存储单元，由于该储存单元的数值可以改变，所以叫它“变量”。

由于存放数据内容的大小不同导致所需要存储单元的容量不同，在Java语言中使用”数据类型“加以描述，为了便于下次访问还需要指定变量的名称。

> [!NOTE]
>
> int是整数类型，String是字符串类型

### 声明变量和初始化

- 数据类型 变量名 = 初始值 ;
- 其中 = 初始值可以省略，默认要写上

```java
/*
    编程实现变量的声明和使用
*/
public class VarTest
{
    public static void main(String[] args)
    {
    //1.声明一个初始值为10的元素类型为int类型的变量
    int ia = 10;
    //2.打印变量的数值 + 字符串连接符，用于实现连接的功能
    System.out.println("ia = " + ia);
    //ia = 10
    System.out.println("-------------------------");
    String sa = "hello";
    System.out.println("sa = " + sa);
    //sa = hello
    }
}
```

```java
//变量在使用之前必须声明
System.out.println("sa = " + sa);// 找不到符号
```

```java
//变量在使用之前必须初始化
String sa;
System.out.println("sa = " + sa);//尚未初始化变量sa
```

```java
int ia = 10;
int ia = 20;
//变量不能重复声明
```

### 标识符（变量名）的命名规则

1. 要求由字母、数字、下划线、以及美元$组成，其中数字不能开头比如：name，age，name1，age1
2. 不能是Java的关键字，关键字就是Java中用于表示特殊含义的单词，比如：public，static，class
3. 大小写敏感，长度没有限制，但不宜过长
4. 标识符尽量做到见名知意，可以是汉字，但不推荐使用

### 变量的输入和输出

```java
/*
   打印自己的姓名和年龄
*/
//导入Java目录⇒util目录⇒Scanner
import java.util.Scanner;
public class AnLi
{
    public static void main(String[] args)
    {
    //1.声明两个变量分别用于记录姓名和年龄
    String name;
    int age;
    System.out.println("请输入你的姓名和年龄：");
    //2.创建扫描器对象来扫描键盘的输入
    Scanner sc =new Scanner(System.in);
    //通过扫描器读取一个字符串存放到变量name中
    name = sc.next();
    //通过扫描器读取一个整数存放到变量age中
    age = sc.nextInt();
    //3.打印变量的数值
    System.out.println("name = " + name);
    system.out.println("age = " + age);
    }
}
```

> [!NOTE]
>
> 优化声明和存放

```java
//通过扫描器读取一个字符串存放到变量name中
String name = sc.next();
//通过扫描器读取一个整数存放到变量age中
int age = sc.nextInt();
System.out.println("name =" + name +", age = " + age);
```

### Java API的使用

- JDK中带有大量的API类，是有Java系统带来的工具库，这些工具是Java官方的技术积累
- 这类存储在JAVA_HOME/jre/lib/rt.jar等文件中，比如：java.lang.string.class java.lang.System.class
- 这些类可以大大简化编程，提高编程，提高开发效率，使用API类要用import语句导入类，比如import java.util.Scanner

### Java的注释

- 注释用于解释代码，给程序员看但计算机忽略注释，有以下三种：
  1. //  单行注释，从//开始，到本行结束，都是注释
  2. /**/  多行注释，从/*开始，到*/到结束，中间所以都是注释
  3. /* 多行注释，从/开始，到*/结束，是一种支持提取的注释
  4. 多行注释不允许嵌套使用！

## 数据类型

- 在Java语言中将数据类型分为两大类：
  1. 基本数据类型：byte，short ，int，long，float，double，boolean，char
  2. 引用数据类型：数组，类，接口，注解，枚举
- 常用的进制：
  1. 在日常生活中采用十进制进行数据的描述，权重10^0，10^1，10^2
  2. 在计算机底层采用二进制进行数据的描述，权重2^0，2^1，2^2，由于现实生活中的数据具有正负数，所以二进制采用最高位(最左边)代表符号位，若是0则代表非负数，若是1则代表负数
- 进制的转换
  1. 正十进制转换为二进制的方式
     - 除二取余法，使用十进制整数不断地除以二直到商为零时将余数逆序排序
     - 拆分法，将十进制整数拆分为若干个二进制权重的和，若有该权重下面写一，否则写零
  2. 正二进制转换为十进制的方式
     - 加权法，使用二进制中的每个数字乘以当前位的权重再累加起来
  3. 负十进制转换为二进制的方式
     - 先将十进制的绝对值转换为二进制，进行按位取反再加一
  4. 负二进制转换为十进制的方式
     - 先减一再按位取反，然后合并为十进制整数后添加负号

## 运算符与分支结构

### 运算符

1. +表示加法运算符    -表示减法运算发   *表示乘法运算符    /表示除法运算符   %表示取模/取余运算符

```java
/*
    编程实现算术运算符的使用
*/

public class SuanShu
{
    public static void main(String[] sags)
    {
    //1.声明两个int类型的变量ia和ib，分别初始化为10和20
    int ia = 10;
    int ib = 20;
    //2.使用算术运算符进行计算
    //表示计算ia和ib的和赋值给变量ic
    //其中ia+ib这个整体叫做表达式，ia和ib叫做操作数，+叫做操作/运算符
    int ic = ia + ib;
    System.out.println("ic = " + ic);//ic = 30
    System.out.println(ia + ib);//30
    System.out.println(ia - ib);//-10
    System.out.println(ia * ib);//200
    System.out.println(ia / ib);//0
    System.out.println(ia % ib);//10
    System.out.println("----------------------------") ;     //3.算术运算符的注意事项
    ia = 21;
    System.out.println(ia / ib);//1
    System.out.println((double)(ia / ib));//1.0
    //希望保留小数部分  
    System.out.println((double)ia / ib);//1.05
    System.out.println(ia / (double)ib);//1.05
    System.out.println(1.0*ia / ib);//1.05
    System.out.println("----------------------------") ;
    //0和0.0做除数的效果 
    //编译ok，运行发生ArithmeticException 算数异常
    //System.out.println(2/0);
    //System.out.println(2/0);
    //编译ok，运行显示Infinity 无穷
    }
}
```

> [!IMPORTANT]
>
> 在Java语言中两个整数相除时，结果只保留整数部分丢弃小数部分
>
> 若希望保留小数部分 
>
> 1.将其中任意一个操作数强转为double类型进行运算
>
> 2.也可以让其中任意一个操作数乘以1.0后进行运算
>
> 3.+既可以作为算术运算符也可以作为字符串连接符，区分方式如下：只要+两端的操作数中有一个是字符串类型，则按照字符串连接符对待

```java
/*
    要输出x小时x分x秒。
*/
import java.util.Scanner;
 public class AnLi1
{
    public static void main(String[] sags)
    {
    System.out.println("请输入整数类型的秒数：");
    Scanner sc =new Scanner(System.in);
    int miao = sc.nextInt();
    int shi = miao / 3600;
    int fen = miao % 3600 / 60;
    int Miao =miao % 60;
    System.out.println(shi + "小时" + fen + "分" + Miao + "秒");
    }
}
```

###  关系/比较运算符

1、>表示是否大于运算符 

2、<表示是否小于运算符 

3、<=表示是否小于等于运算符 

4、>=表示是否大于等于运算符 

5、==表示是否等于运算符 

6、!=表示是否不等于运算符 

> [!IMPORTANT]
>
> 所有以关系运算符作为最终运算的表达式结果一定是boolean类型，只有true(1)和false(0)

```java
/*
    关系运算符的使用
*/
public class GuanXi
{
    public static void main(String[] args)
    {
    int ia = 3;
    int ib = 2;
    System.out.println("ia = " + ia);
    System.out.println("ib = " + ib);
    System.out.println("-----------------------------");
    //使用关系运算符进行比较并打印结果
    System.out.println(ib > ib);  //false
    System.out.println(ib >= ib); //true
    System.out.println(ib < ib);  //false
    System.out.println(ib <= ib); //true
    System.out.println(ib == ib); //true
    System.out.println(ib != ib); //false
    }
}
```

```java
/*
    整数是否为负数
*/
import java.util.Scanner;
public class AnLi2
{
    public static void main(String[] args)
    {
    int guize = 0;
    System.out.println("请输入一个整数");
    Scanner sc =new Scanner(System.in);
    int shu = sc.nextInt();
    System.out.println("-----------------------------");
    //使用关系运算符进行比较并打印结果
    System.out.println(guize < shu);
    }
}
```

### 自增减运算符

++表示自增运算符，主要用于使得变量自身的数值加一

--表示自减运算符，主要用于使得变量自身的数值减一

> [!IMPORTANT]
>
> 对于变量自身来说，++ia和ia++都实现变量数值的加一效果，它们是等价的
>
> ia++表示先让ia的数值作为整个表达式的结果，然后再让ia自身的数值加一
>
> ++ia表示先让ia自身的数值加一，然后在作为整个表达式的结果



```java
/*
  编程实现自增减运算符的使用
*/
public class ZiBian
{
    public static void main(String[] args)
    {
    int ia = 10;
    System.out.println("ia = "+ ia);//ia=10
    //实现ia变量自身的数值加一的功能
    ia++;
    System.out.println("ia = "+ ia);//ia=11
    ++ia;
    System.out.println("ia = "+ ia);//ia=12
    }
    System.out.println("-----------------------------");
    System.out.println(ia++);        //ia=12后加加 后加一
    System.out.println("ia = "+ ia); //ia=13
    System.out.println(++ia);        //ia=14前加加 前加一
    System.out.println("ia = "+ ia); //ia=14
}
```

### 逻辑运算符

&& 表示逻辑与运算符，相当于“并且”，同真为真，一假为假。

||表示逻辑或运算符，相当于“或者”，一真为真，同假为假。

！表示逻辑非运算符，相当于“取反”，真为假，假为真。

逻辑运算符两端的操作数都是boolean类型的，结果是boolean类型的

```java
/*
   编程实现逻辑运算符的使用
*/
public class LuoJi
{
    public static void main(String[] args)
    {
    boolean b1 = true;
    boolean b2 = false;
    System.out.println("b1 = " + b1);
    System.out.println("b2 = " + b2);
    System.out.println("---------------------");
    //实现逻辑运算符的使用
    System.out.println(b1 && b2);  //并且 同真为真，一假为假 false
    System.out.println(b1 || b2);  //或者 一真为真，同假为假 true
    System.out.println(!b1);       //取反 真为假，假为真 false
    System.out.println(!b2);       //取反 真为假，假为真 true
    }
}
```

```java
/*
    编程判断是否是三位数
*/
import java.util.Scanner;
public class AnLi3
{
    public static void main(String[] args)
    {
    int b1 = 99;
    int b2 = 1000;
    System.out.println("请输入一个正整数：");
    Scanner sc =new Scanner(System.in);
    int shu =sc.nextInt();
    System.out.println("-----------------------------");
    System.out.println(b1 < shu && shu < b2);
    }
}
```

> [!IMPORTANT]
>
> 短路特性：
>
> 对于&&来说，若第一个条件为假则整个表达式一定为假，第二个条件不用判断；
>
> 对于||来说，若第一个条件为真则整个表达式一定为真，第二个条件不用判断；

```java
public class AnLi3
{
    public static void main(String[] args)
    {
    int ia = 3;
    int ib = 2;
    boolean b3 = (++ia == 3) && (++ib == 2);
    System.out.println("b3 = " + b3); //false
    System.out.println("ia = " + ia); //4
    System.out.println("ib = " + ib); //2
    System.out.println("-----------------------------"); 
    boolean b4 = (++ia == 5) || (++ib == 2);
    System.out.println("b4 = " + b4); //true
    System.out.println("ia = " + ia); //5
    System.out.println("ib = " + ib); //2
    }
}
```



### 条件运算符
