# 一. Java编程基础与程序设计

## 1. Java程序开发入门

### **1.1 计算机的体系结构**

**1.1.1基本概念**

​	计算机（computer）俗称电脑，主要由计算机硬件和软件两个部分组成。

**1.1.2常见的计算机硬件**

​	计算机的常见的硬件：CPU、内存、硬盘、显卡、键盘、鼠标、显示器、...

​		CPU：

​			- 中央处理器，计算机核心部件。

​			- 主要用于处理各种计算机的指令以及软件中的数据等。

​		内存 ：

​			- 计算机中的存储部件。

​			- 主要用于临时存放CPU访问数据的内容，CPU直接访问效率高。

​			- 容量小，一旦断电会造成数据的丢失。

​			（拓展）

​			1TB = 1024Gb、1Gb = 1024Mb、1Mb = 1024Kb、1Kb = 1024byte(字节)、1byte = 8bit(二进制位)

​			通常一个英文字母占一个字 节，一个汉字占两个字节。
​		硬盘：

​			- 计算机的存储部件。

​			- CPU不能直接访问硬盘中的数据，效率较低。

​			- 容量大，断电不会造成数据的丢失。

​		其中键盘叫做标准输入设备，显示器叫做标准输出设备。

**1.1.3常见的计算机软件**

​	计算机中常见的软件主要分为两部分：系统软件 和 应用软件。

​	系统软件主要指操作系统，主流操作系统：Windows/Unix/Linux/ios/Android。

​	应用软件主要指安装在操作系统之上的软件：QQ、微信、谷歌浏览器、...

**1.1.4计算机的体系结构**

​	使用者 → 应用软件 → 系统软件（系统软件分为：内核（Kernel）和外壳（Shell）） → 硬件设备

### 1.2 Java语言的概述

**1.2.1 Java语言的背景**

​	Java语言诞生于1995年，该语言之父是詹姆斯-高斯林，之前隶属于sun公司，现在隶属于0racle公司。

​	Java语言在编程语言排行榜占据重要的地位。

**1.2.2 Java的主要版本**

（1）Java SE(Java Platform,Standard Edition)

​		- 称之为“Java平台标准版” ，主要学习Java语言的语法规范和常见类。

（2）Java EE(Java Platform, Enterprise Edition)

​		- 称之为“Java平台企业版”，主要学习Java后台开发技术，编写B/S架构项目。

### 1.3 开发环境的搭建和使用

**1.3.1 jdk的下载和安装**

（1）下载方式

​	方式一：通过官网下载 www.oracle.com/www.sun.com

​	方式二：通过搜索下载 

（2）安装方式

​	若下载的是绿色版，则直接解压即可。

​	若下载的安装板，则直接一路点击下一步即可。

​	切记`jdk`的安装路径不要有中文！

**1.3.2 相关的概念**

​	`jdk` - Java开发工具包，只要做Java开发就需要下载和安装该软件。

​	`jre` - Java运行时环境信息，只要运行Java程序就需要下载和安装该软件。

​	`jvm` - Java虚拟机，是Java程序与计算机操作系统之间的桥梁。

​	`javac.exe` - Java语言的编译器，主要用于将Java源代码进行编译生成字节码文件。

​	`java.exe` - Java语言的解释器，主要用于启动Java虚拟机对字节码文件进行解释执行。

**1.3.3 Java程序的编写流程**

（1）新建文本文档，将文件名由`xxx.txt`修改为`xxx.java`。

（2）使用记事本的方式打开文件，编写Java代码后进行保存。

（3）启动dos窗口，切换到`xxx.java`文件所在的路径中。

（4）用`javac` `xxx.java`进行编译，生成`xxx.class`的字节码文件。

（5）使用java xxx进行解释执行，打印最终结果。

注意：

​	当文件扩展名默认不显示时的处理方式：组织 → 文件夹和搜索选项  查看 → 隐藏已知文件类型的扩展名 → 去掉勾选 → 确定

Java程序示例：

```java
public class HelloWorld/*类名*/{/*类体*/
	    public static void main/*主方法，程序入口*/(String[] args) {/*方法体*/
            System.out.println("hello world");
    }
}
```

**1.3.4 常用快捷键**

​	`ctrl+s` 保存	`ctrl+x` 剪切	`ctrl+c` 复制	`ctrl+z` 撤销	`ctrl+v` 粘贴	`ctrl+f` 查找	`ctrl+a` 全选

​	`windows+d` 回到桌面	`windows+e` 打开主文件夹	windows+l 锁屏	`windows+tab` 切换任务窗口

​	`windows+r` 打开运行，输入`cmd`后回车就可以启动dos窗口

​	`alt+tab` 切换任务

​	`ctrl+alt+delete` 启动任务管理器

​	`ctrl+shift` 切换输入法，若切换到中文后则使用shift键进行中英文切换

**1.3.5 环境变量的配置**

（1）基本概念

​	通常情况下可执行文件只能在该文件所在的路径中访问，若希望该可执行文件可以在任意路径中使用则需要将该可执行文件的路径信息配置到环境变量Path中。

（2）实现方式

​	计算机 → 右键，选择属性 → 高级系统设置 → 高级 → 环境变量 → 系统变量 → 找到Path → 将javac.exe所在的路径信息复制到Path变量值的最前面，加上英文版的分号 → 一路点击确定即可。

​	切记Path变量值原来的内容不要改变，配置完毕后重新启动dos窗口！

**1.3.6跨平台原理**

​	由于不同的操作系统中都提供了Java虚拟机进行翻译，因此同一份字节码文件可以在不同的操作系统中执行，从而赢得了“一次编译，到处运行”的美名。

## 2. Java语言的基本语法格式

### 2.1 变量和注释

**2.1.1基本概念**

​	当需要在Java程序中记录单个数据内容时，则声明一个变量即可，而声明变量的本质就是在内存空间中申请一块存储单元，由于该存储单元的数值可以改变，因此得名为”变量“。

​	由于存放数据内容的大小不同导致所需存储单元的容量不同，在Java语言中使用数据类型加以描述，为了便于下次访问还需要指定变量的名称。

**2.1.2 声明方式**

​	数据类型 变量名 = 初始值；

Java程序示例：

```java
public class VarTest {
    public static void main(String[] args) {
        //1.声明一个初始值为10元素类型为int类型的变量
		int ia = 10;
        //2.打印变量的数值 +字符串连接符，用于实现连接的功能
        System.out.println("ia = " + ia);// ia =10
        
        System.out.println("------------------------------");
        //3.变量在使用之前必须声明
        //System.out.println("sa = " + sa);//错误：找不到符号
        
        System.out.println("------------------------------");
        //4.变量在使用之前必须初始化
        //String sa;
        //System.out.println("sa = " + sa);//错误：可能尚未初始化变量sa
        
        System.out.println("------------------------------");
        String sa = "hello";
        System.out.println("sa = " + sa);// sa = hello
        
        System.out.println("------------------------------");
        //int ia =20;//错误：已在方法main(String[])中定义了变量ia
    }
}
```

**2.1.3 标识符（变量名）的命名规则**

（1）要求由字母、数字、下划线以及美元$组成，其中数字不能开头。

（2）要求不能使用Java中的关键字，所谓关键字就是,Java中用于表示特殊含义的单词。

（3）区分大小写，长度没有限制但不宜过长。（不推荐使用）

（4）尽量做到见名知意，可以是汉字，不推荐。

Java程序示例：

```java
import java.util.Scanner

public class VarIO {
    public static void main(String[] args) {
        //1.声明两个变量分别用于记录姓名和年龄
        String name;
        int age;
        //2.提示用户输入姓名和年龄并存到上述变量中
        System.out.println("请输入您的姓名和年龄:");
        Scanner sc=new Scanner(System.in);
        name =sc.next();
        age = sc.nextInt();
        //3.打印变量的数值
        System.out.println("name = " + name,"age"+ age);
    }
}
```

**2.1.4 注释**

// 表示单行注释，从//开始一直到本行末尾的所有内容都是注释。

/**/ 表示多行注释，从/ * 开始一直到 * /之间的所有内容都是注释。（不能嵌套使用！）

### 2.2数据类型

**2.2.1 基本分类**

​	在Java语言中将数据类型分为两大类：

​	（1）基本数据类型

​		`byte、short、int、long、float、double、boolean、char`

​	（2）引用数据类型

​		数组、类、接口、注解、枚举

**2.2.2 常用数据类型**

​	在日常生活中采用十进制进行数据的描述，权重：10^0、10^1、10^2、…

​	在计算机底层采用二进制进行数据的描述，权重：2^0、2^1、2^2、…

​	由于现实生活中的数据具有正负数，因此二进制中采用最高位(最左边)代表符号位若是0则代表非负数，若是1则代表负数。

2.2.3 进制之间的转换

（1）正十进制转换为二进制的方式

​	a.除2取余法，使用一进制整数不断地除以2直到商为0时将余数逆序排序即可。

​	b.拆分法，将十进制整数拆分为若干个二进制权重的和，若有该权重下面写1，否则写0。

（2）正二进制转换为十进制的方式

​	a.加权法，使用二进制中的每个数字乘以当前位的权重再累加起来。

（3）负十进制转换为二进制的方式

​	a.先将十进制的绝对值转换为二进制，进行按位取反再加1。

（4）负二进制转换为十进制的方式

​	a.先减1再按位取反，然后合并为十进制整数后添加负号。

## 3. 运算符与表达式

### 3.1运算符

**3.1.1 算数运算符**

​	+ 表示加法运算符

​	- 表示减法运算符

​	* 表示乘法运算符

​	/ 表示除法运算符

​	% 表示取模/取余运算符

Java程序示例：

```java
public class ArithmeticTest {
    public static void main(String[] args) {
		int ia =10;
        int ib =2;
        System.out.println(ia+ib);//12
        System.out.println(ia-ib);//8
        System.out.println(ia*ib);//20
        System.out.println(ia/ib);//5
        System.out.println(ia%ib);//0
        
    }
}
```

注意事项：

（1）在Java语言中两个整数相除时，结果只保留整数部分丢弃小数部分；

（2）若希望保留小数部分，则处理方式如下:

​	a.将其中任意一个操作数强转为double类型进行运算即可；

​	b.让其中任意一个操作数乘以1.0后进行运算即可；

（3）0不能做除数，0.0可以做除数但结果是无穷；

（4）)+既可以作为算术运算符也可以作为字符串连接符，区分方式如下:只要+两端的操作数中有，一个是字符串类型，则按照字符串连接符对待，结果字符串；

**3.1.2 关系/比较运算符**

​	> 表示是否大于运算符

​	>= 表示是否大于等于运算符

​	< 表示是否小于运算符

​	<= 表示是否小于等于运算符

​	== 表示是否等于运算符

​	!=  表示是否不等于运算符

​	所有以关系运算符作为最终运算的表达式结果一定是`boolean`类型，只有true和false。

Java程序示例：

```java
public class RelationTest {
    public static void main(String[] args) {
		int ia =3;
        int ib =2;
		System.out.println(ia>ib);//true
        System.out.println(ia>=ib);//true
        System.out.println(ia<ib);//false
        System.out.println(ia<=ib);//false
        System.out.println(ia==ib);//false
        System.out.println(ia!=ib);//true
    }
}
```

**3.1.3 自增减运算符**

​	++ 表示自增运算符，主要用于使得变量自身的数值加1

​	-- 表示自减运算符，主要用于使得变量自身的数值减1

Java程序示例：

```java
public class MyselfTest {
    public static void main(String[] args) {
		int ia =10;
        System.out.println("ia = "+ia);//ia =10
        a++;
        System.out.println("ia = "+ia);//ia =11
        ++a;
        System.out.println("ia = "+ia);//ia =12

        System.out.println("------------------------------");
        System.out.println(ia++);//12
        System.out.println("ia = "+ia);//13
        System.out.println(++ia);//14
        System.out.println("ia = "+ia);//14
    }
}
```

注意：

​	（1）对于变量自身来说，`++ia`和`ia++`都实现变量自身数值的加1效果，是等价的；

​	（2）`ia++`表示先让`ia`的数值作为整个表达式的结果，然后再让`ia`自身的数值加1;表示先让`ia`自身的数值加1，然后再作为整个表达式的结果;

**3.1.4 逻辑运算符**

​	&& 表示逻辑与运算符，相当于"并且”，同真为真，一假为假。

​	|| 表示逻辑或运算符相当于"或者”一真为真，同假为假。

​	! 表示逻辑非运算符，相当于"取反"，真为假，假为真。

​	逻辑运算符两端的操作数都是`boolean`类型的，结果应该是`boolean`类型的。

Java程序示例：

```java
public class LogicTest {
    public static void main(String[] args) {
		boolean b1 = true;
        boolean b2 = false;
        System.out.println(b1&&b2);//false
        System.out.println(b1||b2);//false
        System.out.println(!b1);//false
        System.out.println(!b2);//true
        
        System.out.println("------------------------------");
        int ia = 3;
        int ib = 2;
        boolean b3 = (++ia == 3) && (++ib == 2);
        System.out.println("b3 = " + b3);//false
        System.out.println("ia = " + ia);//4
        System.out.println("ib = " + ib);//2
        
        boolean b4 = (++ia == 5) || (++ib == 2);
        System.out.println("b4 = " + b4);//true
        System.out.println("ia = " + ia);//5
        System.out.println("ib = " + ib);//2
    }
}
```

短路特性（如果第一个表达式的值即可得出最后的结果，则不计算第二个表达式）：

​	对于逻辑与来说，若第一个条件为假则整个表达式一定为假，第二个条件不用判断:

​	对于逻辑或来说，若第一个条件为真则整个表达式一定为真，第二个条件不用判断;

**3.1.5 条件/三目运算符**

​	条件表达式?表达式1:表达式2

​	→ 判断条件是否成立

​		→ 若成立，则执行表达式1；

​		→ 若不成立，则执行表达式2；

Java程序示例：

```java
import java.util.Scanner

public class Test {
    public static void main(String[] args) {
		System.out.println("输入一个整数");
        Scanner sc = new Scanner(System.in);
        int number = sc.nexInt();
        System.out.println(number < 0 ? "负数" : "非负数");
    }
}
```

**3.1.6 赋值运算符**

（1）简单赋值运算符

​	= 表示赋值运算符，主要用于将=右边的数据赋值给=左边的变量，覆盖原来的数值。

（2）复合赋值

​	+=、-=、*=、……

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        int ia = 3;
        System.out.println("ia = "+ia);//3
        
        ia = 5;
        System.out.println("ia = "+ia);//5
        
        //ia = ia + 2;
        ia += 2
        System.out.println("ia = "+ia);//7
        
    }
}
```

**3.1.7 移位运算符**

​	<< 表示左移运算符，用于将数据的二进制位向左移动，右边使用0补充

​	>> 表示右移运算符，用于将数据的二进制位向右移动，左边使用符号位补

​	>>> 表示逻辑右移运算符，用于将数据的二进制位向右移动，左边使用0补充

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        // 初始化变量
        int ia = 8;    // 二进制: 0000 1000
        int ib = 2;     // 移位位数
        
        // 左移运算符 <<
        int ic = ia << ib;  // 8 << 2 = 32 (0010 0000)
        System.out.println(ia + " << " + ib + " = " + ic);
        
        // 右移运算符 >>
        int id = ia >> ib;  // 8 >> 2 = 2 (0000 0010)
        System.out.println(ia + " >> " + ib + " = " + id);
        
        // 无符号右移 >>>
        int ie = -ia >>> ib; // -8 >>> 2 = 1073741822
        System.out.println("-" + ia + " >>> " + ib + " = " + ie);
    }
}
```

**3.1.8 位运算符**

​	& 表示按位与运算符，就是按照二进制位进行与运算，同1为1，一0为0(1-真 0-假)。

​	| 表示按位或运算符，就是按照二进制位进行或运算，一1为1，同0为0。

​	~ 表示按位取反运算符，按照二进制位进行取反，1为0，0为1。

​	^ 表示按位异或运算符，按照二进制位进行异或运算，相同为0，不同为1。

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        int ia = 0b1100;    // 12 (二进制: 1100)
        int ib = 0b1010;    // 10 (二进制: 1010)
        
        // 按位与 (&)
        int ic = ia & ib;   // 1100 & 1010 = 1000 (8)
        System.out.println(ia + " & " + ib + " = " + ic);
        
        // 按位或 (|)
        int id = ia | ib;   // 1100 | 1010 = 1110 (14)
        System.out.println(ia + " | " + ib + " = " + id);
                
        // 按位取反 (~)
        int ig = ~ia;      // ~0000...00001100 = 1111...11110011 (-13)
        System.out.println("~" + ia + " = " + ig);
        
        // 按位异或 (^)
        int ie = ia ^ ib;   // 1100 ^ 1010 = 0110 (6)
        System.out.println(ia + " ^ " + ib + " = " + ie);
    }
}
```

**3.1.9 运算符的优先级**

​	a.()优先级最高

​	b.=优先级最低

​	c.算术运算符 > 移位运算符 > 关系运算符 > 位运算符 > 逻辑运算符 > 三元运算符 > 赋值运算符

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
		int a = 10, b = 5, c = 1;
		int result = a + b * c;  // 先乘后加，结果为15

		boolean x = true, y = false, z = true;
		boolean boolResult = x || y && z;  // 先与后或，结果为true

		int d = 1 << 2 + 3;  // 先加后移位，相当于1<<5，结果为32

		int e = a > b ? a : b + 10;  // 先计算b+10，再三元运算
    }
}
```

## 4. Java语言的流程控制

### 4.1 if分支结构

**4.1.1 基本概念**

​	在某些特殊场合中需要进行判断并作出选择时，就需要使用分支结构。

**4.1.2 if分支结构**

（1）语法格式

​	if(条件表达式){

​		语句块；

​	}

（2）执行流程

​	判断条件表达式是否成立

​		→若成立，则执行语句块；

​		→若不成立，则跳过语句块；

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        int ia = 10;
        
        // 最简单的if语句
        if (ia > 0) {
            System.out.println(ia + " 是正数");
        }
        
        // 只有一条语句时可以省略大括号（但不推荐）
        if (ia % 2 == 0)
            System.out.println(ia + " 是偶数");
    }
}
```

**4.1.3 if-else分支结构**

（1）语法格式

​	if(条件表达式){

​		语句块1；

​	}else{

​		语句块2；

​	}

（2）执行流程

​	判断条件表达式是否成立

​		→若成立，则执行语句块1；

​		→若不成立，则执行语句块2；

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        int ia = -5;
        
        // 标准if-else结构
        if (ia > 0) {
            System.out.println(ia + " 是正数");
        } else {
            System.out.println(ia + " 不是正数");
        }
        
        // 嵌套if-else
        if (ia > 0) {
            System.out.println(ia + " 是正数");
        } else if (ia < 0) {
            System.out.println(ia + " 是负数");
        } else {
            System.out.println(ia + " 是零");
        }
    }
}
```

**4.1.4 if-else if-else分支结构**

（1）语法格式

​	if(条件表达式1){

​		语句块1；

​	}else if(条件表达式2){

​		语句块2；

​	}

​	……

​	else{

​		语句块n；

​	}

（2）执行流程

​	判断条件表达式1是否成立

​		→若成立，则执行语句块1；

​		→若不成立，则判断条件表达式2是否成立

​			→若成立，则执行语句块2；

​			→若不成立，则执行语句块n；

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        int ia = 25;
        
        // 使用逻辑运算符组合多个条件
        if (ia > 0 && ia < 10) {
            System.out.println(ia + " 是一位数正数");
        } else if (ia >= 10 && ia < 100) {
            System.out.println(ia + " 是两位数正数");
        } else if (ia >= 100 || ia <= -100) {
            System.out.println(ia + " 是三位数或更大");
        } else {
            System.out.println(ia + " 是负数或特殊值");
        }
    }
}
```

### 4.2 循环结构

**4.2.1 基本概念**

​	在某些特殊场合中需要重复执行一段代码时，借助循环结构加以处理。

**4.2.2 for循环**

（1）语法格式

​	for(初始化表达式；条件表达式；修改初始值表达式){

​		循环体；

​	}

（2）执行流程

​	执行初始化表达式→判断条件表达式是否成立

​		→若成立，则执行循环体→修改初始值表达式→判断条件表达式是否成立

​		→若不成立，则循环结束

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        // 打印0到4的数字
        for (int ia = 0; ia < 5; ia++) {
            System.out.println("当前值: " + ia);
        }
        
        // 循环可以省略大括号（单条语句时，但不推荐）
        for (int ib = 5; ib > 0; ib--)
            System.out.println("倒计时: " + ib);
    }
}
```

**4.2.3 break和continue关键字**

​	break关键字用于循环中表示跳出当前循环；

​	continue关键字用于循环中表示结束本次循环继续下一次循环；

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        // 在for循环中使用break
        for (int ia = 0; ia < 10; ia++) {
            if (ia == 5) {
                System.out.println("遇到5，跳出循环");
                break;
            }
            System.out.println("当前值: " + ia);
        }
        // 在for循环中使用continue
        for (int ia = 0; ia < 10; ia++) {
            if (ia % 2 != 0) {
                continue; // 跳过本次循环的剩余部分
            }
            System.out.println("偶数: " + ia);
        }
    }
}
```

4.2.4 特殊的循环

​	for(;;) - 这种没有循环条件的循环叫做无限循环，俗称"死循环"。

​	通常与break关键字搭配使用。

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        // for(;;) 实现的死循环
        for (;;) {
            System.out.println("这是一个死循环");
            if (Math.random() > 0.8) {  // 80%概率继续循环
                System.out.println("随机数大于0.8，退出");
                break;
            }
        }
    }
}
```

**4.2.5 双重循环**

（1）语法格式

​	for(初始化表达式1；条件表达式1；修改初始值表达式1){

​		for(初始化表达式2；条件表达式2；修改初始值表达式2){

​			循环体；

​		}

​	}

（2）执行流程

​	执行初始化表达式1→判断条件表达式1是否成立

​		→若成立，则执行表达式2→判断条件表达式2是否成立

​			→若成立，则执行循环体→执行表达式2→判断条件表达式2是否成立

​			→若不成立，则内层循环结束→执行表达式1→判断条件表达式1是否成立

​		→若不成立，则外层循环结束

（3）注意事项

​	a.外层循环变量动一下，则内层循环变量跑一圈；

​	b.当需要打印多行多列的数据内容时，可以使用双重for循环；

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        // 打印九九乘法表
        for (int ia = 1; ia <= 9; ia++) {
            for (int ib = 1; ib <= ia; ib++) {
                System.out.print(ib + "×" + ia + "=" + (ia * ib) + "\t");
            }
            System.out.println();
        }
    }
}
```

**4.2.6 while循环**

（1）语法格式

​	while（条件表达式）{

​		循环体；

​	}

（2）执行流程

​	判断条件表达式是否成立

​		→若成立，则执行循环体→判断条件表达式是否成立

​		→若不成立，则循环结束

（3）注意事项

​	a. while循环和for循环可以完全互换;

​	b. while(true)和for(;;)表示无限循环;

​	c. while循环主要用于明确循环条件但不明确循环次数的场合中;for循环主要用于明确循环次数或范围的场合中;

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        int ia = 0;
        
        // 基本的while循环
        while (ia < 5) {
            System.out.println("Count is: " + ia);
            count++;
        }
        
        System.out.println("循环结束");
    }
}
```

### 4.3 switch-case分支结构

**4.3.1 switch-case分支结构**

（1）语法格式

switch(变量/表达式){

​		case 字面值1：语句块1；break;

​		case 字面值2：语句块2；break;

​		……

​		default:语句块n;

​	}

（2）执行流程

​	计算变量/表达式的数值→判断是否匹配字面值1

​		→若匹配，则执行语句块1→执行break跳出当前结构

​		→若不匹配，则判断是否匹配字面值2

​			→若匹配，则执行语句块2→执行break跳出当前结构

​			→若不匹配，则执行语句块n

（3）注意事项

​	switch()中支持的数据类型有：byte、short、int、char，jdk1.5支持枚举类型，jdk1.7支持String类型。

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        int ia = 2;
        
        switch (ia) {
            case 1:
                System.out.println("ia 等于 1");
                break;
            case 2:
                System.out.println("ia 等于 2");
                break;
            case 3:
                System.out.println("ia 等于 3");
                break;
            default:
                System.out.println("ia 不是 1、2 或 3");
        }
    }
}
```

## 5. Java语言的数组声明与应用

### 5.1一维数组

**5.1.1 基本概念**

​	一维数组的本质就是在内存中申请一段连续的存储单元。

​	数组元素 - 主要指存放到数组中的数据内容。

​	数组长度 - 主要指数组的容量或最多可存放的元素个数。

​	数组下标 - 主要指元素 编号，从0开始可以取到长度-1。

**5.1.2 声明方式**
（1）语法格式

​	数据类型[] 数组名称 = new 数据类型[数组的长度];

（2）元素的初始化

​	数据类型[] 数组名称 = {元素值1，元素值2，……}

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
        // 方式1: 声明后初始化
        int[] ia1;
        ia1 = new int[3];  // 包含3个元素，默认值0
        
        // 方式2: 声明时初始化
        double[] da1 = new double[5];  // 默认值0.0
        
        // 方式3: 直接赋值初始化
        String[] sa1 = {"Java", "Python", "C++"};
        
        // 方式4: 匿名数组
        char[] ca1 = new char[]{'A', 'B', 'C'};
    }
}
```

**5.1.3 数组的增删改查操作**

Java程序示例：

```java
import java.util.Arrays;

public class Test {
    public static void main(String[] args) {
 // 初始化数组
        int[] ia = new int[5];
        System.out.println("初始数组: " + Arrays.toString(ia));//Arrays.toString方法它会返回一个字符串，格式为[元素1, 元素2, ..., 元素n]
        
        // 填充初始值
        for (int i = 0; i < ia.length; i++) {
            ia[i] = i + 1;
        }
        System.out.println("填充后: " + Arrays.toString(ia)); // [1, 2, 3, 4, 5]
        
        // 1. 增 - 添加元素
        ia = addElement(ia, 6);
        System.out.println("添加后: " + Arrays.toString(ia)); // [1, 2, 3, 4, 5, 6]
        
        // 2. 删 - 删除元素
        ia = removeElement(ia, 2);
        System.out.println("删除后: " + Arrays.toString(ia)); // [1, 2, 4, 5, 6]
        
        // 3. 改 - 修改元素
        updateElement(ia, 1, 99);
        System.out.println("修改后: " + Arrays.toString(ia)); // [1, 99, 4, 5, 6]
        
        // 4. 查 - 查找元素
        int index = findElement(ia, 5);
        System.out.println("元素5的索引: " + index); // 3
    }
    
    // 添加元素
    public static int[] addElement(int[] arr, int element) {
        int[] newArr = new int[arr.length + 1];
        System.arraycopy(arr, 0, newArr, 0, arr.length);
        newArr[newArr.length - 1] = element;
        return newArr;
    }
    
    // 删除元素
    public static int[] removeElement(int[] arr, int index) {
        if (index < 0 || index >= arr.length) {
            return arr;
        }
        int[] newArr = new int[arr.length - 1];
        System.arraycopy(arr, 0, newArr, 0, index);
        System.arraycopy(arr, index + 1, newArr, index, arr.length - index - 1);
        return newArr;
    }
    
    // 修改元素
    public static void updateElement(int[] arr, int index, int newValue) {
        if (index >= 0 && index < arr.length) {
            arr[index] = newValue;
        }
    }
    
    // 查找元素
    public static int findElement(int[] arr, int target) {
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == target) {
                return i;
            }
        }
        return -1;
    }
}
```

### 5.2 二维数组

**5.2.1 基本概念**

​	二维数组本质上就是由多个一维数组组成的数组，也就是说二维数组中的每个元素都是一个一维数组，而一维数组中的每个元素才是数据内容。

**5.2.2 声明方式**

（1）语法格式

​	数据类型 [ ] [ ] 数组名字 = new 数据类型 [行数] [列数]；

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
		// 三种声明方式
		int[][] ia1;      // 推荐方式
		int[] ia2[];      // 合法但不推荐
		int ia3[][];      // C语言风格，不推荐
    }
}
```

（2）元素的初始化

​	数据类型 [ ] [ ] 数组名字 = {{元素值1，元素值2，……}，……}

Java程序示例：

```java
public class Test {
    public static void main(String[] args) {
    	// 方式1: 指定行数和列数
		int[][] iaMatrix1 = new int[3][4]; // 3行4列，默认值0

        // 方式2: 直接初始化
        int[][] iaMatrix2 = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        // 方式3: 不规则数组（每行长度不同）
        int[][] iaMatrix3 = new int[3][];
        iaMatrix3[0] = new int[2]; // 第一行2列
        iaMatrix3[1] = new int[3]; // 第二行3列
        iaMatrix3[2] = new int[1]; // 第三行1列
    }
}
```

