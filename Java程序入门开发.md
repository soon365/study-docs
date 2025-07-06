# 					Java程序入门开发

### 一、计算机的基本概念

#### 	  基本概念：

​	计算机是一种广泛应用于各个领域的设备，主要有计算机硬件和计算机软件组成。

#### 	计算机硬件：

​		 CPU - 中央处理器，是计算机中最合性的部件，相当于人的大脑。

​			     - 主要用于处理各种计算机的指令以及软件中的数据等

​		 内存 - 是计算机内部的存储部件

​			     - 主要用于临时存放CPU访问的数据内容，CPU直接访问且效率更高

​			     - 容量小，断电容易造成数据丢失

​		 硬盘 - 是计算机的存储部件。

​			     - CPU不能直接访问硬盘中的数据，因此效率比较低。

​			     - 容量大，若断电不会造成数据的丢失。

##### Tip：

​		1Tb = 1024Gb

​		1Gb = 1024Mb

​		1Mb = 1024Kb

​		1Kb = 1024byte（字节）	通常一个英文字母占用1个字节，一个汉字占用2个字节

​		1byte = 8bit（二进制位）	在计算机的底层识别0和1组成的二进制序列

#### 	常见的计算机软件

​		计算中常见的软件主要分为两部分:系统软件和应用软件。

​		其中系统软件主要指操作系统，主流操作系统:Windows/Unix/Linux/ios/Android。

​		其中应用软件主要指安装在操作系统之上的软件:QQ、迅雷、火狐浏览器。

​		![image-20250628161657920](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20250628161657920.png)

#### 	计算机的体系结构

![image-20250628154734665](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20250628154734665.png)

##### 			使用者 => 应用软件 => 系统软件 => 硬件设备

##### 			=> 其中系统软件分为:内核(Kerne1)和外壳(She11)



### 二、Java语言概述

#### Java语言的主要版本

Java SE (Java Platform, Standard Edition)

​	-称之为“Java平台标准版”，主要学习Java语言的语法规范和常见类。

Java EE (Java Platform, Enterprise Edition)

​	-称之为“Java平台企业版”，主要学习Java后台开发技术，编写B/S架构项目。

Java ME (Java Platform, Micro Edition)

​	-称之为Java 平台微型版，随着Android平台的迅速普及已经走向淘汰。

#### 开发环境的搭建和使用(重点)

#####   jdk的下载和安装

下载方式：

​	方式一:通过官网下载www.sun.com/www.oracle.com

​	方式二:通过搜索下载www.baidu.com/www.sogou.com

安装方式：

​	若下载的是绿色版，则直接解压即可。

​	若下载的是安装版，则直接一路点击下一步即可。

​	切记 jdk 的安装路径中不要有中文！

##### 相关的概念

​	jdk - Java开发工具包，只要做Java开发就需要下载和安装该软件。

​	jre - Java运行时环境信息，只要运行Java程序就需要下载和安装该软件。

​	jvm - Java虚拟机，是Java程序与计算机操作系统之间的桥梁。

​	javac.exe - Java语言的编译器，主要用于将Java源代码进行编译生成字节码文件。

​	java.exe - Java语言的解释器，主要用于启动Java虚拟机对字节码文件进行解释执行。

##### Java程序的编写流程

​	新建文本文档，将文件名由xxx.txt修改为xxx.java；

​	使用记事本的方式打开文件，编写Java代码后进行保存；

​	启动dos窗口，切换到xxx.java文件所在的路径中；

​	使用javac xxx.java进行编译，生成xxx.class的字节码文件；

​	使用java xxx进行解释执行，打印最终结果；

#### 第一条命令Hello World

```
public class HelloWorld {

	public static void main(String[]args) {
	
		System.out.println("Hello World!");

	}

}
```

**`public class HelloWorld`**
- 定义了一个名为`HelloWorld`的公共类
- 在Java中，每个程序至少需要一个类，且类名必须与文件名一致（这里是`HelloWorld.java`）

- 就像给你的笔记本取个名字叫"HelloWorld"
- 在Java中，每个程序都需要这样一个"笔记本"来写内容

**public static void main(String[] args)`**

- 这是Java程序的入口点（主方法）
- `public`表示该方法可以被外部访问
- `static`表示该方法属于类而不需要创建实例
- `void`表示该方法不返回任何值
- `main`是方法名
- `String[] args`是命令行参数数组

- 也相当于这是电脑开始读你笔记的"起点"
- 就像书本的第一页，电脑从这里开始执行你的指令

**`System.out.println("Hello World!");`**

- `System.out`是标准输出流，相当于电脑的"嘴巴"
- `println`方法用于打印字符串并换行，让电脑"说"出东西
- `"Hello World!"`是要输出的字符串，让电脑说的具体内容

#### 常用的快捷键

​	ctrl + s 保存	ctrl + x剪切	ctrl + c 复制	ctrl + z 撤销

​	ctrl + v 粘贴	ctrl + a全选	ctrl + f 查找

​	windows + d 	回到桌面	windows + e 	打开计算机	windows + l 	锁屏

​	windows + r 	打开运行输入cmd后回车就可以启动dos窗口

​	windows + tab     切换任务

​	alt + tab 		切换任务

​	ctrl + alt + delete 	启动任务管理器

​	ctrl + shift 	    切换输入法，若切换到中文后则使用shift键进行中英文切换



# Java语言的基本语法格式

### 一、Java变量与注释

#### 代码案例：

```
/**
 * 小卖部库存管理系统（完整八大数据类型演示）
 * 日期：2025-6-29
 */
public class StoreManagement {
    public static void main(String[] args) {
        // ============== 八大数据类型变量 ==============
        // 1. 整数类型
        byte dailyLimit = 100;          // 每日限购量（-128~127）
        short shelfNumber = 205;        // 货架编号（-32768~32767）
        int stock = 50;                 // 库存数量（最常用整数类型）
        long barcode = 690123456789L;   // 商品条形码（注意L后缀）
        
        // 2. 浮点类型
        float cost = 2.5f;              // 成本价（单精度，注意f后缀）
        double price = 3.5;             // 零售价（双精度，默认）
        
        // 3. 字符类型
        char category = 'B';            // 商品分类（B=饮料）
        
        // 4. 布尔类型
        boolean isOnSale = true;        // 促销状态
        
        // 5. 字符串类型（虽然不是基本类型，但常用）
        String productName = "可口可乐";
        
        // ============== 打印信息 ==============
        System.out.println("=== 商品完整信息 ===");
        System.out.println("名称：" + productName);
        System.out.println("分类：" + category + "类");
        System.out.println("货架编号：" + shelfNumber);
        System.out.println("条形码：" + barcode);
        System.out.println("成本价：" + cost + "元");
        System.out.println("零售价：" + price + "元");
        System.out.println("库存：" + stock + "瓶");
        System.out.println("每日限购：" + dailyLimit + "瓶");
        System.out.println("促销中：" + (isOnSale ? "是" : "否"));
    }
}
```

#### 什么是变量？

​	当需要在Java程序中记录单个数据内容时，则声明一个变量即可，而声明变量的本质就是在内存空间中申

请一块存储单元，由于该存储单元的数值可以改变，因此得名为"变量。

​	由于存放数据内容的大小不同导致所需存储单元的容量不同，在Java语言中使用数据类型加以描述，为了

便于下次访问还需要指定变量的名称。

就像上述案例中小卖部的储物格，每个格子有：

- 名字（变量名）
- 存放的东西（值）
- 只能放特定类型的东西（数据类型）

#### 变量的声明：

##### 	数据类型 变量名 = 初始值； 

#### 八大基本变量类型：

|   类型    |              例子              |             说明              |            生活比喻            |
| :-------: | :----------------------------: | :---------------------------: | :----------------------------: |
|   `int`   |         `int age = 10`         |      存储整数（最常用）       |      商品库存数量（50瓶）      |
|  `float`  |      `float cost = 2.5f`       | 存储小数（单精度，需加f后缀） |     商品成本价（精确到角）     |
| `double`  |      `double price = 3.5`      |   存储小数（双精度，默认）    |      商品售价（精确到分）      |
| `boolean` |    `boolean isOpen = true`     |        存储true/false         |   店铺是否营业、商品是否促销   |
|  `byte`   |    `byte smallStock = 100`     |     极小整数（-128~127）      |      每日限量商品剩余数量      |
|  `short`  |     `short shelfNo = 302`      |   较小整数（-3.2万~3.2万）    |          商品货架编号          |
|  `long`   | `long barcode = 690123456789L` |     极大整数（需加L后缀）     |           商品条形码           |
|  `char`   |     `char category = 'A'`      |   存储单个字符（用单引号）    | 商品分类代号（A=饮料，B=零食） |

#### 变量命名规则

- 变量不能重复声明
- 不能以数字开头：`1product` → `product1` 
- 不能是Java关键字，比如：public、static、class、……
- 区分大小写：`age`和`Age`是不同变量
- 推荐驼峰命名法：`productName`（首字母小写，后面单词首字母大写）

#### Java注释：

##### 单行注释

```
// 这是单行注释，解释下面代码的作用
int stock = 50; // 也可以写在代码后面
```

##### 多行注释

```
/*
这是多行注释
可以用来写较长的说明
比如这个库存管理系统的功能介绍
*/
```

##### 文档注释（特殊的多行注释）

```
/**
 * 这是文档注释
 * 通常用于说明类或方法的功能
 * 可以用工具自动生成文档
 */
```



### 二、变量的输入和输出

#### 代码案例：

```
/*
	编程实现姓名和年龄的输入输出
*/
import java.util.Scanner;
public class VarIOTest {
    public static void main(String[] args) {
        String name;
        int age;

        System.out.println("请输入您的姓名和年龄:”);

        Scanner sc =newScanner(System.in);

        name = sc.next();

        age = sc.nextInt();

        System.out.println("name =" + name);

        System.out.println("age =" + age);

    }
}
```

#### 代码讲解：

#### 导入Scanner类

```
import java.util.Scanner;
```

- 这行代码告诉Java我们要使用`Scanner`工具
- `Scanner`就像是一个"扫描仪"，可以帮助我们读取用户的键盘输入
- 必须放在程序的最前面（除了注释）

#### 主方法框架

```
public class VarIOTest {
    public static void main(String[] args) {
        // 程序内容
    }
}
```

- 每个Java程序都需要一个类（这里是`VarIOTest`）
- `main`方法是程序的入口，代码从这里开始执行

#### 变量声明

```
String name;  // 用于存储姓名
int age;      // 用于存储年龄
```

- `String`是字符串类型，适合存储文本（如姓名）
- `int`是整数类型，适合存储数字（如年龄）

#### 用户输入处理

```
System.out.println("请输入您的姓名和年龄:");
Scanner sc = new Scanner(System.in);
name = sc.next();      // 读取字符串
age = sc.nextInt();    // 读取整数
```

先提示用户输入

创建`Scanner`对象，绑定到系统输入（键盘）

`sc.next()`读取用户输入的下一个单词（直到空格）

`sc.nextInt()`读取用户输入的下一个整数

#### 输出结果

```
System.out.println("name = " + name);
System.out.println("age = " + age);
```

- 将变量值与描述文字连接起来输出
- `+`在这里用于字符串连接

### 进制转换

​	常见的进制有：二、八、十进制和十六进制。

​	其中十六进制有些特殊，由1~9,a~f表示，a到f代表10到15。

​	在日常生活中采用十进制进行数据的描述，权重:10^0、10^1、10^2、……

​	在计算机底层采用二进制进行数据的描述，权重:2^0、2^1、2^2、……

​	由于现实生活中的数据具有正负数，因此二进制中采用最高位（最左边）代表符号位若是0则代表非负数，若是1则代表负数。

​	如：

​			10^3	10^2	10^1	10^0

​			  千	      百	    十	     个

十进制整数：    1               2	      3	       4

正十进制转换为二进制的方式

​	a.除2取余法，使用十进制整数不断地除以2直到商为0时将余数逆序排序即可

​	b.拆分法，将十进制整数拆分为若干个二进制权重的和，若有该权重下面写1，否则写0

​	如:
​	45 = 32 + 8 + 4 + 1

​		128	64	32	16	8	4	2	1

​		  0	   0	   1	  0	 1	1	0	1	=>	0010  1101

正二进制转换为十进制的方式
	a.加权法，使用二进制中的每个数字乘以当前位的权重再累加起来。

​	如:

​		0010 11001   =  0×2^7  + 0×2^6  + 1×2^5  + 0×2^4  + 1×2^3  + 1×2^2  + 0×2^1  + 1×2^0
​					=  0  +  0  +  32  +  0  +  8  +  4  +  0  +  1

​					=45

负十进制转换为二进制的方式

​	a.先将十进制的绝对值转换为二进制，进行按位取反再加1。

​	如：

​		-45  =>  绝对值转换为二进制：0010  1101

​			=>  按位取反：		   1101  0010

​			=>  加1：			     1101  0011

​		-45 + 45 = 0

​			-45：1101  0011

​			 45：0010  1101  +

​		=======================

​		    	 1  0000 0000（最高位溢出，丢弃）=>  0

负二进制转换为十进制的方式

​	a.先减1再按位取反，然后合并为十进制整数后添加符号。

​	如：

​		1101  0011    =>  先减1：		1101  0010

​					=>  按位取反：	  0010  1101

​					=>  合并为十进制：   45

​					=>  添加负号：	  -45	



# 运算符与表达式

### 一、Java中的算数运算符

#### 代码案例：

```java
public class ArithmeticTest {

	public static void main (String[] args) {
	
		//1.声明两个int类型的变量ia和ib，分别初始化为10和2
		//int ia=10，ib=2;//声明两个int类型的变量，不推荐使用
		int ia = 10;
		int ib =2;
		
		//2.使用算术运算符进行计算
		//表示计算ia与ib的和赋值给变量ic,
		// 其中ia+ib这个整体叫做 表达式，ia和ib叫做操作数，+叫做操作/运算符
		int ic = ia + ib;
		System.out.println("ic ="+ ic);//ic = 12
		System.out.println(ia + ib);//12
		System.out.println(ia - ib);//8
		System.out.println(ia * ib);//20
		System.out.println(ia / ib);//5
		System.out.println(ia % ib);//0
		
		System.out.println("---------------------");
		//3.算术运算符的注意事项
		ia = 5;
		System.out.println(ia / ib);
        //2//希望保留小数部分
        System.out.printIn((double)ia / ib);//2.5
        System.out.printIn(ia/(double)ib);//2.5
        System.out.println((double)(ia / ib));//2.0
        System.out.println(1.0*ia / ib);//2.5 推荐该方式
	}
}
```

#### 算术运算符：

​	`+`  表示加法运算符	`-`   表示加法运算符	`*`  表示加法运算符

​	`/`  表示加法运算符	`%`  表示取模/取余运算符

#### 运算讲解：

```
int ia = 10;  // 第一个数字，值为10
int ib = 2;   // 第二个数字，值为2
System.out.println(ia + ib); // 10 + 2 = 12
System.out.println(ia - ib); // 10 - 2 = 8
System.out.println(ia * ib); // 10 × 2 = 20
System.out.println(ia / ib); // 10 ÷ 2 = 5
System.out.println(ia % ib); // 10 ÷ 2 余数是0
```

|   运算   |  代码写法   | 结果 |    说明     |
| :------: | :---------: | :--: | :---------: |
|   加法   |  `ia + ib`  |  12  |    10+2     |
|   减法   |  `ia - ib`  |  8   |    10-2     |
|   乘法   |  `ia * ib`  |  20  |    10×2     |
|   除法   |  `ia / ib`  |  5   |    10÷2     |
|   取余   |  `ia % ib`  |  0   |   10÷2余0   |
| 小数除法 | `1.0*ia/ib` | 2.5  | 5÷2保留小数 |

#### 注意事项:

（1）在Java语言中两个整数相除时，结果只保留整数部分丢弃小数部分；

（2）若希望保留小数部分，则处理方式如下:

​	a.将其中任意一个操作数强转为double类型进行运算即可；

​	b.让其中任意一个操作数乘以1.0后进行运算即可(推荐)；

（3）`0`和`0.0`作为除数的效果 编译ok，运行发生`ArithmeticException` 算术异常



### 实现时间的转换和打印

#### 代码案例：

```Java
import java.util.Scanner;

public class TimeArithmetic {

	public static void main(String[] args) {
	
	//1.提示用户输入整数类型的秒数并使用变量记录
	System.out.println("请输入一个整数类型的秒数:Scanner sc = new Scanner(System.in);
	int number =sc.nextInt();
	
	//2.将秒数转换为时分秒并使用变量单独记录
	//3666秒 => 1小时1分钟6秒钟
	//3666 / 3600 = 1 小时	3666 % 3600 = 66 / 60 = 1分钟
	//3666 % 60 = 6秒钟
	int hour = number / 3600;	//拆分小时数
	int minute = number % 3600 / 60;	//拆分小时数
	int second = number % 60;	//拆分秒数
	
	//3.打印最终的转换结果
	System.out.println(number +"秒拆分为:" + hour + "时” + minute +"分" + second +"秒”);
	
	//4.+作为算术运算符和字符串连接符的区别
	System.out.println("" + hour + minute +second);		//116
	System.out.println(hour + "" + minute +second);		//116
	System.out.println(hour + minute + "" + second);	//26
	System.out.println(hour + minute + second + "");	//8
	System.out.println(hour + (minute +second) + "");	//8
	System.out.println(hour + minute + (second + ""));	//26
	}
} 
```

#### 注意事项：

+   `+` 既可以作为算术运算符也可以作为字符串连接符，区分方式如下:

​	只要 `+` 两端的操作数中有一个是字符串类型，则按照字符串连接符对待，结果字符串



### 二、关系运算符

#### 代码案例：

```Java
public class RelationTest {
	public static void main (String[] args) {
        int ia = 3;
        int ib = 2;
        System.out.println("ia = " + ia);//ia=3
       	System.out.println("ib = " + ib); //ib=2
        System.out.println("-----------------------");
        //使用关系运算符进行比较并打印结果
        System.out.println(ia > ib);	//true
        System.out.println(ia >= ib);	//true	大于等于表示大于或者等于
        System.out.println(ia < ib);	//false
        System.out.println(ia <= ib);	//false
        System.out.println(ia == ib);	//false
        System.out.println(ia != ib);	//true
	}
}
```

#### 关系运算符：

​	`>`  表示是否大于运算符	`>=`   表示是否大于等于运算符	`<`  表示是否小于运算符

​	`<=`  表示小于等于运算符	`==`  表示是否等于运算符	`!=` 表示是否不等于运算符

​	注意：

+ 所有以关系运算符作为最终运算的表达式结果一定是`boolean`类型，只有`true`和`false`。



### 三、自增减运算符

#### 代码案例：

```Java
/*
编程实现自增减运算符的使用
*/
    public class MyselfTest {
        public static void main(String[] args) {
            int ia = 10;
            System.out.println("ia = " + ia);//ia= 10
            //实现变量ia自身的数值加1的功能
            ia++;
			System.out.println("ia = " + ia);//ia=11
            //实现变量ia自身的数值加1的功能
            ++ia;
            System.out.println("ia = " + ia);//ia = 12
            System.out.println("------------------------------");
            System.out.println(ia++);			//12
            System.out.println("ia = " + ia);	//13
            System.out.println(++ia);			//14
            System.out.println("ia = " + ia);	//14
        }
    }
```

​	`+`表示加法运算符	`-`表示减法运算符

​	`++`表示自增运算符	主要用于使得变量自身的数值加1

​	`--`表示自减运算符	主要用于使得变量自身的数值减1

​	注意:

+ 对于变量自身来说，`++ia` 和 `ia++` 都实现变量自身数值的加1效果，是等价的；

+ `ia++` 表示先让ia的数值作为整个表达式的结果，然后再让`ia`自身的数值加1；



### 三、逻辑运算符

#### 代码案例：

```java
/*
	编程实现逻辑运算符的使用
*/
public class LogicTest {
    public static void main(String[] args) {
        
        boolean b1 = true;
        boolean b2 = false;
        System.out.println("b1 = " + b1);	//b1 = true
        System.out.println("b2 = " + b2);	//b2 = false
        
        System.out.println("------------------------------");
        //实现逻辑运算符的使用
        System.out.println(b1 && b2);	//false
        System.out.println(b1 || b2);	//true
        System.out.println(!b1);	//false
        System.out.println(!b2);	//true
        
        System.out.println("------------------------------");
        //测试一下逻辑运算符的短路特性
        int ia = 3;
        int ib = 2;
        boolean b3 = ( ++ia == 3 ) && ( ++ib == 2 );
        System.out.println("b3 = " + b3);	//false
        System.out.println("ia = " + ia);	//4
        System.out.println("ib = " + ib);	//2
        
        boolean b4 = (++ia == 5) || (++ib == 2);
        System.out.println("b3 = " + b3);	//true
        System.out.println("ia = " + ia);	//5
        System.out.println("ib = " + ib);	//3
    }
}
```

​	`&&`逻辑与运算符	相当于”并且“，同真为真，一假为假。

​	`||`逻辑或运算符	相当于"或者“，一真为真，同假为假。

​	`!`逻辑非运算符	   相当于”取反“，真为假，假为真。

​	注意：

+ 逻辑运算符两端的操作数都是`boolean`类型的，结果应该是`boolean`类型的。



### 四、条件运算符（三目运算符）

#### 代码案例：

```java
/*
	编程使用关系运算符进行判断并打印
*/
import java.util.Scanner;

   public class RelationJudgeTest {
   	
       public static void main(String[] args) {
           //1.提示用户输入一个整数并使用变量记录
           System.out.printf("请输入一个整数：");
           Scanner sc = new Scanner(System.in);
           int number = sc.nextInt();
           
           //2.使用关系运算符进行判断并打印
           System.out.printIn(number < 0）;
           System.out.printIn(number < 0 ? "负数":"非负数");
    }
}
```

运算符结构：

​	条件表达式 ? 表达式1: 表达式2

​	=>判断条件表达式是否成立

​		=>若成立，则执行表达式1;

​		=>若不成立，则执行表达式2;



### 五、赋值运算符

#### 代码案例：

```java
/*
	编程实现赋值运算符的使用
*/
public class AssignTest {
    
    public static void main(String[] args) {
       
        int ia = 3;
        System.out.println("ia = " + ia);	//ia =3
        
        System.out.println("------------------------------");
        //使用简单赋值运算符
        ia =5
		System.out.println("ia = " + ia);	//ia=5
        
        System.out.println("------------------------------");
        //使用复合赋值运算符
        ia = ia + 2;
        System.out.println("ia = " + ia);	//ia =7
    }
}
```

##### 简单赋值

​	`=`表示赋值运算符，主要用于将=右边的数据赋值给=左边的变量，覆盖原来的数值.

如：

​	`ia=2`；- 表示使用数据2给变量`ia`赋值，覆盖该变量`ia`原来的数值

##### 笔试题：

​	`ia == 2`；- 判断`ia`的数值是否等于2

​	`2 == ia`；- 判断2是否等于`ia`的数值，结果与上述方式等价，但推荐该方式

​	`ia = 2`;     - 将数据2赋值给变量`ia`，覆盖原来的数值
​	`2 = ia`;     - 编译报错

##### 复合赋值：

​	`+=`	`-=`	`*=`	……

如:

​	`int ia = 2`;

​	`ia = ia + 3`;	从结果上等价于:   `ia += 3`;

##### 常用运算符的优先级：

![image-20250630201750085](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20250630201750085.png)

+ ()的优先级极高；
+ =的优先级极低；
+ 若实在不确定运算符的优先级，则可以借助()加以确定；



### 六、移位运算符

​	`<<`表示左移运算符，用于将数据的二进制位向左移动，右边使用0补充；

​	`>>`表示右移运算符，用于将数据的二进制位向右移动，左边使用符号位补充；

​	`>>>`表示逻辑右移运算符，用于将数据的二进制位向右移动，左边使用0补充；



### 七、位运算符

#### 代码案例：

```java
/*
	编程实现位运算符的使用
*/
public class TestBit {
    
    public static void main(String[] args) {
       
        byte b1= 11;
        byte b2 = 13;
        
       System.out.println("bl = " + b1);	//b1 = 11
       System.out.println("b2 = " + b2);	//b2 = 13
        
       System.out.println("------------------------------");
       //11:0000 1011
       //13:0000 1101
       System.out.println(bl & b2);	//0000 1001 => 9
       System.out.println(bl | b2);	//0000 1111 => 15
       System.out.println(bl ^ b2);	//0000 1001 => 6
       //0011 1011<=111 0100 <= 1111 0011 <= 0000 1100 => 12 => 12
       System.out.println(~bl);
    }
}
```

​	`&`  表示按位与运算符，就是按照二进制位进行与运算，同1为1，一 0 为 0 (1-真 0-假)；

​	`|`  表示按位或运算符，就是按照二进制位进行或运算，一1为1，同0为0；

​	`~`  表示按位取反运算符，按照二进制位进行取反，1为0，0为1；

​	`^`  表示按位异或运算符，按照二进制位进行异或运算，相同为0，不同为1；



# Java语言的流程控制

### 一、分支结构

### if分支结构

#### 代码案例

```java
public class IfTest {
    
    public static void main(String[]  args) {
        //1.提示用户输入年龄信息并使用变量记录
        System.out.println("请输入您的年龄：");
        Scanner sc =newScanner(System.in);
        int age = sc.nextInt();
        
        //2.使用if分支结构判断是否成年并给出对应的提示
        if(age >= 18) {
            System.out.println("开心地浏览起了网页...");
        }
        
        //3.无论是否成年都打印一句话
        System.out.println("无奈地回家了!");
    }
}
```

##### 基本概念：

+ 在某些特殊场合中需要进行判断并作出选择时，就需要使用分支结构。

##### 语法结构：

​	if (条件表达式) {

​		语句块;

​	}

##### 执行流程：

​	判断条件表达式是否成立

​		=> 若成立，则执行语句块；

​		=> 若不成立，则跳过语句块；

### if-else分支结构

#### 代码案例

```java
public class IfTest {
    
    public static void main(Stringl args) {
            //1.提示用户输入考试成绩并使用变量记录
            System.out.println("请输入您的考试成绩:");
            Scanner sc =newScanner(System.in);
            int score =sc.nextInt();

            //2.使用if-else分支结构判断是否及格并给出对应的提示
            if(score >=60){
                System.out.println("恭喜您考试通过了!");
            }
            }else {
                System.out.println("下学期来补考吧!");
            //3.打印一句经典语录
            System.out.println("世界上最遥远的距离不是生与死而是你在if我在else,看似相交却又永远分离!");
    }
}
```

##### 语法格式：

​	if (条件表达式) {

​		语句块1;

​	}else{

​		语句块2;

​	}

##### 执行流程：

​	判断条件表达式是否成立

​		=> 若成立，则执行语句块1；

​		=> 若不成立，则执行`else`语句块2；

### if-else  if-else分支结构

#### 代码案例

```java
import java.util.Scanner;

public class IfElseifElseTest {
    
    public static void main(Stringl args) {
        //1.提示用户输入身份信息并使用变量记录
        System.out.println("请输入您的身份信息: ");
        Scanner sc = new Scanner(System.in);
        String str = sc.next();
        
        //2.使用if-else if-else分支结构判断身份信息并给出对应的提示
        //由于String类型是引用数据类型，因此使用equals方法进行判断
        if("军人”.equals(str)) {
           System.out.println("请免费乘车!");
        }else if("学生”.equals()) {
           System.out.println("请购买半价票!");
        }
        else{
            System.out.println("全价票等着您!");
        }
        //3.打印一句话
		System.out.println("坐上了火车去拉萨，去看那美丽的布达拉!");
    }
}
```

##### 语法格式：

​	if (条件表达式1) {

​		语句块1;

​	}else if (条件表达式2) {

​		语句块2;

​	}

​	……

​	else {

​		语句块n;

​	}

##### 执行流程：

​	判断条件表达式1是否成立

​		=> 若成立，则执行语句块1；

​		=> 若不成立，则判断条件表达式2是否成立；

​			=> 若成立，则执行语句块2；

​			=> 若不成立，则执行语句块n；

### for循环结构

#### 代码案例

```java
/*  
   编程实现for循环的使用
 */
public class ForTest {
  
  public static void main(String[] args) throws Exception {
    
     for(int money = 500; money >= 100; money -= 100) {
       System.out.println("当前账户余额：" + money + "，正在出钞，请稍后...");
       
       Thread.sleep(5000); //睡眠5秒的过程
       System.out.println("请取走您的钞票！\n\n\n");
     }
     
     System.out.println("现在可以尽情地挥霍了...");
     
   }
}
```

##### 语法格式：

​	for(初始化表达式;条件表达式;) {

​		循环体；

​	}

##### 执行流程：

​	执行初始化表达式 => 判断条件表达式是否成立

​		=>若成立，则执行循环体 => 修改初始值表达式 => 判断条件表达式是否成立

​		=>若不成立，则循环结束

特殊的for循环：

​	for(; ;)  -  这种没有循环条件的循环叫做无限循环，俗称“死循环”。

### Break关键字和Continue关键字

```Java
/*
  编程实现break关键字和continue关键字的使用
*/
public class BreakContinueTest {
    public static void main(String[] args) {
        for(int i = 1; i <= 20; i++) {
            if(0 == i%5) {
                continue; //结束本次循环继续下一次循环  奔向了i++
            }
            if(18 == i) {
                break; //跳出当前循环
            }
            System.out.println("i = " + i); //1 2 3 4 6 ... 17
        }
        // break执行后跳到这里了...
    }
}
```

+ break关键字用于循环中表示跳出当前循环；
+ continue关键字用于循环中表示结束本次循环继续下一次循环；

### 双重for循环

#### 代码案例

```
/*
  编程实现双重for循环的使用
*/
public class ForforTest {
    public static void main(String[] args) {
    	for(int i = 1; i <= 5; i++) {
            // 用于控制打印的空格个数
            for(int j = 1; j <= 5 - i; j++) {
                // 打印完毕不换行
                System.out.print(" ");
            }
            // 内层循环用于控制当前行打印的列数
            for(int j = 1; j <= 2 * i - 1; j++) {
                // 打印完毕不换行
                System.out.print("*");
            }
            // 专门用于换行
            System.out.println();
        }
    }
}    
```

##### 语法格式：

​	for(初始化表达式1; 条件表达式2; 修改初始值表达式3) {

​		for(初始化表达式4 ; 条件表达式5 ; 修改初始值表达式6) {

​			循环体;

​		}

​	}

##### 执行流程：

​	执行表达式1 => 判断表达式2是否成立

​		=> 若成立，则执行循环体 => 执行表达式6 => 判断表达式5是否成立

​			=> 若不成立，则内层循环结束 => 执行表达式3 => 判断表达式2是否成立

​			=>若不成立，则外层循环结束

​		=>若不成立，则外层循环结束

注意：

+ 外层循环变量动一下，则内层循环变量跑一圈；
+ 当需要打印多行多列的数据内容时，可以使用双重for循环；

### While循环：

#### 代码案例：

```java
public class WhileTest {
    public static void main(String[] args) {
        // 1.使用for循环打印1~10之间的所有整数
        for(int i = 1; i <= 10; i++) {
            System.out.println("i = " + i);
        }

        System.out.println("-----------------------------");

        // 2.使用while循环打印1~10之间的所有整数
        int i = 1;
        while(i <= 10) {
            System.out.println("i = " + i);
            i++;
        }
    }
}
```

##### 语法格式：

​	while(条件表达式){

​		循环体;

​	}

##### 执行流程：

​	判断条件表达式是否成立

​		=> 若成立，则执行循环体 => 判断条件表达式是否成立

​		=> 若不成立，则循环结束

注意：

+ while循环和for循环可以完全互换；

+ while(true)和for(;;)表示无限循环；

+ while循环主要用于明确循环条件但不明确循环次数的场合中；

  for循环主要用于明确循环次数或范围的场合中；

### switch-case分支结构

#### 代码案例：

```java
import java.util.Scanner;

public class TestSwitchMenu {
    public static void main(String[] args) {
        // 1.提示用户输入1~5之间的整数并使用变量记录
        System.out.println("请输入1~5之间的整数：");
        Scanner sc = new Scanner(System.in);
        int choose = sc.nextInt();

        // 2.使用switch-case分支结构根据不同的输入给出对应的提示
        switch(choose) {
            case 1:
                System.out.println("显示所有用户");
                break;
            case 2:
                System.out.println("增加新用户");
                break;
            case 3:
                System.out.println("修改用户信息");
                break;
            case 4:
                System.out.println("删除用户信息");
                break;
            case 5:
                System.out.println("退出系统");
                break;
            default:
                System.out.println("输入错误，请输入1~5之间的整数");
                
            //1.提示用户输入1~5之间的整数并使用变量记录
            System.out.println("请输入1~5之间的整数:");
            int choose = sc.nextInt();
            
            //2.使用switch-case分支结构根据不同的输入给出对应的提示
            switch(choose) {
            	case 1: System.out.println("显示所有用户"); break;
                case 2:System.out.println("增加新用户");break;
                case 3:System.out.println("修改用户信息");break;
                case 4:System.out.println("删除用户信息");break;
                case 5:System.out.println("退出系统");break;
                default:System.out.println("输入错误，请重新输入!");
            }
        }
    }
}
```

##### 语法格式：

​	switch(变量/表达式) {

​		case 字面值1: 语句块1; break;

​		case 字面值2:语句块2;break;

###### 		……

​		default: 语句块n;

​	}

##### 执行流程：

​	计算变量/表达式的数值 => 判断是否匹配字面值1

​		=> 若匹配，则执行语句块1 => 执行break跳出当前结构

​		=> 若不匹配，则判断是否匹配字面值2

​			=> 若匹配，则执行语句块2 => 执行break跳出当前结构

​			=> 若不匹配，则执行语句块n

注意：

​	switch()中支持的数据类型有：byte、short、char以及int类型，从idk1.5开始支持枚举类型，从jdk1.7开始支持String类型；



# Java语言的数组声明与应用

### 一、一维数组

##### 基本概念

​	当需要在程序中记录单个数据内容时，则声明一个变量即可；、

​	当需要在程序中记录多个类型相同的数据内容时，则声明一维数组即可，一维数组的本质就是在内存中申请一段连续的存储单元。

+ 数组是相阆数据类型的多个元素的容器，元素按线性顺序排列。
+ 所谓线性顺序是指除第一个元素外，每一个元素都有唯一的前驱元素;除最后一个元素外，每一个元素都有唯一的后继元素:（”一个跟一个”）。
+ 数组的操作其实就是对下标的控制，可以通过下标方式访问数组中每个元素。

![image-20250701101031535](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20250701101031535.png)

#### 代码案例

```java
public class ArrayTest {
    public static void main(String[] args) {
        // 1.声明一个长度为3元素类型为int类型的一维数组
        int[] arr = new int[3];

        // 2.打印数组的长度以及每个元素的数值
        System.out.println("数组的长度是：" + arr.length); // 3
        System.out.println("下标为0的元素是：" + arr[0]);  // 0 默认值
        System.out.println("下标为1的元素是：" + arr[1]);  // 0
        System.out.println("下标为2的元素是：" + arr[2]);  // 0
        
        // 编译ok，运行产生ArrayIndexOutOfBoundsException数组下标越界异常
        // System.out.println("下标为3的元素是：" + arr[3]);

        System.out.println("-----------------------------");
        /3.使用循环实现数组中所有元素的打印
        for(int i=0;i < arr.length;i++) {
        	System.out.println("下标为" + i + "的元素是: " + arr[i]);//0
        }
        
        System.out.println("-----------------------------");
        //4.声明一个长度为5元素类型为double类型的数组并打印默认值
        double[] dArr =new double[5];
        for(int i=0;i < dArr.length; i++) {
        	System.out.println("下标为" + i + "的元素是: " + dArr[i]);//0.0
        }
        
        System.out.println("-----------------------------");
        //5.实现对数组arr中的元素依次赋值为11 22 33
        /*
        arr[0]= 11;
        arr[1]= 22;
        arr[2]= 33;
        */
        for(int i = 0;i < arr.length; i++) {
            arr[i] =
        }
        //使用循环实现数组中所有元素的打印
        for(int i = 0;i < arr.length; i++) {
            System.out.println(arr[i]);//11 22 33
        }
    }
}
```



##### 语法格式

​	数据类型[]  数组名称 = new 数据类型[数组的长度]；

如：

​	`int []  arr = new int[5];`	-  表示声明一个长度为5元素类型为int类型的一维数组

​	`int num=5;`		   		     -  表示声明一个初始值为5的变量

​	`int arr[] = new int [5];`	  -  不推荐使用

##### 元素的初始化

​	数据类型[]  数组名称 = {元素值1，元素值2,……};

如：

​	`int[] arr = { 10，20，30，40，50 };`



### 数组的增删改查

#### 代码案例

```java
/* 
   编程实现数组的增删改查操作
*/
public class ArrayOperationTest {
    public static void main(String[] args) {
        // 1.声明一个长度为5元素类型为int类型的一维数组
        int[] arr = new int[5];
        
        // 打印所有元素值
        System.out.print("数组中的元素初始值为：");
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " "); // 输出：0 0 0 0 0
        }
        System.out.println();
        
        System.out.println("-----------------------------");
        // 2.使用10、20、30、40分别给数组中前四个位置元素赋值
        for(int i = 0; i < arr.length - 1; i++) {
            arr[i] = (i + 1) * 10;  // 依次赋值为10,20,30,40
        }
        // 打印所有元素
        System.out.print("数组赋值后的元素为：");
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");  // 输出：10 20 30 40 0
        }

        System.out.println();  // 换行

    }
}
```

##### 数组的插入操作

```java
	// 3.将数据50插入到数组中下标为0的位置，原有元素向后移动
        for(int i = arr.length - 1; i > 0; i--) {
            arr[i] = arr[i-1];  // 将每个元素向后移动一位
        }
        arr[0] = 50;  // 在首位插入新值

        // 打印插入后的数组
        System.out.print("数组插入后的元素为：");
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");  // 输出：50 10 20 30 40
        }
        System.out.println();  // 换行
```

##### 数组的删除操作

```java
	// 4.将数据50从数组中删除，后续元素向前移动
        for(int i = 0; i < arr.length-1; i++) {
            arr[i] = arr[i+1];  // 每个元素向前移动一位
        }

        arr[4] = 0;  // 将最后一个元素置为0

        // 再次打印所有元素
        System.out.print("数组删除后的元素为：");
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");  // 输出：10 20 30 40 0
        }

        System.out.println();  // 换行
```

##### 数组的查找操作

```java
// 5.查找数组中是否包含元素20，若包含将元素20改为200
    for(int i = 0; i < arr.length; i++) {
        if(20 == arr[i]) {
            arr[i] = 200;
            //break; // 加上break的效果就是只要找到1个20就查找结束
        }
    }

    // 再次打印所有元素
    System.out.print("数组改查后的元素为：");
    for(int i = 0; i < arr.length; i++) {
        System.out.print(arr[i] + " "); // 输出示例：10 200 30 40 0
    }

    System.out.println(); // 换行
```



### 二、二维数组

##### 基本概念

​	一维数组本质上就是一段连续的存储单元，用于存放多个类型相同的数据内容;

​	二维数组本质上就是由多个一维数组组成(摞在一起)的数组，也就是说二维数组中的每个元素都是一个一维数组，而一维数组中的每个元素才是数据内容；



##### 一维数组与二维数组的特征

![image-20250701105927991](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20250701105927991.png)

#### 代码案例

```java
/*
  编程实现二维数组的声明和打印
*/
public class ArrayArrayTest {
    public static void main(String[] args) {
        // 1.声明一个2行3列的int型二维数组（默认值全为0）
        int[][] arr = new int[2][3];

        // 2.打印二维数组所有元素
        // 外层循环控制行数
        for(int i = 0; i < 2; i++) {
            // 内层循环控制列数
            for(int j = 0; j < 3; j++) {
                System.out.print(arr[i][j] + " "); // 打印元素加空格
            }
            System.out.println(); // 每行结束换行
        }
        
        System.out.println("--------------------------------------------------");
        // 3.二维数组中元素的初始化和打印
        int[][] brr = {
            {1, 2, 3},  // 第一行
            {4, 5, 6}   // 第二行
        };

        // 使用外层for循环控制打印行数（动态获取行数）
        for(int i = 0; i < brr.length; i++) {
            // 使用内层for循环控制打印列数（动态获取每行列数）
            for(int j = 0; j < brr[i].length; j++) {
                System.out.print(brr[i][j] + " ");  // 1 2 3   4 5 6
            }
            System.out.println();  // 每行结束换行
        }
        
        System.out.println("---------------------------------------------------");
        // 4.二维数组的特殊用法（不规则数组）
        int[][] crr = new int[3][];  // 声明3行的二维数组（每行长度未定）

        // 分别为每行分配不同长度的数组
        crr[0] = new int[3];  // 第一行3列
        crr[1] = new int[4];  // 第二行4列
        crr[2] = new int[5];  // 第三行5列
    }
}
```

##### 语法格式

​	数据类型[] []  数组名称 = new 数据类型[行数] [列数];

如：

​	int [] [] brr = new int [2] [3];  -  声明一个具有2行3列元素类型为int类型的二维数组

​	其中行下标的范围是:0~1；

​	其中列下标的范围是:0~2；

##### 二维数组的分析

​	`brr.length`  表示二维数组的长度，也就是二维数组中元素的个数，也就是一维数组的个数，也就是行数

​	`brr[0].length`  表示二维数组中的第一个元素的长度，也就是第一行的长度，也就是第一行的列数

​	`brr[0] [0]`  表示二维数组中第一行第一列的数据内容

##### 元素的初始化

​	数据类型[] []  数组名称 =  {{初始值1，初始值2, …… }, …… };

如：

​	int[] [] brr = {{1,2,3}, {4, 5,6}};



# 理解面向对象思想和概念

### 一、面向对象编程的概念

#### 什么是对象？

+ 万物皆对象

#### 什么又是面向对象？

+ 面向对象就是指以特征（属性）和行为的观点去分析现实世界中事物的方式

#### 什么又是面向对象编程？

+ 面向对象编程就是指先使用面向对象的方式进行分析，再使用任意一门面向对象的编程语言进行翻译的过程。
+ 其中C语言是一门面向过程的编程语言。
+ 其中C++语言是一门既面向过程又面向对象的编程语言。
+ 其中Java语言是一门纯面向对象的编程语言。

#### 如何学好面向对象编程语言？

+ 深刻理解面向对象编程的三大特征：封装、继承、多态。



### 二、类、对象以及引用

#### 对象和类的概念

+ 对象是客观存在的实体，在Java语言体现为内存空间的一块区域。
+ 类就是分类的概念，是对具有相同特征和行为的多个对象共性的抽象描述，在Java语言中包含描述特征的成员变量和描述行为的成员方法，是创建对象的模板。
+ 类定义了该类型对象的数据结构，称之为 **成员变量** 同时，也定义了一些可以被调用的功能，称之为**成员方法**。
+ 类是用于构建对象的模板，对象的实质就是**内存**中块存储区域，其数据结构由定义它的类来决定。

##### 如：

​	String name "富强";	int age = 18;	……

​	String name2 "张三";	int age = 17;	……

​	String name "李四";	int age = 20;	……

​	……

​	人类：

​	特征：姓名、年龄

​	行为：学习、吃饭

#### 类的定义

##### 类定义的语法格式

​	class 类名 {

​		类体;

​	}

##### 如：

​	class Person {

​	}

##### 注意：

+ 当类名有多个单词组成时，要求每个单词的首字母都要大写；



##### 成员变量定义的语法格式

​	

```
class 类名 {

​		数据类型 成员变量 = 初始值;	- 其中 =初始值 通常省略，分号不能省略

	}
```

##### 如：

```
	class Person {

​		String name;

​		int age;

	}
```

##### 注意：

+ 当成员变量名由多个单词组成时，要求从第二个单词起每个单词首字母大写；

##### 扩展：

+ 局部变量 - 主要指在方法体中声明的变量，作用范围从声明开始到方法体结束
+ 成员变量 - 主要指在方法体外类体内声明的变量，作用范围从声明到类体结束



#### 对象的创建

+ 当一个类的定义存在后，可以使用 **new** 关键字创建该类的对象。对象创建的过程一般称为类的实例化。

##### 语法格式

new 类名 () {

​	new Point(); 	- 创建Person类型的对象，由于该对象没有名字因此叫做”匿名对象“

}

##### 注意：

+ 一个类定义完毕后，使用new关键字创建/构造对象的过程叫做 类的实例化;
+ 创建对象的本质就是在内存中的堆区申请存储空间，来存放该对象独有的特征信息



#### 引用

##### 基本概念

+ 在Java语言中使用引用数据类型声明的变量叫做引用型变量，简称为"引用"
+ 引用变量主要用于记录对象在堆区中的内存地址信息，便于下次访问

#### 代码案例

```java
/* 
   编程实现Person类的定义和使用
*/
public class Person {
    String name; // 用于描述姓名的成员变量
    int age;     // 用于描述年龄的成员变量

    public static void main(String[] args) {
        // 1.创建Person对象（成员变量默认值：name=null, age=0）
        Person p = new Person();
        
        // 2.打印初始成员变量
        System.out.println("我是" + p.name + ", 今年" + p.age + "岁了！"); 
        // 输出：我是null, 今年0岁了！
        
        System.out.println("--------------------------------------------------");
        
        // 3.修改成员变量
        p.name = "张三";
        p.age = 18;
        
        // 4.打印修改后的信息
        System.out.println("我是" + p.name + ", 今年" + p.age + "岁了！");
        
        System.out.println("---------------------------------------------------");
    }
}
```

##### 语法格式

类名 引用变量名

##### 如：

`Person p;`  -  表示声明Person类型的引用变量p，本质上在栈区申请存储空间

`Person p  =  new Person();`  -  表示声明引用变量p来记录Person类型对象的地址信息

引用变量名 . 成员变量名;

##### 如：

`p.name = "zhangfei";`	-  表示使用引用变量p访问所指向堆区对象的姓名特征



### 三、成员方法

#### 代码案例

```java
/* 
   编程实现Person类的定义和使用
*/
public class Person {
    String name; // 用于描述姓名的成员变量
    int age;     // 用于描述年龄的成员变量
    
    void show() {
        System.out.println("我是" + p.name + ", 今年" + p.age + "岁了！"); 
    }
    
    void setName(String s){
        name = s;
    } 
    
    void setAge(Int i){
        age = i;
    } 
    
    String getName(){
        return name;
    }
    
    int getAge(){
        return age;
    }
    
    public static void main(String[] args) {
        // 1.创建Person对象（成员变量默认值：name=null, age=0）
        Person p = new Person();
        // 2.打印初始成员变量
        // System.out.println("我是" + p.name + ", 今年" + p.age + "岁了！"); 
        p.show();
        // 输出：我是null, 今年0岁了！
        
        System.out.println("--------------------------------------------------");
        
        // 3.修改成员变量
        p.name = "张三";
        p.age = 18;
        
        // 4.打印修改后的信息
        // System.out.println("我是" + p.name + ", 今年" + p.age + "岁了！");
        p.show();
        
        System.out.println("---------------------------------------------------");
        // 调用成员方法实现姓名和年龄的修改
        p.setName("guanyu");
        p.setAge(35);
        p.show();
        
        System.out.println("---------------------------------------------------");
        // 调用成员方法实现姓名和年龄的获取
        String str = p.getName();
        System.out.println("获取到的姓名是: + str");//guanyu
        int res = p.getAge();
        System.out.println("获取到的年龄是: + res");// 35
    }
}
```

##### 语法格式

​	class 类名 {

​		返回值类型   成员方法名（形参列表） {

​			成员方法体；

​	}

}

##### 如：

​	class Person {

​		void show() {

​			System.out.println("没事出来秀一下！")；

​	}

}

注意：

​	当成员变量名由多个单词组成时，通常要求从第二个单词起每个单词首字母大写。

#### 返回值类型

+ 返回值主要指从方法体内向方法体外返回的数据内容；
+ 返回值类型主要指返回值的数据类型，可以是基本数据类型，也可以是引用数据类型；

##### 如：

+ 当返回的数据内容是66时，则返回值类型写`int`即可;
+ 当返回的数据内容是3.14时，则返回值类型写`double`即可;
+ 当返回的数据内容是"hello"时，则返回值类型写`String`即可;

在方法体中使用return关键字来返回数据内容

##### 如：

+ 当返回的数据内容是66时，则方法体中写:return  66;
+ 当返回的数据内容是num时，则方法体中写:return num;
+ 若该方法不需要返回任何数据内容，则返回值类型写void即可。

#### 形参列表

+ 形式参数主要用于将方法体外的数据传入到方法体的内部，格式:数据类型形参名。

+ 形参列表主要指多个形式参数组成的整体，格式如下:

  ​	数据类型 形参名1，数据类型 形参名2, ......

##### 如：

+ 当传入的数据内容是66时，则形参列表写为:  ` int i `  即可;
+ 当传入的数据内容是3.14时，则形参列表写为:  `double d`  即可;
+ 当传入的数据内容是"hello"时，则形参列表写为:  `String s`  即可;
+ 当传入的数据内容是66和"he11o"时，则形参列表写为: `int i`  `String s`即可；
+ 若该方法不需要传入任何数据内容时，则形参列表位置啥也不写即可;

#### 成员方法体

​	成员方法体主要编写描述该方法功能的语句

##### 如：

+ 当该方法的功能就是打印时，则方法体中写 `System.out.println("...”);`即可
+ 当该方法的功能就是返回66时，则方法体中写`return 66;`即可

#### 方法的调用

##### 语法格式

​	引用变量名.成员方法名(实参列表);

##### 如：

​	`p.show();`	-  表示使用引用变量p调用show方法

##### 注意：

+ 实际参数列表主要用于对形式参数列表进行初始化操作,因此参数的个数、类型、顺序等都必须与形参列表保持一致;

+ 实参可以传递直接量、变量、表达式以及方法的调用等;



#### JVM内存结构-方法区

+ 该空间用于存放类的信息。Java程序运行时，首先会通过类装载器载入类文件的字节码信息，经过解析后将其装入方法区。在方法区保存类的各种信息

`Point p = new Point();`

`Point`类首先被装载到 `JVM` 的方法区，包括类的基本信息和方法定义等。



# 构造方法及方法重载

### 一、构造方法和方法重载

#### 代码案例

```java
/*
  编程实现Person类的定义
*/
public class Person {
    String name; // 用于描述姓名的成员变量
    int age;     // 用于描述年龄的成员变量

	// 无参构造方法
	Person(){
		// System.out.println("会不会调用我？");
        name = "xiaomage";
        age = 18;
    }
    // 有参构造方法
    Person(String s, int i){
		// System.out.println("会不会调用我？");
        s = "zhangfei";
        i = 18;
    }
    // 实现打印所有特征的方法
    void show() {
        System.out.println("我是" + name + "，今年" + age + "岁了！");
    }

    public static void main(String[] args) {
        // 声明Person类型的引用指向Person类型的对象
        Person p = new Person();
        p.show(); // 输出：我是xiaomage，今年18岁了！
        
        System.out.println("----------------------------------");
        Person p2 = new Person("zhangfei");
        p2.show(); // 输出：zhangfei，今年18岁了！
    }
}
```

##### 如：

​	Person p=new Person();	-  声明Person类型的引用指向Person类型的对象

​	p.show();				  -  使用引用变量p调用show方法

#### 构造方法

##### 语法格式

​	class  类名  {

​		类名（形参列表） {

​			构造方法体

​		}

​	}

##### 如：

​	class Person {

​		Person() {

​		}

​	}

##### 注意：

+ 构造方法的名称与类名完全相同，没有返回值类型连void都不许有
+ 当使用new关键字构造对象时会自动调用构造方法进行成员变量的初始化工作。

##### 默认构造方法

+ 当一个类中没有自定义任何形式的构造方法时，编译器会自动添加一个无参的空构造方法，叫做默认/缺省构造方法，如:`Person(){}`
+ 若类中出现自定义构造方法，则编译器不再提供任何形式的构造方法。

#### 方法的重载

#### 代码案例

```java
/*
  编程实现方法重载的测试
*/
public class OverloadTest {
    // 无参show方法
    void show() {
        System.out.println("show()");
    }
    
    // 重载的show方法（参数个数不同）
    void show(int i) {  //ok 体现在参数的个数不同
        System.out.println("show(int)");
    }
	void show(int i,double d) {  //ok 体现在参数的个数不同
        System.out.println("show(int,double)");
    }
	void show(int i,int j) {  //ok 体现在参数的类型不同
        System.out.println("show(int,int)");
    }
    void show(double d,int i) {  //ok 体现在参数的顺序不同
        System.out.println("show(double,int)");
    }
    void show(int d,double i) {  //erro 与参数变量名无关
        System.out.println("show(int,double)");
    }
    
    public static void main(String[] args) {
        // 声明本类类型的引用指向本类的对象
        OverloadTest ot = new OverloadTest();
        
        // 调用成员方法
        ot.show();     // 调用无参show方法
        ot.show(66);   // 调用带int参数的show方法
        ot.show(66,3.14);
    }
}
```

##### 基本概念

​	在Java语言中若方法的名称相同但参数列表不同，这样的方法之间构成重载关系。

##### 体现形式

+ 方法重载的主要形式有:参数的个数不同、参数的类型不同、参数的顺序不同，与形参变量名和返回值类型无关，但建议返回值类型最好相同

+ 判断方法是否重载的核心:调用能否区分。

##### 实际意义

​	对于调用者来说只需要记住一个方法名就可以调用各种不同的版本实现不同的效果。

##### 如：

​	`char c = 'a';`

​	`System.out.println(c);`

​	`int i = 10;`

​	`System.out.println(i);`

​	`double d = 3.14;`

​	`System.out.println(d);`

​	……

### 二、this关键字

```java
/* 
  编程实现this关键字概念的测试
*/
public class ThisTest {
    // 无参构造方法
    ThisTest() {
        //在构造方法中出现this代表当前正在构造的对象
        System.out.println("构造方法");
    }
    
    // 成员方法
    void show() {
        //在成员方法中出现this代表当前正在调用的对象
        System.out.println("成员方法");
    }
    
    public static void main(String[] args) {
        // 创建对象并调用方法
        ThisTest tt = new ThisTest();  // 触发构造方法执行
        tt.show();                     // 调用成员方法
        System.out.println("main方法中: tt = " + tt);
        
        System.out.println("----------------------------------");
        ThisTest tt2 = new ThisTest();  
        tt2.show(); 
        System.out.println("main方法中: tt2 = " + tt2);
    }
}
```

##### 基本概念

+ 在构造方法中`this`关键字代表当前正在构造的对象。
+ 在成员方法中`this`关键字代表当前正在调用的对象。

##### 原理分析：

​	当成员方法中访问成员变量时默认会加上`this.`(相当于汉语中"我的”)，当不同的引用调用同一个成员方法时会导致成员方法中的`this`不同，那么`this.`访问的结果随之不同。

##### 使用方式：

+ 当形参变量和成员变量同名时，在构造方法或成员方法中通常优先使用形参变量，若希望使用成员变量就需要在变量名的前面加上`this.`进行说明(重中之重)。
+ 在构造方法的第一行使用this(实参)的方式可以调用本类中的其它构造方法(了解)



### 三、方法的传参和递归调用

#### 方法的传参过程

#### 代码案例

```Java
/*
编程实现参数传递过程的测试
*/
public class ArgumentTest {
    void show(int i) {
        i = 200;
        System.out.println("i = " + i); // 输出: i = 200
    }

    public static void main(String[] args) {
        ArgumentTest at = new ArgumentTest();
        int num = 10;
        at.show(num);
        System.out.println("num = " + num); // 输出: num = 10
    }
}
```

#### 

+ 分配实参然间，基本类型在栈中赋值，引用类型变量在栈中指向堆中的对象
+ 传递参数装实就是在栈中分配形参的空间，然后把栈中实参的值复制过来。
+ 在方法中使用形参，方法结束形参出栈(消失)，只剩下实参。

##### 掌握内容

+ 当基本数据类型的变量作为方法的参数传递时，形参变量的改变不会影响到实参；
+ 用数据类型的变量作为方法的参数传递时，形参变量指向的内容发生改变后会影响到实参变量指向的
+ 当引用数据类型的变量作为方法的参数传递时，形参变量改变指向后再改变指向的内容时不会影响到实参变量指向的内容；

#### 递归调用

#### 代码案例

```java
/*  
   编程实现阶乘的计算并打印
*/
public class JiechengTest {

    // 自定义成员方法实现参数n阶乘的计算并返回
    int show(int n) {
        int res = 1;
        for(int i = n; i > 1; i--) {
            res *= i; // res = res * i;
        }
        return res;
    }

    public static void main(String[] args) {
        JiechengTest jt = new JiechengTest();
        int num = jt.show(5);
        System.out.println("最终计算的结果是：" + num); // 输出：最终计算的结果是：120
    }
}

```



##### 基本概念

+ 在一个方法体的内部调用当前方法自身的形式，叫做递归。

##### 如：

​	void show() {

​		show();

​	}

##### 案例：

​	自定义成员方法实现参数n阶乘的计算并返回

##### 解析：

​	5 ! = 5 * 4 * 3 * 2 * 1；

​	4! = 4 * 3 * 2 * 1；

​	3 ! = 3 * 2 * 1；

​	2 ! = * 2 * 1；

​	1 ! =  1；

​	n ! = n * (n-1) * (n-2) * …… *



# 面向对象的封装特性和static关键字

### 一、封装

#### 代码概念

```java
/*
  编程实现Person类的封装
*/
public class Person {
    // 1.私有化成员变量，使用private关键字修饰
    private String name;
    private int age;
    private String country;

    // 2.提供构造方法
    public Person() {
    }

    public Person(String name, int age, String country) {
        setName(name);
        setAge(age);
        setCountry(country);
    }

    // 3.提供公有的get和set方法，并在方法体中进行合理值的判断
    public String getName() {
        return name;
    }

    public void setName(String name) {
        if (name == null || name.trim().isEmpty()) {
            throw new IllegalArgumentException("姓名不能为空");
        }
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age < 0 || age > 150) {
            throw new IllegalArgumentException("年龄必须在0-150之间");
        }
        this.age = age;
    }

    public String getCountry() {
        return country;
    }

    public void setCountry(String country) {
        if (country == null || country.trim().isEmpty()) {
            throw new IllegalArgumentException("国家不能为空");
        }
        this.country = country;
    }

    @Override
    public String toString() {
        return "Person{" +
                "name='" + name + '\'' +
                ", age=" + age +
                ", country='" + country + '\'' +
                '}';
    }
}
```



##### 基本概念

+ 通常情况下测试类可以对封装类中的成员变量进行赋值，若赋值的数据合法但不合理无论时编译阶段还是运行阶段都不会报错或者给出提示，此时与现实生活不符。
+ 为了避免上述错误的发生，就需要对成员变量进行密封包装处理，该机制就叫做封装换句话说，封装就是一种保证成员变量值合理性的机制。

##### 实现流程

（1）私有化成员变量，使用private关键字修饰;

（2）提供公有的get和set方法，在方法体中进行合理值的判断;

（3）在构造方法中调用set方法进行合理值的判断

### 二、static关键字

#### 代码案例

```
/*
   编程实现Singleton类的测试
*/
public class SingletonTest {
    
    public static void main(String[] args) {
        // 声明Singleton类型的引用指向该类型的对象
        Singleton s1 = new Singleton();
        Singleton s2 = new Singleton();
        System.out.println(s1 == s2); // 判断s1的数值是否与s2相等  false
    }
}

/*
   标准单例模式实现（补充）
*/
class Singleton {
    // 1.私有化构造方法
    private Singleton() {}
    
    // 2.声明本类类型的引用指向本类类型的对象
    private static Singleton instance = new Singleton();
    
    // 3.提供公有的get方法负责将对象返回出去
    public static Singleton getInstance() {
        return instance;
    }
}
```

##### 基本概念

+ 通常情况下成员变量隶属于对象层级，每创建一个对象就需要申请独立的内存空间来存放该对象独立的成员变量信息，若所有对象的某个成员变量数值完全一样却又单独存放会造成内存空间的浪费。

+ 为了解决上述问题，则使用static关键字修饰成员变量，此时该成员变量由对象层级提升为类层级被所有对象共享，该成员变量随着类的加载准备就绪，与是否创建对象无关

+ 类加载只做一次，包括:

  1. 类名.的时候会类加载。

  2. new对象时会类加载。
  3. 程序员可以用程序加载，比如:Class.forName();

+ 静态的成员(属性和方法)可以用对象.调用，但一般推荐用类名.调用。

##### 使用方式

+ 在非静态的成员方法中既能访问非静态的成员也能访问静态的员；
  （成员:成员变量+成员方法，静态成员被所有对象共享）。

+ 在静态的成员方法中只能访问静态的成员不能访问非静态的成员；

  （成员:成员变量+成员方法，调用静态方法时可能还没有创建）。

+ 只有隶属于类(所有对象共享)的属性才能加static，static不能随便加。

##### 案例：

​	编程实现Singleton类的封装；

​	编程实现SingletonTest类的

​	编程实现SingletonTest类对Singleton类进行测试，要求在main方法中能得到且只能得到Singleton类的一个对象。

#### 单例设计模式

##### 基本概念

+ 在某些特殊场合中一个类对外提供且只提供一个对象，这样的类叫做单例类。

+ 主要用于固定的场合而设计单例类的思想和模式叫做单例设计模式，

##### 实现流程

+ 私有化构造方法，使用private关键字修饰；

+ 声明本类类型的引用指向本类类型的对象，使用private static共同修饰；

+ 提供公有的get方法负责将成员变量的数值返回出去，使用static关键字修饰；

##### 实现方式

+ 单例设计模式的实现方式有两种：饿汉式和 懒汉式，在以后的开发中推荐饿汉式

### 三、继承

#### 代码案例

```java
/*
  编程实现构造块和静态代码块的认识和使用
*/
public class TestStaticBlock {
    
    // 构造代码块（每次创建对象时都会执行）
    {
        System.out.println("构造块！");
    }
    
    // 静态代码块（类加载时执行，仅执行一次）
    static {
        System.out.println("静态代码块！");
    }
    
    // 构造方法
    public TestStaticBlock() {
        System.out.println("构造方法体！");
    }
    
    public static void main(String[] args) {
        System.out.println("-- 第一次创建对象 --");
        TestStaticBlock tsb1 = new TestStaticBlock();
        
        System.out.println("\n-- 第二次创建对象 --");
        TestStaticBlock tsb2 = new TestStaticBlock();
    }
}
```

##### 基本概念

学生类:

​	特征:学号、姓名、年龄

​	行为:学习、吃饭、

教师类:

​	特征:工号、姓名、年龄

​	行为:i讲课、吃饭、娱乐

工人类:
	特征:姓名、年龄、薪水

​	行为:工作、吃饭、娱乐

+ 当多个类之间有相同的特征和行为时，可以将相同的内容提取出来组成一个公共类，让多个类吸收公共类中已有特征和行为而在多个类的内部编写自己独有特征和行为的方式，叫做继承。
+ 使用继承可以提高代码的复用性和扩展性以及可维护性。

##### 如：

`public class StudentextendsoPerson（） {}`	-  表示Student类继承自Person类

​	其中Person类叫做基类、父类、超类

​	其中Student类叫做派生类、子类、孩子类

##### 使用方式

（1）非静态的成员方法中既能访问非静态的成员也能访问静态的成员；

（成员：成员变量 + 成员方法静态的内容被所有对象共享）

（2）静态的成员方法中只能访问静态的成员不能访问非静态的成员;
使用静态内容时可能还没有创建对象)
（成员：成员变量 + 成员方法）

（3）只有隶属于类层级被所有对象共享的内容才可以使用`static`关键字修饰;(不能滥用`static`关键字)



# 面向对象的继承特性和final关键字

### 一、继承特性

##### 基本概念

+ 当多个类之间有相同的特征和行为时，可以将相同的内容提取出来组成一个公共类，让多个类吸收公共类中已有特征和行为而在多个类的内部编写自己独有特征和行为的方式叫做继承。
+ 使用继承可以提高代码的复用性和扩展性以及可维护性。
+ 在Java语言中使用extends(扩展)关键字来表达继承关系

##### 如：

+ `public class Worker extends Person`	- 表示Worker类继承自Person类

+ 其中Person类叫做基类、父类、超类
+ 其中Worker类叫做派生类、子类、孩子类

##### 注意事项

（1）子类可以继承父类的成员变量和成员方法，其中私有成员变量可以继承但不可以直接使用，子类不可以继承父类的构造方法和私有方法。

（2）无论使用何种方式构造子类对象时，都会自动调用父类中的无参构造方法来初始化从父类中继承下来的成员变量，相当于在子类构造方法第一行增加代码:super()的效果

（3）使用继承必须满足子类isa父类的逻辑关系，也就是不能滥用继承。一个子类只能有一个父类，但一个

（4）Java语言中只支持单继承不支持多继承，也就是父类可以有多个子类。

![image-20250703210230881](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\image-20250703210230881.png)

#### 方法的重写

##### 基本概念

若从父类中继承下来的方法不满足子类的需求时，就需要在子类中重新写一个与父类中一样的方法来覆盖从父类中继承的版本，这种方式就叫做重写。

##### 重写的原则

+ 要求方法名相同、参数列表相同、返回值类型相同，从idk1.5开始允许返回子类类型
+ 要求方法的访问权限不能变小，可以相同或者变大。
+ 要求不能抛出更大的异常(异常机制)

### 二、访问控制

##### 常用的访问控制符

访问控制	符访问权限	本类	本包中的类	子类	其它包中的其它类

public		公有的	      ok		ok		  ok			ok

protected	 保护的	      ok		 ok		  ok			no

啥也不写	    默认的	     ok		 ok		  ok			no

private		私有的	    ok		 no		  no		       no

+ public修饰的内容可以在任意位置使用；

+ private修饰的内容只能在本类中使用；

+ 通常情况下，成员变量都使用private修饰，成员方法都使用public修饰；

##### 包的定义

package 包名;

package 包名1.包名2...包名n；- 便于管理，避免命名冲突的问题

### 三、final关键字

##### 基本概念

final本意为"最终的，不可更改的"，该关键字可以修饰类、成员方法、成员变量等。

##### 使用方式

final关键字修饰类表示该类不能被继承。

	- 为了防止滥用继承带来的危害
	- 如:java.lang.String类等

final关键字修饰成员方法表示该方法不能被重写但可以被继承。

- 为了防止不经意间造成的方法重写
- 如:java.text.DateFormat类中的format方法等

final关键字修饰成员变量表示该成员变量必须初始化而且不能更改。

+ 为了防止不经意间造成数值的更改。
+ 如: java.lang.Thread类中的MAX_PRIORITY等

扩展：

​	在以后的开发中很少单独使用static关键字或final关键字修饰成员变量，通常都是使用`public static final`共同修饰成员变量来表达常量的含义，常量的命名规则是：要求所有字母大写，不同单词之间采用下划线连接，如：

​	`public static final double PI= 3.14;`

# 面向对象的多态特性及抽象类和接口

### 一、多态

#### 代码案例

```
public class PersonWorkerTest {
    public static void main(String[] args) {
        // 1. 父类引用指向父类对象
        Person p = new Person("zhangfei", 30);
        p.show(); // 调用父类方法

        System.out.println("------------------------");

        // 2. 子类引用指向子类对象
        Worker w = new Worker("guanyu", 35, 4000);
        // 当子类没有重写show方法时，下面调用父类的show方法
        w.show();
        
        System.out.println("------------------------");
        // 3.声明父类类型的引用指向子类类型的对象，形成了多态”
        // 子类 is a 父类
        Person pw = new Worker("liubei",40,8000);
        // 当子类没有重写show方法时，下面调用父类的show方法
        // 当子类重写show方法后，下面调用子类的show方法
        // 在编译阶段调用父类中的show方法，在运行阶段调用子类重写的版本
        pw.show();
        
        System.out.println("------------------------");
        // 4.测试一下父类的引用是否能够调用父类独有的方法以及子类独有的方法
        String str1 = pw.getName();
        System.out.println("获取到的姓名是:" + str1);// liubei
        
        //pw.getSalary();error
        pw.test();
        Person.test();
        
        System.out.println("------------------------");
        // 5.若希望父类引用可以调用子类独有的方法，则需要强制类型转换
        // 从Person类型向Worker类型的转换，大到小的转换，强制类型转换
        int num=((Worker)pw).getsalary();
        System.out.println("获取到的薪水是:"+num);//8000
        
        // 从Person类型向string类型的转换编译报错
        // string str2=(string)pw;
        // 从Person类型向Teacher类型的转换编译通过，
        // 运行发生classcastException类型转换异常
        // Worker类型不能转换到Teacher类型
        // Teacher t=(Teacher)pw;
        if(pw instanceof Teacher) {
        	System.out.println("可以放心地转换了!");
        } else {
        	System.out.println("转换有风险，操作需谨慎!");
        }
    }
}
```



##### 基本概念

​	多态主要指同一种事物表现出来的多种形态。

​	饮料：可乐、雪碧、脉动、乐虎、红牛、...

​	宠物：狗、猫、鸟、乌龟、鱼、...

​	人：学生、教师、工人、...

##### 语法格式

​	父类类型 引用变量名 = new 子类类型();

##### 如：

​	Person pw=new Worker();

​	pw.show();

##### 解析：

​	编译阶段调用Person类中show方法，在运行阶段调用Worker类中重写以后的show方法

##### 使用场景

​	a.通过方法的参数传递形成多态。

​	public static void draw(Shape s){}

​	TestShape.draw(new Rect(1,2,3, 4));

​	

​	b.在方法体中直接使用多态的语法格式

​	TestAbstract ta=new SubTestAbstract();

​	ta.show();

##### 多态的效果

+ 当父类的引用指向子类的对象时，父类的引用可以直接调用父类独有的方法;
+ 当父类的引用指向子类的对象时，父类的引用不可以直接调用子类独有的方法；
+ 对于父子类都有的非静态成员方法来说，编译阶段调用父类版本，运行阶段调用子类重写以后的版本；
+ 对于父子类都有的静态方法来说，编译和运行阶段调用父类版本，隶属于类层级，因此与指向的对象无关；

##### 引用数据类型之间的转换

(1)引用数据类型之间的转换分为:自动类型转换，和强制类型转换。

​	其中自动类型转换主要指从小范围到大范围之间的转换，也就是子类到父类的转换

​	其中强制类型转换主要指从大范围到小范围之间的转换，也就是父类到子类的转换

(2)引用数据类型之间的转换必须发生在父子类之间，否则编译报错

(3)若转换到的目标类型是子类类型但不是该引用真正指向的子类类型，则编译通过，运行阶段发生类型转换异常。

(4)为了避免上述错误的发生，可以使用`instanceof`进行判断，具体格式如下:

​	if(引用变量名  `instanceof`  数据类型)	- 判断引用变量指向的对象是否为后面类型

```java
public class ShapeTest {
    // 自定义成员方法实现参数指定矩形特征的打印
    // 矩形类型的引用指向矩形自己的对象，没有多态
    // Rect r = new Rect(1, 2, 3, 4);

    public static void draw(Rect r) {
        // 最终调用矩形类中自己的show方法
        r.show();
    }
    // 自定义成员方法实现参数指定圆形特征的打印
    // 圆形类型的引用指向圆形的对象，没有多态
    // circle c=new circle(5,6,7);
	public static void draw(Circle c){
        c.show();
    }
    
    public static void main(String[] args) {
        ShapeTest.draw(new Rect(1, 2, 3, 4));
    }
}
```

##### 多态的意义

​	多态的实际意义在于可以屏蔽不同子类的差异性实现通用的编程，但可以调用不同的方法带来不同的结果。

### 二、抽象类

##### 抽象方法的概念

​	抽象方法就是指不能具体实现的方法，也就是没有方法体并使用abstract关键字修饰

##### 语法格式

​	访问控制符 返回值类型 方法名称 (形参列表)

##### 如：

​	public abstract void cry();

##### 抽象类的概念

​	抽象类就是指不能具体实例化的类，也就是不能创建对象并使用 `abstract` 关键字修饰

##### 注意事项

(1)抽象类中可以有成员变量、构造方法以及成员方法;

(2)抽象类中可以有抽象方法也可以没有抽象方法;

(3)拥有抽象方法的类必须是抽象类，因此严格来说，具有抽象方法并且使用abstract关键字修饰的类才算真正意义上的抽象类。

##### 实际意义

​	抽象类的意义不在于自身创建对象而在于被继承，当一个类继承抽象类后必须重写抽象类中的抽象方法，否则该类也变成抽象类

​	也就是说抽象类对子类具有强制性和规范性，因此叫做模板设计模式。

##### 经验分享

​	在以后的开发中推荐使用多态的语法格式，当父类的引用指向子类的对象时，那么父类引用直接调用的所有方法一定是父类拥有的方法，若希望更换子类时，只需要将new关键字后面的类型修改而其它地方无需更改立即生效，从而提高了代码的可维护性。

该方式的缺点就是：不能直接访问子类独有的方法，若访问则需要强转，

### 三、接口

##### 基本概念

接口就是一种比抽象类还抽象的类，体现为所有成员方法都是抽象方法。

定义类的关键字是`class`，而定义接口的关键字是`interface`。

继承类的关键字是`extends`，而实现接口的关键字是`implemets`。

##### 类和接口之间的关系

类和类之间的关系	使用`extends`关键字表达继承的关系	支持单继承

类和接口之间的关系	使用`implemets`关键字表达实现的关系	支持多实现

接口和接口之间的关系	使用extends关键字表达继承的关系	支持多继承

##### 抽象类和接口之间的区别

1)定义抽象类的关键字是`abstract class`，而定义接口的关键字是`interface`。

2)继承抽象类的关键字是`extends`，而实现接口的关键字是`implements`。

3)继承抽象类支持单继承，而实现接口可以多实现。

4)抽象类中可以有构造方法，而接口中不可以有构造方法。

5)抽象类中可以有成员变量，而接口中只可以有常量。

6)抽象类中可以有成员方法，而接口中只可以有抽象方法。

7)抽象类中增加方法可以不影响子类，而接口中增加方法通常都影响子类。

8)从`jdk1.8`开始允许接口中出现非抽象方法，但需要使用`defautt`关键字修饰。



### 四、匿名内部类

##### 基本概念

​	如果在一段程序中需要创建一个类的对象（通常这个类需要实现某个接口或者继承某个类），而且对象创建后这个类的价值也就不存在了，这个类可以不必命名，称之为匿名内部类。

##### 语法格式

​	接口/父类类型 引用变量名 = new 接口 / 父类类型 () {方法的重写};

##### 经验分享

当接口类型的引用作为方法的形参时，实参的传递方式有两种:

+ 自定义类实现接口，然后创建该类的对象作为实参传递；

+ 使用匿名内部类的语法格式来得到接口类型的引用；

##### 回调模式

​	回调模式是指：如果一个方法的参数是接口类型，则在调用该方法时，需要创建并传递一个实现此接口类型的对象，而该方法在运行时会调用到参数对象中所实现的方法（接口中定义的）。



#### 五、内部类

##### 基本概念

+ 当一个类的定义出现在另外一个类的类体中时，那么这个类叫做内部类，而这个内部类所在的类叫做外部类。

+ 类中的内容:成员变量、成员方法、构造方法、静态成员、构造块和静态代码块、内部类

##### 语法格式

​	class 外部类名 {

​		class 内部类名 {

​			内部类的类名;

​		}

​	}

##### 如：

​	class A {

​		class B {

​		}

​	}

##### 实际作用

+ 当一个类存在的价值仅仅是为某一个类单独服务时，那么就可以将这个类定义为所服务类中的内部类，这样可以隐藏该类的实现细节并且可以方便的访问外部类的私有成员而不再需要提供公有的get和set方法。

##### 基本分类

​	普通内部类	-  直接将一个类的定义放在另外一个类的类体中。

​	静态内部类	-  使用static关键字修饰的内部类，隶属于类层级。

​	局部内部类	-  直接将一个类的定义放在方法体的内部时。

​			  	 -  作用范围是从声明开始一直到方法体结束。



# Java的各种数据类型对象库的处理应用

### 一、Object类

#### 常用的包

+ java.lang 包 - 该包是Java语言中的核心包，该包中的内容由Java虚拟机自动导入的
  + 如：String类、System类等
+ java.util 包  - 该包是Java语言中的工具包，里面包含了大量的工具类和集合类等
  + 如：Scanner类、Random类等
+ java.io 包 - 该包是Java语言中的输入输出包，里面包含了大量读写文件的类等
  + 如：File0utputStream类、FileInputStream类等
+ java.net 包 - 该包是Java语言中的网络包，里面包含了大量网络编程的类等
  + 如：ServerSocket类、Socket类等如:ServerSocket类、Socket类等

​	… …

##### 基本概念

+ java.lang.Object类是所有类层次结构的根类，任何类都是该类的直接或间接事类

##### 常用的方法

Object()	- 使用无参方式构造对象。

boolean  equals(Object obj)	- 用于判断调用对象是否与参数对象相等。

	- 该方法默认比较两个对象的地址，与 == 运算符结果相同。
	- 为了使得该方法比较两个对象的内容，则需要重写该方法。
	- 若该方法重写后，则应该重写hashCode方法来维护hashCode方法的常规协定

int hashCode() - 用于获取调用对象的哈希码值（内存地址编号）。

	-  若调用equals方法的结果相等，则各自调用hashCode方法的结果相同。
	-  若调用equals方法的结果不相等，则各自调用hashCode方法的结果不相同。
	-  为了维护上述的常规协定与equals方法结果保持一致，就需要重写该方法

String toString()-用于获取对象的字符串形式

+ 该方法默认返回的字符串为: 包名.类名@哈希码值的十六进制形式
+ 为了返回更有意义的数据内容则需要重写该方法
+ 当使用print或println方法打印引用时，会自动调用toString方法

#### 代码案例

```java
public class Student {
    private int id;
    private String name;
    public Student() {
    	super();
    }
    
    public Student(int id , String name) {
    	super();
    	setId(id);
    	setName(name);
    }
    
    public int getId() {
        return id;
    }
    
    public void setId(int id) {
        if(id > 0) {
            this.id = id;
        } else {
            System.out.println("学号不合理！！！");
        }
    }
    
    public String getName() {
        return name;
    }
    
    public void setName(String name) {
        this.name = name;
    }
    
    public void show() {
        System.out.println("我叫" + getName() + "，学号是: " + getId());
    }
    
    @Override
    public boolean equals(Object obj){
        /*
        // 1.当调用对象和参数对象的地址相同，则内容一定相同
        if(this == obj){
    		return true;
        }   
        // 2.当调用对象不为空而参数对象为空时，则内容一定不相同
        if(null == obj){
    		return false;
        } 
        // 3.当参数对象和调用对象的类型相同时，才需要获取里面的内容比较
        if(obj instanceof Student){
			if(this.getId() == ((Student) obj).getId()){
            return true;
            } else {
                return false;
            }
        }
        // 4.若类型不相同则没有可比性，直接返回错误
    	return false;
        */
        if(this == obj)return true;
        if(null == obj)return false;
        if(obj instanceof student) {
            return this.getId()==((student)obj).getId();
        }
		return false;
    }    
    
    // 为了和equals方法保持一致，因此要重写该方法
    @Override
    public int hashCode(){
        // return getId();
        int type = 12;
        return type*31 + getId();
    }
    // 为了返回更有意义的数据内容，因此重写该方法
    @Override
    public String toString(){
    	return "student[id = getId()+ "，name + getName() + "]";
    }    
}
```

```java
public class StudentTest {
    public static void main(String[] args) {
        Student s1 = new Student(1001, "zhangfei");
        s1.show(); // 1001 zhangfei
        
        System.out.println("------------------------");
        
        Student s2 = new Student(1002, "guanyu");
        // 调用从Object类中继承下来的equals方法，默认比较对象的地址
        // 在equals方法的源码中：this就是s1，
        // 当student类中重写equals方法后，则调用重写以后的版本
        boolean b1 = s1.equals(new Person());
        System.out.println("b1 = " + b1); // b1 = false
        System.out.println(s1 == s2); // false 比较地址
        
        System.out.println("------------------------");
        // 调用从object类中继承下来的hashcode方法
        // 当student类中重写hashcode方法后，则调用重写的版本不再代表内存的编号
        int ia = s1.hashcode();
        System.out.println("对象s1的哈希码值为:" + ia);
        int ib = s2.hashcode();
        System.out.println("对象s2的哈希码值为:" + ib);
        
        System.out.println("------------------------");
        string str1= s1.tostring();
        System.out.println("str1 + str1");
        // cn.learn.day11.student@55D	Student[id =1001,name = zhangfei]
        System.out.println("str1 = " + str1);
        System.out.println("s2 = " + s2);	// 自动调用tostring方法
        System.out.println(s2);	// 自动调用tostring方法
    }
}
```

### 二、包装类和数字处理类

##### 如：

​	Person p=newPerson();	- 声明Person类型的引用指向Person类型的对象

​	int num = 10;			   - 声明int类型的变量num初始值为10

​	Java语言是一门纯面向对象的编程语言

​	public class MyInteger {

​		private int num =10;

​	}

​	MyInteger it = new MyInteger()

#### 包装类的概念

​	由于Java语言是一门纯面向对象编程语言，而8种基本数据类型声明的变量并不是对象，为了满足Java语言的特性就需要对这些变量进行对象化处理，而实现该功能的相关类就叫做包装类。

#### 包装类的分类

int => java.lang.Integer类

char => java.lang.Character类

其它类型对应的包装类就是将首字母变成大写

#### Integer类

##### 基本概念

​	java.lang.Integer类是int类型的包装类，里面包含了一个int类型的成员变量。

​	该类由final关键字修饰表示不能被继承。

##### 常用方法

​	Integer(int value)	- 根据参数指定的整数构造对象

​	Integer(String s)	  - 根据参数指定的字符串构造对象

​	该类重写了equals()、hashCode()、toString()方法

​	int intValue()	-用于获取调用对象中的整数数据并返回,

​	static Integer value0f(int)	  - 根据参数指定的整数返回对应的Integer对象

​	static int parseInt(String s)	-用于将String类型转换为int类型并返回。

```java
public class IntegerTest {
    public static void main(String[] args) {
        // 1. 构造Integer类型的对象并打印
        Integer it1 = new Integer(10);
        // 自动调用toString方法得到String类型的返回值
        System.out.println("it1 = " + it1); // it1 = 10

        Integer it2 = new Integer("20");
        // 编译ok，运行产生NumberFormatException数字格式异常
        // Integer it2 = new Integer("20a"); 

        System.out.println("it2 = " + it2); // it2 = 20	String
        
        System.out.println("------------------------");
        // 2.调用成员方法进行测试
        //相当于实现了从Integer类型到int类型的转换，叫做拆箱
        int res = it2.intValue();
        System.out.println("获取到的整数值是:" + res); // 20 int
        //相当于实现了从int类型到Integer类型的转换，叫做装箱
        Integer it3 =Integer.valueOf(res);
        System.out.println("it3 = " + it3);// it3=20 string
        res = Integer.parseInt("12345");
        System.out.println("转换的整数数据是:" + res); // 12345 int类型
        /string str1= string.valueOf(res);
        String str1 ="" + res;
        System.out.println("转换的字符串数据是:"+str1);// 12345 string类型
        
        System.out.println("------------------------");
        //从jdk1.5开始增加了新特性:自动装箱和自动拆箱
        Integer it4 = 10;//自动装箱
        res = it4;//自动拆箱
    }
}
```

#### BigDecimal类

##### 基本概念

​	由于float类型和double类型的运算肯能会有所误差，为实现精确运算则需要借助Java.math.BigDecimal类型加以描述

##### 常用方法

 BigDecimal(String val)	- 根据参数指定的字符串构造对象,

BigDecimal add(BigDecimal augend)

​	- 用于计算调用对象和参数对象的和并返回

BigDecimal subtract(BigDecimal subtrahend)

​	-  用于计算调用对象和参数对象的差并返回

BigDecimal multiply(BigDecimalmultiplicand)

​	- 用于计算调用对象和参数对象的积并返回。

BigDecimal divide(BigDecimal divisor)

​	- 用于计算调用对象和参数对象的商并返回

#### String类

#### 代码案例

```java
// String类型的常量池
public class StringPoolTest {
    public static void main(String[] args) {
        String str1 = "abc";
        System.out.println("str1 = " + str1); // str1 = abc
        
        String str2 = "abc";
        System.out.println(str1 == str2); // 关系运算符 比较地址 true
        
        System.out.println("----------------------");
        
        String str3 = "123";
        System.out.println(str3 == str1); // 比较地址 false
    }
}
```



```java
// String类型的构造方法
public class StringConstructorTest {
    public static void main(String[] args) {
        // 1.使用无参方式构造String类型的对象并打印 "" null
        String str1 = new String();
        System.out.println("str1 = " + str1); // str1=啥也没有
        
        System.out.println("------------------------");
        
        // 2.使用字节数组来构造String对象并打印
        byte[] bArr = {97, 98, 99, 100, 101};
        // 表示使用bArr数组中下标从1开始的3个字节来构造字符串对象
        String str2 = new String(bArr, 1, 3);
        System.out.println("str2 = " + str2); // str2 = bcd
        String str3 = new String(bArr);
        System.out.println("str3 = " + str3); // str3 = abcde
        
        System.out.println("------------------------");
        // 3.使用字符数组来构造string对象并打印
        char[] cArr = {'h', 'e', 'l', 'l', 'o'};
        
        // 使用cArr数组中从下标1开始的2个字符构造字符串
        String str4 = new String(cArr, 1, 2);
        System.out.println("str4 = " + str4); // str4 = el
        
        // 使用整个cArr数组构造字符串
        String str5 = new String(cArr);
        System.out.println("str5 = " + str5); // str5 = hello
        
        System.out.println("--------------------------------------------------");
        
        // 4.使用字符串字面量构造String对象
        String str6 = new String("world");
        System.out.println("str6 = " + str6); // str6 = world
    }
}
```



##### 基本概念

​	java.lang.String类用于描述字符串，Java应用程序中所有字符串字面值都可以作为String类型的对象加以描述，如:"abc"等。java.lang.String类用于描述字符串，Java应用程序中所有字符串字面值都可以作为String类型的对象加以描述，如:"abc"等。

该类描述的字符串内容是个常量，一旦创建完毕后则不能更改，因此可以被共享。

##### 如：

​	String str1 =" abc "

​	str1 = " 123 "	- 改变str1的指向而不是指向的内容

#### 常量池

​	由于String类型描述的字符串内容是个常量不可改变，因此Java虚拟机提供了一个常量池，当Java程序中出现字符串内容时就放入常量池中，若后续出现重复的字符串内容则直接使用池中已有的对象而不需再次创建，从而提高了性能。



# Java字符串和日期处理

### 一、String类型的常用方法

##### String定义有charAt方法:

​	char  charAt (int index)	- 方法charAt用于返回字符串指定位置的字符。参数index表示指定的位置

​	int lengtht	- 返回字符串字符序列的长度

#### 代码案例

```java
public class stringcharTest {
	public static void main(String[] args) {
        // 1.构造String类型的对象
        String str1 = new String("hello");

        // 2.获取字符串的长度以及每个字符的内容
        System.out.println("字符串的长度是：" + str1.length()); // 5
        System.out.println("下标为0的字符是：" + str1.charAt(0)); // 'h'
        System.out.println("下标为1的字符是：" + str1.charAt(1)); // 'e'
        System.out.println("下标为2的字符是：" + str1.charAt(2)); // 'l'
        System.out.println("下标为3的字符是：" + str1.charAt(3)); // 'l'
        System.out.println("下标为4的字符是：" + str1.charAt(4)); // 'o'
        
        // 注意：下面这行代码会抛出StringIndexOutOfBoundsException异常
        // 因为"hello"的长度是5，有效下标范围是0-4
        System.out.println("下标为5的字符是：" + str1.charAt(5));
        
        System.out.println("--------------------------------------------------");
        
        // 使用for循环打印所有字符
        for(int i = 0; i < str1.length(); i++) {
            System.out.println("下标为" + i + "的字符是：" + str1.charAt(i));
        }
        
        System.out.println("--------------------------------------------------");
        
        // 练习：使用两种方式实现将字符串"12345"转换为整数12345并打印
        String str2 = new String("12345");
        
        // 方式一：调用Integer类中的parseInt方法进行转换
        int ia = Integer.parseInt(str2);
        System.out.println("转换后的结果是：" + ia); // 12345
        
        System.out.println("--------------------------------------------------");
        
        // 方式二：取出字符串中的每个字符并转换为整数数据再合并起来
        int res =0;
        for(int i=0; i< str2.length(); i++){
			res =res*10+(str2.charAt(i) -'0');//res=1; res=12; res=123;
		}
        System.out.println("转换后的结果是：" + ib); // 12345
    }
}
```

#### String类型中多个方法的使用

```java
public class StringMethodDemo {
    public static void main(String[] args) {
        // 1.构造String类型的对象
        String str1 = new String("Let Me Give You Some Color To See See!");

        // 2.调用成员方法进行测试
        // 判断是否包含参数指定的内容
        boolean b1 = str1.contains("some");
        System.out.println("b1 = " + b1); // b1 = false
        
        b1 = str1.contains("Some");
        System.out.println("b1 = " + b1); // b1 = true

        System.out.println("----------------------");

        // 将所有字符转换为小写
        String str2 = str1.toLowerCase();
        System.out.println("str1 = " + str1); // 原字符串不变
        System.out.println("str2 = " + str2); // 转换为小写后的字符串
        
        System.out.println("----------------------");
        
        // 转换为大写
        String str3 = str1.toUpperCase();
        System.out.println("str1 = " + str1);
        System.out.println("str3 = " + str3); // 转换为大写后的字符串
        
        System.out.println("----------------------");
        
        // 去除两端的空白字符
        String str4 = str1.trim();
        System.out.println("str1 = " + str1);
        System.out.println("str4 = " + str4); // 去除两端的空白字符
        
        System.out.println("------------------------");
        
        // 判断字符串是否以...开头和结尾
        boolean b1 = str1.startsWith("Let");
        System.out.println("b1 = " + b1); // false
        
        b1 = str1.startsWith(" ");
        System.out.println("b1 = " + b1); // true
        
        b1 = str1.endsWith("See!");
        System.out.println("b1 = " + b1); // true
    }
}
```

#### String类中的equals实现登录

+ String类重写了继承自0bject的equals方法，其逻辑为:字符序列相同的String对象equals返回true。
+ 通常使用equals方法判断两个字符串的字符序列是否相同。
+ String还提供`equalslgnoreCase`方法，该方法在判断时将忽略大小写

```java
import java.util.Scanner;

public class LoginSystem {
    public static void main(String[] args) {
        // 创建Scanner对象用于接收用户输入
        Scanner sc = new Scanner(System.in);
        
        // 给予用户3次登录尝试机会
        for(int i = 3; i > 0; i--) {
            // 1.提示用户输入用户名和密码信息
            System.out.println("请输入用户名和密码信息：");
            
            // 获取用户输入
            String userName = sc.next();
            String passWord = sc.next();
            
            // 2.验证用户名和密码
            if("admin".equals(userName) && "123456".equals(passWord)) {
                System.out.println("登录成功！欢迎使用...");
                break; // 登录成功，退出循环
            } else {
                // 计算剩余尝试次数
                int remainingAttempts = i - 1;
                System.out.println("用户名或密码错误！您还有" + remainingAttempts + "次机会！");
            }
        }
        
        // 关闭Scanner
        sc.close();
    }
}
```

#### String类中的indexOf方法

+ indexOf方法用于实现在学符串中检索另外一个字串。
+ String提供几个重载的indexOf方法：
  + int indexOf(String str)	- 在字符串中检索st，返回发第、出现的位置，如果找不到则返回-1
  + int indexOf(String str,int fromIndex)	- 类似indexOf(String)，但是是从字符串的fromIndex位置开始检索

#### 代码案例

```java
public class StringIndexOfDemo {
    public static void main(String[] args) {
        // 1.构造String类型的对象
        String str1 = new String("Good Good Study, Day Day Up!");

        // 2.调用indexOf方法查找指定字符串内容
        // 查找"good"（区分大小写）
        int pos = str1.indexOf("good");
        System.out.println("pos = " + pos); // pos = -1（未找到）
        
        // 查找"Good"（从开头查找）
        pos = str1.indexOf("Good");
        System.out.println("pos = " + pos); // pos = 0（首次出现在开头）
        
        // 从下标0开始查找"Good"
        pos = str1.indexOf("Good", 0);
        System.out.println("pos = " + pos); // pos = 0
        
        // 从下标1开始查找"Good"
        pos = str1.indexOf("Good", 1);
        System.out.println("pos = " + pos); // pos = 5（第二次出现的位置）
        
        // 补充：查找不存在的字符串
        pos = str1.indexOf("Hello");
        System.out.println("pos = " + pos); // pos = -1
        
        // 补充：查找单个字符
        pos = str1.indexOf('D');
        System.out.println("pos = " + pos); // pos = 10
    }
}
```

#### String类中的subString方法

substring方法用于返回一个字符串的子字符串。

substring常用重载方法定义如下:

|                     方法签名                     |                           功能描述                           |
| :----------------------------------------------: | :----------------------------------------------------------: |
| `String substring(int beginIndex, int endIndex)` | 返回字符串中从下标`beginIndex`（包括）开始到`endIndex`（不包括）结束的子字符串 |
|        `String substring(int beginIndex)`        | 返回字符串中从下标`beginIndex`（包括）开始到字符串结尾的子字符串 |

#### 代码案例

```java
public class SubstringDemo {
    public static void main(String[] args) {
        String str = "Hello, World!";
        
        // 使用两个参数的substring方法
        String sub1 = str.substring(7, 12); // "World"
        System.out.println(sub1);
        
        // 使用一个参数的substring方法
        String sub2 = str.substring(7); // "World!"
        System.out.println(sub2);
    }
}
```

##### 注意事项：

1. `beginIndex`必须是非负且小于字符串长度
2. `endIndex`必须大于`beginIndex`且不超过字符串长度
3. 如果参数超出范围会抛出`StringIndexOutOfBoundsException`异常



### 二、StringBuilder类和StringBuffer类

##### 如：

​	`String str1  = "ab";`

​	`String str2  = "abc";`

​	`String str3  = "abcd";`

​	……

##### 基本概念

​	由于`String`类型描述的字符串内容是个常量不可更改，当程序中出现大量类似的字符串时需要单独存放从而浪费内存空间，若希望使用一块内存空间进行存储并且可以修改字符串内容，则应该使用`StringBuilder`类和`StringBuffer`类

​	其中`StringBuffer`类从jdk1.0始存在，该类支持线程安全，因此访问的效率比较低

​	其中`StringBuilder`类从jdk1.5开始存在，该类不支持线程安全，访问的效率比较高

#### 代码案例

```java
public class StringBuilderCrudDemo {
    public static void main(String[] args) {
        // 1. 初始化（原图代码）
        String str1 = "hello";
        System.out.println("str1 = " + str1); // hello
        
        StringBuilder sb1 = new StringBuilder(str1);
        
        // 2. 增：插入操作（原图代码）
        StringBuilder sb2 = sb1.insert(0, "abcd");
        System.out.println("插入开头后: " + sb1); // abcdhello
        
        sb1.insert(4, "1234");
        System.out.println("插入中间后: " + sb1); // abcd1234hello
        
        sb1.insert(sb1.length(), "ABCD");
        System.out.println("插入末尾后: " + sb1); // abcd1234helloABCD
        
        // 3. 增：追加操作（原图代码）
        sb1.append("world");
        System.out.println("追加后: " + sb1); // abcd1234helloABCDworld
        System.out.println("当前容量: " + sb1.capacity()); // 扩容后的容量
        
        // 4. 删：删除操作（新增）
        sb1.delete(4, 8); // 删除"1234"
        System.out.println("删除4-8后: " + sb1); // abcdhelloABCDworld
        
        sb1.deleteCharAt(0); // 删除首字符
        System.out.println("删除首字符后: " + sb1); // bcdhelloABCDworld
        
        // 5. 改：替换操作（新增）
        sb1.replace(1, 4, "***"); // 替换第1-3字符
        System.out.println("替换1-4后: " + sb1); // b***helloABCDworld
        
        sb1.setCharAt(0, 'A'); // 修改单个字符
        System.out.println("修改首字符后: " + sb1); // A***helloABCDworld
        
        // 6. 查：查询操作（新增）
        System.out.println("第5个字符: " + sb1.charAt(4)); // h
        System.out.println("hello的位置: " + sb1.indexOf("hello")); // 5
        System.out.println("长度: " + sb1.length()); // 17
        
        // 7. 其他操作（保持原图扩容说明）
        System.out.println("最终结果: " + sb1);
        System.out.println("最终容量: " + sb1.capacity()); 
        /* 扩容机制说明（原图注释保留）：
           初始容量 = 原字符串长度 + 16
           扩容公式：newCapacity = (oldCapacity * 2) + 2 */
    }
}
```

##### 方法说明：

| 操作类型 |       方法       |        说明        |
| :------: | :--------------: | :----------------: |
|  **增**  |    `append()`    |   在末尾追加内容   |
|          |    `insert()`    | 在指定位置插入内容 |
|  **删**  |    `delete()`    | 删除指定范围的字符 |
|          | `deleteCharAt()` | 删除指定位置的字符 |
|  **改**  |   `replace()`    | 替换指定范围的内容 |
|          |  `setCharAt()`   | 修改指定位置的字符 |
|  **查**  |    `charAt()`    | 获取指定位置的字符 |
|          |   `indexOf()`    |    查找子串位置    |
|          |  `substring()`   |    获取子字符串    |
|   其他   |   `reverse()`    |     反转字符串     |
|          |    `length()`    |      获取长度      |
|          |   `toString()`   |   转为String对象   |

#### StringBuilder实现字符串内容的反转和相互转换

##### StringBuilder类的常用方法如下：

| StringBuilder类的常用方法                              | 功能描述   |
| :----------------------------------------------------- | ---------- |
| `StringBuilder append(String str)`                     | 追加字符串 |
| `StringBuilder insert(int offset,String str)`          | 插入字符串 |
| `StringBuilder delete(int start,int end)`              | 删除字符串 |
| `StringBuilder replace(int start,int end, String str)` | 替换字符串 |
| `StringBuilder reverse()`                              | 字符串反转 |

##### 返回值的意义

+ `StringBuilder`的很多方法的返回值均为`StrngBuider`类型。这些方法的返回语句均为: `return this.`
+ 可见，这些方法在对StringBuilder所封装的字符序列进行改变后又返回了该对象的引用。基于这样的设计的目的在于可以按照如下简洁的方式书写代码:

`sb.append("ibm").append("java").insert(3,"oracle").replace(9, 13, "JAVA");System.out.println(sb.toString());`



# 包装类、集合、数据结构

### 一、集合(容器)框架

##### 集合的由来

+ 当需要在程序中记录单个数据内容时，则声明一个变量即可；

+ 当需要在程序中记录多个类型相同的数据内容时，则声明一个一维数组即可；

+ 当需要在程序中记录多个类型不同的数据内容时，则构造一个对象即可；

+ 当需要在程序中记录多个类型相同的对象时，则声明一个对象数组即可；
+ 当需要在程序中记录多个类型不同的对象时，则声明一个集合即可；

##### 集合框架结构

+ 在Java语言中集合框架的顶层是:java.util.Collection集合和java.util.Map集合

+ 其中Co1lection集合中操作元素的基本单位是：单个元素

+ 其中Map集合中操作元素的基本单位是：单对元素。

在以后的开发中很少直接使用Co1lection集合，而是使用该集合的子集合:List集合Queue集合、Set集合等。

### 二、Collection集合

##### 基本概念

`java.util.Collection`集合是集合框架的根接口，其它接口是该接口的子接口。

##### 常用的方法

| boolean add(E e);           | 向集合中添加对象     |
| --------------------------- | -------------------- |
| boolean contains(Object o); | 判断是否包含指定对象 |
| boolean remove(Object o);   | 从集合中删除对象     |
| void clear();               | 清空集合             |
| int size();                 | 返回包含对象的个数   |
| boolean isEmpty();          | 判断是否为空         |

#### 代码案例

```java
import java.util.ArrayList;
import java.util.Collection;

public class CollectionTest {

    public static void main(String[] args) {
        // 1.声明Collection类型的引用指向实现类ArrayList的对象
        // 接口类型的引用指向实现类的对象，形成了多态
        Collection c1 = new ArrayList();

        // 2.调用方法实现元素的添加
        boolean b1 = c1.add(new String("one"));
        System.out.println("b1 = " + b1); // b1 = true
        // 自动调用toString方法，最终调用实现类中的toString方法
        // 该方法的默认打印格式为：[元素1,元素2,...]
        System.out.println("c1 = " + c1); // c1 = [one]
		
        b1 = c1.add(new Integer(2));
        System.out.println("b1="+ b1); // b1 = true
        System.out.println("c1="+c1); //c1 =[one, 2]
        
        b1 = c1.add(new student(1001,"zhangfei",30));
        System.out.println("bl="+b1);// b1 = true
        // [one,2,student [id=1001,name=zhangfei,age=30]]
        //打印集合的本质就是打印每个元素值，本质上就是调用元素对应的toString方法
        
        System.out.println("-------------------------------------");
        // 3.调用方法实现查找的功能
        b1 = c1.contains(new Integer(1));
        System.out.println("b1 =" + b1); // false
        
        b1 = c1.contains(new Integer(2));
        System.out.println("b1 =" + b1); // true
        
        contains方法的执行原理:(o==null ?e==null :o.equals(e))
        //若传入的实参对象为nu11,则判断集合中所有元素是否有null值
        // 若传入的实参对象不为nu11，则使用参数对象调用equals方法与集合中
        // 元素依次比较是否相等
        // 当Student类中没有重写equals方法时，调用从Object继承的版本比较地址
        // 若希望比较两个对象的内容，则应该重写equals方法
        // 当Student类中重写equals方法后，调用重写的版本 比较内容
        b1 = c1.contains(new student(1001,"zhangfei",30));
        System.out.println("bl="+ b1);//false true
        
        System.out.println("-------------------------------------");
        
        // 4.调用方法实现删除的操作
        // [one, 2, Student [id=1001, name=zhangfei, age=30]]
        boolean b1 = c1.remove(new String("two"));
        System.out.println("b1 = " + b1); // b1 = false
        // [one, 2, Student [id=1001, name=zhangfei, age=30]]
        System.out.println("c1 = " + c1);

        b1 = c1.remove(new String("one"));
        System.out.println("b1 = " + b1); // b1 = true
        // [2, Student [id=1001, name=zhangfei, age=30]]
        System.out.println("c1 = " + c1);

        // 调用方法实现清空集合
        c1.clear();
        System.out.println("c1=" + c1);// c1=[啥也没有]
    }
}
```



### 三、List集合

##### 基本概念

+ java.util.List集合是Collection集合的子集合，该集合中元素有先后次序且允许重复
+ 该集合的主要实现类有:`ArrayList`类、`LinkedList`类、`Stack`类、`Vector`类等
+ 其中`ArrayList`类的底层是采用动态数组进行数据管理，访问方便，增删不方便
+ 其中`LinkedList`类的底层是采用链表进行数据管理，增删方便，访问不方便
+ 其中`Stack`类主要用于描述具有后进先出特征的数据结构，叫做栈，`last in first out` 该类的底层是采用数组进行数据的管理。
+ 其中`Vector`类的底层采用数组进行数据的管理，与`ArrayList`类相比属于线程安全的类因此效率比较低，在以后的开发中推荐使用`ArrayList`类取代之。

##### 常用方法

+ `List`除了继承`Collection`定义的方法外，还根据其线性表的数据结构定义了-系列方法:其中最常用的就是基于下标的`get`和`set`方法。

|                        方法签名                        |         功能描述         |
| :----------------------------------------------------: | :----------------------: |
|            `void add(int index, E element)`            | 向集合中指定位置添加元素 |
| `boolean addAll(int index, Collection<? extends E> c)` |   向集合中添加所有元素   |
|                   `E get(int index)`                   | 从集合中获取指定位置元素 |
|             `E set(int index, E element)`              |    修改指定位置的元素    |
|                 `E remove(int index)`                  |    删除指定位置的元素    |

##### 代码案例

```java
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class ListOperationsExample {
    public static void main(String[] args) {
        // 1. 创建List集合
        List<String> list = new ArrayList<>();
        
        // 2. 增操作
        list.add("Apple");       // 末尾添加
        list.add(0, "Banana");   // 指定位置添加
        list.addAll(List.of("Orange", "Grape")); // 批量添加
        System.out.println("添加元素后: " + list); // [Banana, Apple, Orange, Grape]
        
        // 3. 删操作
        list.remove("Apple");                // 按元素删除
        list.remove(0);                      // 按索引删除
        list.removeAll(List.of("Grape"));    // 批量删除
        System.out.println("删除元素后: " + list); // [Orange]
        
        // 4. 改操作
        list.set(0, "Peach"); // 修改指定位置元素
        System.out.println("修改元素后: " + list); // [Peach]
        
        // 5. 查操作
        boolean contains = list.contains("Peach"); // 判断包含
        String element = list.get(0);              // 获取元素
        int index = list.indexOf("Peach");        // 获取索引
        System.out.println("查询结果: 包含Peach-" + contains + 
                         ", 首元素-" + element + 
                         ", Peach索引-" + index);
        
        // 6. 遍历操作
        System.out.println("\n遍历方式1: for循环");
        for (int i = 0; i < list.size(); i++) {
            System.out.println(list.get(i));
        }
        
        System.out.println("\n遍历方式2: 增强for循环");
        for (String fruit : list) {
            System.out.println(fruit);
        }
        
        System.out.println("\n遍历方式3: 迭代器");
        Iterator<String> it = list.iterator();
        while (it.hasNext()) {
            System.out.println(it.next());
        }
        
        System.out.println("\n遍历方式4: forEach + Lambda");
        list.forEach(System.out::println);
    }
}
```



### 四、泛型机制

##### 基本概念

​	通常情况下集合中可以存放不同类型的对象，本质上是将这些对象全部看做`Object`类型放入的，因此从集合中取出元素时也是`Object`类型，为了表达元素最真实的数据类型就需要强制类型转换，而强制类型转换可能发生类型转换异常。

​	为了避免上述错误的发生，从jdk1.5开始提出泛型机制，也就是在集合名称的右侧使用<数据类型>的方式明确要求该集合可以存放的元素类型，若放入其它类型则编译报错

##### 如：

​	List It1 = new LinkedList();	- 可以放入任意类型对象，取出麻烦

​	List< String > It1 = new LinkedList< String >();	- 只能放入String类型，取出方便

#### 代码案例

```java
import java.util.LinkedList;
import java.util.List;

public class ListExample {
    public static void main(String[] args) {
        // 1. 使用泛型机制声明List集合的引用指向实现类的对象
        List<String> lt1 = new LinkedList<String>();
        
        // 2. 放入元素并打印
        lt1.add("one");
        lt1.add("two");
        System.out.println("lt1 = " + lt1); // [one, two]
        System.out.println("----------------------");
        
        // 3. 取出元素并打印
        String str1 = lt1.get(0);
        System.out.println("取出的元素是：" + str1); // one
        System.out.println("----------------------");
        // 从jdk1.7开始增加新特性:后面<>中的数据类型可以省略菱形特性
        // List<Integer> lt2 = new LinkedList<Integer>();
        List<Integer> lt2 = new LinkedList<>();
    }
}
```

##### 原理分析

​	泛型的本质就是参数化类型，也就是让数据类型作为参数传递，集合定义中的E相当于形式参数负责占位，而使用集合时<>中的数据类型相当于实际参数负责给形式参数初始化当初始化完毕后所有E被替换为实际参数表示的类型进行使用。

​	由于E支持的数据类型非常广泛，因此得名为"泛型"。

##### 如：

​	// 其中i叫做形式参数，负责占位						其中E叫做形式参数，负责占位

​	// int i= 5;											E = String;

​	// int i = 10;										     E = String;	

​	public static void show( int i ){						    public interface List(E) {

​		......											   	...

​	}													}

​	// 其中5叫做实际参数，用于给形式参数初始化			  其中String叫做实际参数

​	show(5);											   List< String > lt1 = ... ;

​	show(10);											 List< Student > lt2 = ... ;



# Java中的数据结构

### 一、Queue集合

##### 基本概念

+ `java.util.Queue`集合是`Collection`集合的子集合，与`List`集合是平级关系。
+ 该集合的主要实现类是:`Linkedist`类，因为该类在增删方面有一定的优势。
+ 该集合用于描述具有先进先出特征的数据结构，叫做队列( first in first out )

#### 代码案例

```java
import java.util.LinkedList;
import java.util.Queue;

public class QueueTest {
    public static void main(String[] args) {
        // 1. 声明Queue类型的引用指向实现类的对象
        Queue<Integer> q1 = new LinkedList<Integer>();

        // 2. 将数据11、22、33、44、55依次放入队列中
        for(int i = 1; i <= 5; i++) {
            boolean b1 = q1.offer(i * 11);
            
            System.out.println("b1 = " + b1);
            System.out.println("队列中的元素有：" + q1); // [11, 22, 33, 44, 55]
        }
        
        // 3. 获取队首元素并打印
        Integer head = q1.peek();
        System.out.println("队首元素为：" + head); // 11
        
        // 4. 将队列中的所有元素依次删除并打印
        System.out.println("\n依次删除元素：");
        while(!q1.isEmpty()) {
            Integer removed = q1.poll();
            System.out.println("删除元素：" + removed + "，剩余队列：" + q1);
        }
        
        // 5. 打印队列中最终的所有元素
        System.out.println("\n最终队列中的元素：" + q1); // []
    }
}
```

##### 主要方法

|       方法签名       |                  方法说明                  |
| :------------------: | :----------------------------------------: |
| `boolean offer(E e)` | 将一个对象添加至队尾，若添加成功则返回true |
|      `E poll()`      |          从队首删除并返回一个元素          |
|      `E peek()`      |        返回队首的元素（但并不删除）        |

### 二、Set集合

##### 基本概念

+ `java.util.Set`集合是`Collection`集合的子集合，与`List`集合以及`Queue`集合平级关系
+ 该集合与`List`集合的主要区别在于:元素没有先后次序并且不允许重复的元素
+ 该集合的主要实现类有:`HashSet`类和`TreeSet`类
+ 其中`Hashset`类的底层采用哈希表进行数据管理的。
+ 其中`TreeSet`类的底层采用二叉树进行数据管理的。

#### 代码案例

```java
import java.util.HashSet;
import java.util.Iterator;
import java.util.Set;

public class SetExample {
    public static void main(String[] args) {
        // 原始代码：初始化Set集合
        Set<String> s1 = new HashSet<>();
        s1.add("two");
        s1.add("one");
        s1.add("three");
        
        // 场景1：使用迭代器遍历Set集合
        System.out.println("\n1. 使用迭代器遍历Set集合：");
        Iterator<String> iterator = s1.iterator();
        while(iterator.hasNext()) {
            System.out.println(iterator.next());
        }

        // 场景2：方式一实现toString功能（直接拼接）
        System.out.println("\n2. 迭代器实现toString方式一：");
        System.out.println(setToString1(s1)); // [one, two, three]

        // 场景3：方式二实现toString功能（StringBuilder）
        System.out.println("\n3. 迭代器实现toString方式二：");
        System.out.println(setToString2(s1)); // [one, two, three]

        // 场景4：迭代过程中删除元素
        System.out.println("\n4. 迭代删除元素(two)：");
        removeElement(s1, "two");
        System.out.println("删除后集合：" + s1); // [one, three]
    }

    // 方式一：直接字符串拼接实现toString
    private static String setToString1(Set<?> set) {
        if(set.isEmpty()) return "[]";
        
        Iterator<?> it = set.iterator();
        String result = "[" + it.next();
        while(it.hasNext()) {
            result += ", " + it.next();
        }
        return result + "]";
    }

    // 方式二：使用StringBuilder实现toString
    private static String setToString2(Set<?> set) {
        StringBuilder sb = new StringBuilder("[");
        Iterator<?> it = set.iterator();
        while(it.hasNext()) {
            sb.append(it.next());
            if(it.hasNext()) sb.append(", ");
        }
        return sb.append("]").toString();
    }

    // 使用迭代器安全删除元素
    private static void removeElement(Set<String> set, String target) {
        Iterator<String> it = set.iterator();
        while(it.hasNext()) {
            if(it.next().equals(target)) {
                it.remove(); // 安全删除当前元素
                break;
            }
        }
    }
}
```

#### HashSet集合放入元素的过程

1. 先调用元素的hashCode()方法得到哈西码，通过算法算在哈西表中的位置。
2. 如果该位置没有元素，直接放入即可。
3. 如果该位置有元素，调用元素的equals()方法比较是不是相等。
4. 如果相等，则保留旧元素丢弃新元素。
5. 如果不相等，则放入该位置的链表中一个元素

#### Set集合的遍历

+ 所有`Collectiom`的实现类都实现了其`Iterato`方法，该方法返回一个口类型的对象，用于实现对集合元素的迭代遍历。
+ lterator接口的主要方法有：

|      方法签名       |              功能描述               |
| :-----------------: | :---------------------------------: |
| `boolean hasNext()` | 判断集合中是否有可以迭代/访问的元素 |
|     `E next()`      |  用于取出一个元素并指向下一个元素   |
|   `void remove()`   |    用于删除访问到的最后一个元素     |

#### 增强版的for循环（for each结构）

##### 语法格式

​	for (元素类型  变量名  :  数组名/集合名) {

​		循环体;

​	}

##### 执行流程

​	不断地从数组或集合中取出一个元素并赋值给变量并执行循环体，直到处理完毕所有元素为止。



### 三、Map集合

##### 基本概念

+ `java.util.Map<K,V>`集合中操作元素的基本单位是:单对元素，其中类型参数如下:
  + K	- 此映射所维护的键(key)的类型
  + V	- 映射值(value)的类型
+ 该集合中不允许出现重复的键，每个键最多只能映射到一个值。
+ 该集合的主要实现类有：`HashMap`类和`TreeMap`类。
+ 其中`HashMap`类的底层是采用哈希表进行数据管理的。
+ 其中`TreeMap`类的底层是采用“又树进行数据管理的。

##### Map集合实现增删改查以及遍历的代码案例

```java
import java.util.HashMap;
import java.util.Map;

public class MapTest {
    public static void main(String[] args) {
        // 1. 声明Map集合
        Map<Integer, String> m1 = new HashMap<>();
        
        // 2. 增操作
        System.out.println("===== 增操作 =====");
        String str1 = m1.put(1, "one");
        System.out.println("str1 = " + str1); // null（首次添加返回null）
        System.out.println("集合内容：" + m1);  // {1=one}

        str1 = m1.put(2, "two");
        System.out.println("str1 = " + str1); // null
        System.out.println("集合内容：" + m1);  // {1=one, 2=two}

        str1 = m1.put(2, "TWO"); // 测试key重复
        System.out.println("str1 = " + str1); // two（返回旧值）
        System.out.println("集合内容：" + m1);  // {1=one, 2=TWO}

        // 3. 删操作
        System.out.println("\n===== 删操作 =====");
        String removed = m1.remove(1);
        System.out.println("删除key=1的值：" + removed); // one
        System.out.println("集合内容：" + m1);  // {2=TWO}

        boolean isRemoved = m1.remove(2, "two");
        System.out.println("按kv删除结果：" + isRemoved); // false（值不匹配）
        System.out.println("集合内容：" + m1);  // {2=TWO}

        // 4. 改操作
        System.out.println("\n===== 改操作 =====");
        m1.replace(2, "NEW TWO");
        System.out.println("修改后集合：" + m1); // {2=NEW TWO}

        boolean isReplaced = m1.replace(2, "TWO", "NEW TWO");
        System.out.println("条件替换结果：" + isReplaced); // false（旧值不匹配）
        
        // 5. 查操作
        System.out.println("\n===== 查操作 =====");
        System.out.println("获取key=2的值：" + m1.get(2)); // NEW TWO
        System.out.println("检查key=3是否存在：" + m1.containsKey(3)); // false
        System.out.println("检查值'NEW TWO'是否存在：" + m1.containsValue("NEW TWO")); // true
        
        // 6. 遍历操作（补充）
        System.out.println("\n===== 遍历操作 =====");
        m1.put(3, "three");
        System.out.println("方式1：entrySet遍历");
        for(Map.Entry<Integer, String> entry : m1.entrySet()) {
            System.out.println(entry.getKey() + "=" + entry.getValue());
        }
        
        System.out.println("\n方式2：keySet遍历");
        for(Integer key : m1.keySet()) {
            System.out.println(key + "=>" + m1.get(key));
        }
    }
}
```



### 四、异常机制

##### 基本概念

+ 异常就是"不正常"的含义，在Java语言中用于表示运行阶段发生的错误。
+ `java. lang. Throwable`类是`Java`语言中所有错误(`Error`)和异常(`Exception`)的超类。
+ 其中`Error`类主要用于描述比较严重无法编码解决的问题，如:JVM挂了
+ 其中`Exception`类主要用于描述比较轻微可以编码解决的问题，如:0作为除数。

##### 基本分类

+ `java.lang.Exception`类是所有异常类的超类，主要分为以下两大类：
  + `RuntimeException`		- 运行时异常，也叫作非检测性异常
  + `IOException`和其它异常	- 其它异常，也叫作检测性异常
    + 所谓检测性异常就是在编译阶段能够被编译器检测出来的异常
+ 其中`RuntimeException`类的主要子类：
  + `ArithmeticException`	- 算术异常
  + `ArrayIndexOutOfBoundsException`  - 数组下标越界异常
  + `NullPointerException`	- 空指针异常
  + `ClassCastException`	- 类型转换异常
  + `NumberFormatException`	- 数字格式异常

##### 注意

​	当程序执行过程中发生异常但没有手动处理时，由Java虚拟机采用默认方式处理，而默认处理方式就是:打印异常名称、异常原因、异常发生的位置等并终止程序。

#### 异常的避免

​	在以后的开发中尽量使用if条件判断来避免异常的发生。

#### 异常捕获的语法格式

​	try{

​		编写可能发生异常的语句;

​	}

​		catch(异常类型  变量名){

​		编写针对该类异常的处理语句;

​	}

​	……

​	finally{

​		编写无论是否发生异常都应该执行的语句;

​	}

##### 注意事项

+ 当需要编写多个`catch`分支时，切记小类型的异常应该放在大类型异常的上面。

  ​	懒人的写法：

  ​	catch(Exception) { ... }

+ `finally`主要用于编写善后处理的语句，如:关闭已经打开的文件等；

  ​	try{

  ​		a;

  ​		b;

  ​		c;

  ​	} catch(...) {

  ​		d;

  ​	} finally {

  ​		e;

  ​	}

当上述程序执行过程没有发生异常时的执行流程：a b c e;

当上述程序执行过程发生异常时的执行流程：a b d e;

#### 异常的抛出

##### 基本概念

​	在某些特殊情况下产生的异常无法处理或者不便于处理时，就可以将该异常转移给该方法的调用者，这种方式就叫做异常的抛出。

##### 语法格式

​	访问权限  返回格式  方法名称  (形参列表)  throws  异常类型1，异常类型2，……{}

##### 如：

​	public void show()  throws IOException {}

#### 代码案例

```java
import java.io.FileInputStream;
import java.io.IOException;

public class ExceptionThrowsTest {
    // 在以后的开发中不建议在main方法中抛出异常
    public static void main(String[] args) throws IOException {
        FileInputStream fis = new FileInputStream("c:/a.txt");
        fis.close();
    }
}
```

#### 方法重写的原则

+ 要求方法名相同、参数列表相同、返回值类型相同，从jdk1.5开始允许返回子类类型
+ 要求方法的访问权限不能变小，可以相同或者变大
+ 要求不能抛出更大的异常

#### 代码案例

```
import java.io.IOException;
import org.omg.CORBA.portable.ApplicationException;

public class SubExceptionTest extends SuperExceptionTest {
    
    @Override
    // public void show() throws Exception { error 不能抛出更大的异常
    // public void show() throws ApplicationException { error 不能抛出同级不一样异常
    // public void show() throws IOException { ok 可以抛出相同的异常
    // public void show() throws FileNotFoundException { ok 可以抛出更小的异常
    public void show() { // ok 可以不抛出异常
        // 方法实现
    }
}
```

##### 实现流程

+ 自定义xxxxException继承自Exception类或者其子类；
+ 提供两个版本的构造方法: 无参构造方法 和 字符串 作为参数的构造方法；

##### 自定义异常

+ 很多的软件在开发时都采用异常做错误处理的方式，因此用户可以根据需要自定义异常。
+ 自定义异常的方式为:
  1 继承`Exception`或者异常的子类。
  2 提供两个构造，无参构造和`String`做参数的构造。

##### 基本概念

​	`java.io.File`类主要用于描述文件和目录的路径信息，可以获取名称、大小等属性信息

##### 常用的方法

绝对路径	- 主要指以根目录开始的路径信息，如:c:/...	d:/..	/...

相对路径	- 主要指以当前工作目录开始的路径信息，如:	./...

​		.  表示当前目录	..  表示当前目录的上一级目录

​		-  在以后的开发中尽量使用相对路径

|          方法签名          |                 功能描述                 |
| :------------------------: | :--------------------------------------: |
|  `File(String pathname)`   |      根据参数指定的路径名来构造对象      |
|     `boolean exists()`     | 测试此抽象路径名表示的文件或目录是否存在 |
|     `String getName()`     | 返回由此抽象路径名表示的文件或目录的名称 |
|      `long length()`       |    返回由此抽象路径名表示的文件的长度    |
|   `long lastModified()`    | 返回此抽象路径名表示文件最后一次修改时间 |
| `String getAbsolutePath()` |  返回此抽象路径名表示文件的绝对路径信息  |

#### file类实现文件的创建和删除

```java
import java.io.File;
import java.io.IOException;

public class FileCreateDeleteExample {
    public static void main(String[] args) {
        // 1. 创建文件对象（使用图片中的构造方法）
        File file = new File("test.txt");
        
        // 2. 检查文件是否存在（使用图片中的exists方法）
        System.out.println("文件是否存在: " + file.exists()); // false
        
        // 3. 创建新文件（补充图片中未展示的方法）
        try {
            boolean created = file.createNewFile();
            System.out.println("文件创建结果: " + created); // true
            System.out.println("文件是否存在: " + file.exists()); // true
            
            // 4. 显示文件信息（使用图片中的方法）
            System.out.println("\n文件信息：");
            System.out.println("名称: " + file.getName());
            System.out.println("大小: " + file.length() + " bytes");
            System.out.println("最后修改: " + file.lastModified());
            System.out.println("绝对路径: " + file.getAbsolutePath());
            
            // 5. 删除文件（补充图片中未展示的方法）
            boolean deleted = file.delete();
            System.out.println("\n文件删除结果: " + deleted); // true
            System.out.println("删除后文件是否存在: " + file.exists()); // false
            
        } catch (IOException e) {
            System.out.println("操作失败: " + e.getMessage());
        }
    }
}
```

#### file类实现目录的创建和删除

```java
import java.io.File;

public class DirectoryOperationsExample {
    public static void main(String[] args) {
        // 1. 创建目录对象（使用图片中的构造方法）
        File dir = new File("my_directory");
        
        // 2. 检查目录是否存在（使用图片中的exists方法）
        System.out.println("目录是否存在: " + dir.exists()); // false
        
        // 3. 创建单级目录（补充图片中未展示的方法）
        boolean created = dir.mkdir();
        System.out.println("目录创建结果: " + created); // true
        System.out.println("目录是否存在: " + dir.exists()); // true
        
        // 4. 显示目录信息（使用图片中的方法）
        System.out.println("\n目录信息：");
        System.out.println("名称: " + dir.getName());
        System.out.println("路径: " + dir.getAbsolutePath());
        
        // 5. 创建多级目录（补充图片中未展示的方法）
        File multiDir = new File("parent/child/grandchild");
        System.out.println("\n创建多级目录结果: " + multiDir.mkdirs());
        
        // 6. 删除目录（补充图片中未展示的方法）
        boolean deleted = dir.delete();
        System.out.println("\n目录删除结果: " + deleted); // true
        System.out.println("删除后目录是否存在: " + dir.exists()); // false
        
        // 注意：删除目录前需确保目录为空
        File tempFile = new File("my_directory/temp.txt");
        tempFile.createNewFile();
        System.out.println("\n非空目录删除尝试: " + dir.delete()); // false
    }
}
```

#### file类实现目录中所有内容的获取

```java
import java.io.File;

public class DirectoryContentReader {
    public static void main(String[] args) {
        // 1. 创建目录对象（使用图片中的File构造方法）
        File dir = new File("C:/MyDocuments");
        
        // 2. 检查目录是否存在（使用图片中的exists方法）
        if (!dir.exists() || !dir.isDirectory()) {
            System.out.println("目录不存在或不是有效目录！");
            return;
        }
        
        // 3. 获取目录基本信息（使用图片中的方法）
        System.out.println("目录名称: " + dir.getName());
        System.out.println("绝对路径: " + dir.getAbsolutePath());
        System.out.println("最后修改: " + new Date(dir.lastModified()));
        
        // 4. 获取目录下所有内容（补充图片中未展示的方法）
        System.out.println("\n【目录内容列表】");
        File[] contents = dir.listFiles();
        
        if (contents != null && contents.length > 0) {
            // 打印表头
            System.out.printf("%-20s\t%-10s\t%-20s\n", 
                "名称", "类型", "最后修改时间");
            System.out.println("------------------------------------------------");
            
            for (File item : contents) {
                // 使用图片中的方法获取信息
                String type = item.isDirectory() ? "目录" : "文件";
                String size = item.isFile() ? formatSize(item.length()) : "-";
                
                System.out.printf("%-20s\t%-10s\t%-20s\n",
                    item.getName(),
                    type,
                    new Date(item.lastModified()));
            }
        } else {
            System.out.println("该目录为空");
        }
    }
    
    // 辅助方法：格式化文件大小
    private static String formatSize(long bytes) {
        if (bytes < 1024) return bytes + " B";
        if (bytes < 1024 * 1024) return String.format("%.1f KB", bytes / 1024.0);
        return String.format("%.1f MB", bytes / (1024.0 * 1024));
    }
}
```



### 五、IO流

##### 基本概念

​	`I/O`就是`Input/Output`的简写，也就是输入输出的含义。

​	`I/O`流就是像流水一样不间断地读写状态

##### 基本分类

+ 按照数据读写的基本单位不同分为：字节流  和  字符流。
+ 其中字节流主要指以字节为单位进行读写的流，可以处理任意类型的文件；
+ 其中字符流主要指以字符(2个字节)为单位进行读写的流，只能处理文本文件；
+ 按照数据流动的方向不同分为：输入流  和  输出流(站在程序的角度)。
+ 其中输入流主要指从文件中读取数据内容输入到程序中，也就是读文件；
+ 其中输出流主要指将程序中的数据内容输出到文件中，也就是写文件；

#### 代码案例

```java
import java.io.FileOutputStream;

public class FileOutputStreamTest {
    public static void main(String[] args) {
        try {
            // 1.构造FileOutputStream类型的对象与c:/a.txt文件关联
            // 当文件不存在时，该流会自动创建新的空文件
            // 当文件存在时，该流会自动清空文件中的原有内容
            FileOutputStream fos = new FileOutputStream("c:/a.txt");

            // 2.使用输出流写入数据到文件中
            fos.write(97);  // 97 - 'a'
            System.out.println("写入数据成功！");

            // 3.关闭流对象并释放有关的资源
            fos.close();
        } catch(Exception e) {
            e.printStackTrace();
        }
    }
}
```

### FileOutputStream类

##### 基本概念

​	java.io.FileOutputStream类主要用于将图像数据之类的原始字节流写入输出流中。

##### 常用方法

|                 方法签名                 |                          功能描述                          |
| :--------------------------------------: | :--------------------------------------------------------: |
|           `void write(int b)`            |                 将指定字节写入此文件输出流                 |
| `void write(byte[] b, int off, int len)` | 将指定字节数组中从偏移量off开始的len个字节写入此文件输出流 |
|          `void write(byte[] b)`          |      将b.length个字节从指定字节数组写入此文件输出流中      |
|              `void close()`              |             用于关闭文件输出流并释放有关的资源             |



# Java的IO流处理

### 一、FileInputStream类

##### 基本概念

​	`java.io.FileInputStream`类主要用于从输入流中读取图像数据之类的原始字节流。

##### 常用方法

|                方法签名                |                           功能描述                           |
| :------------------------------------: | :----------------------------------------------------------: |
|              `int read()`              |         读取一个byte无符号填充到int低八位，-1表示EOF         |
|          `int read(byte[] b)`          | 从此输入流中将最多b.length个字节的数据读入字节数组，返回实际读取的字节数 |
| `int read(byte[] b, int off, int len)` | 从此输入流中将最多len个字节的数据读入字节数组的指定偏移位置  |
|             `void close()`             |                 关闭文件输入流并释放相关资源                 |

#### 代码案例

```java
import java.io.FileInputStream;

public class FileInputStreamTest {
    public static void main(String[] args) {
        try {
            // 1.构造FileInputStream类型的对象与c:/a.txt文件关联
            FileInputStream fis = new FileInputStream("c:/a.txt");

            // 2.通过输入流从文件中读取数据内容
            /*
            int res = fis.read();
            System.out.println("读取到的单个字节是：" + res 
                + "，对应的字符是：" + (char)res); // 'a' => 97

            // 每当读取完毕一个字节后，可以继续读取下一个字节
            res = fis.read();
            System.out.println("读取到的单个字节是：" + res 
                + "，对应的字符是：" + (char)res); // '9' => 57
			*/
            
            //使用字节数组来读取文件中的所有内容
            byte[l bArr = new byte[20];
            //期望通过输入流读取10个字节的数据内容
            //放入数组bArr中下标从3开始的索引位置
            int res =fis.read(bArr,3，10);
            System.out.println("读取到的数据内容是:"
            + new string(bArr,3,res) + "实际读取到的数据大小是:" + res);
            // 3.关闭流对象并释放有关的资源
            fis.close();
        } catch(Exception e) {
            e.printStackTrace();
        }
    }
}
```

##### 拷贝操作

```java
import java.io.FileInputStream;
import java.io.FileOutputStream;

public class FileCopyTest {
    public static void main(String[] args) {
        FileInputStream fis = null;
        FileOutputStream fos = null;
        
        try {
            // 1.构造FileInputStream类型的对象与c:/a.txt文件关联
            fis = new FileInputStream("c:/a.txt");
            
            // 2.构造FileOutputStream类型的对象与c:/b.txt文件关联
            fos = new FileOutputStream("c:/b.txt");
            
            // 3.不断地从输入流中读取一个字节写入到输出流中
            int content;
            while ((content = fis.read()) != -1) {
                fos.write(content);
            }
            System.out.println("文件复制完成！");
            
        } catch (Exception e) {
            e.printStackTrace();
        } finally {
            // 4.关闭流对象并释放有关的资源
            try {
                if (fis != null) {
                    fis.close();
                }
                if (fos != null) {
                    fos.close();
                }
            } catch (Exception e) {
                e.printStackTrace();
            }
        }
    }
}
```

### 二、BufferedWriter类

##### 基本概念

​	java.io.Bufferedwriter类主要用于向输出流中写入单个字符、字符数组以及字符串

##### 常用方法

|                  方法签名                   |                         功能描述                         |
| :-----------------------------------------: | :------------------------------------------------------: |
|             `void write(int c)`             |                用于写入单个字符到输出流中                |
| `void write(char[] cbuf, int off, int len)` | 用于将字符数组cbuf中从下标off开始的len个字符写入输出流中 |
|          `void write(char[] cbuf)`          |         用于将字符串数组cbuf中所有内容写入输出流         |
|          `void write(String str)`           |          用于将参数指定的字符串内容写入输出流中          |
|              `void newLine()`               |                用于写入行分隔符到输出流中                |
|               `void close()`                |            用于关闭文件输出流并释放有关的资源            |

#### 代码案例

```java
import java.io.BufferedWriter;
import java.io.FileWriter;

public class BufferedWriterTest {
    public static void main(String[] args) {
        // 1.构造BufferedWriter类型的对象与c:/a.txt文件关联
        try (BufferedWriter bw = new BufferedWriter(new FileWriter("c:/a.txt"))) {
            
            // 2.向输出流中写入单个字符、字符数组以及字符串
            bw.write('A');  // 写入单个字符
            
            char[] chars = {'B', 'C', 'D'};
            bw.write(chars);  // 写入字符数组
            
            bw.write("\nHello World!");  // 写入字符串
            bw.newLine();  // 写入换行符
            bw.write("This is BufferedWriter demo");
            
            System.out.println("数据写入完成！");
            
            // 3.关闭流对象并释放有关的资源
            // try-with-resources 自动关闭
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### 三、BufferedReader类

##### 基本概念

​	`java.io.BufferedReader`类主要用于从输入流中读取单个字符、字符数组以及一行字符串内容。

##### 常用方法

|                 方法签名                  |                           功能描述                           |
| :---------------------------------------: | :----------------------------------------------------------: |
|               `int read()`                | 用于读取单个字符并返回，若读取到文件末尾则返回-1，否则返回实际读取到字符的整数值 |
| `int read(char[] cbuf, int off, int len)` | 用于从输入流中读取len个字符放入数组cbuf中下标从off开始的位置上，若读取到末尾则返回-1，否则返回实际读取到的字符个数 |
|          `int read(char[] cbuf)`          |                用于从输入流中读满整个数组cbuf                |
|            `String readLine()`            |                   用于读取一行字符串并返回                   |
|              `void close()`               |              用于关闭文件输出流并释放有关的资源              |

#### 代码案例

```java
import java.io.BufferedReader;
import java.io.FileInputStream;
import java.io.InputStreamReader;

public class BufferedReaderExample {
    public static void main(String[] args) {
        try {
            // 1.构造BufferedReader类型的对象与c:/a.txt文件关联
            BufferedReader br = new BufferedReader(
                new InputStreamReader(
                    new FileInputStream("c:/a.txt")
                )
            );

            // 2.从输入流中读取数据内容并打印出来
            // 以字符为单位读取文件中的所有内容
            // 在windows系统中行分隔符为：\r\n
            int res = 0;
            while((res = br.read()) != -1) {
                System.out.println("读取到的字符是：" + (char)res + 
                                "，对应的ASCII值为：" + res);
            }

            // 3.关闭流对象并释放有关的资源
            br.close();
        } catch(Exception e) {
            e.printStackTrace();
        }
    }
}
```

### 四、PrintStream类

##### 基本概念

​	java.io.PrintStream类主要用于方便地打印各种数据内容并且自动刷新。

##### 常用方法

|         方法签名         |              功能描述              |
| :----------------------: | :--------------------------------: |
|  `void print(String s)`  | 用于将参数指定的字符串内容打印出来 |
| `void println(String x)` |     用于打印字符串后并终止该行     |
|      `void close()`      | 用于关闭文件输出流并释放有关的资源 |

#### 代码案例

```java
import java.io.FileOutputStream;
import java.io.PrintStream;

public class PrintStreamTest {
    public static void main(String[] args) {
        // 1.构造PrintStream类型的对象与c:/a.txt文件关联
        try (PrintStream ps = new PrintStream(new FileOutputStream("c:/a.txt"))) {
            
            // 2.通过该输出流向文件中写入数据内容"hello"
            ps.print("hello");
            System.out.println("数据写入完成！");
            
            // 3.关闭流对象并释放有关的资源
            // try-with-resources 自动关闭
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### 五、ObjectInputStream类

##### 基本概念

​	java.io.0bjectInputStream类主要用于从输入流中一次性将一个对象的内容读取出来实现了从字节序列到对象的转化过程，叫做反序列化。

##### 常用方法

|              方法签名               |                           功能描述                           |
| :---------------------------------: | :----------------------------------------------------------: |
| `ObjectInputStream(InputStream in)` | 根据参数指定的引用来构造对象 其中InputStream类是个抽象类，实参需要传递子类的对象 |
|        `Object readObject()`        | 主要用于从输入流中读取一个对象并返回 无法通过返回值来判断是否读取到文件的末尾 |
|           `void close()`            |              用于关闭文件输出流并释放有关的资源              |

#### 代码案例

```java
import java.io.FileInputStream;
import java.io.ObjectInputStream;

public class ObjectInputStreamTest {
    public static void main(String[] args) {
        try {
            // 1.构造ObjectInputStream类型的对象与c:/a.txt文件关联
            ObjectInputStream ois = new ObjectInputStream(
                new FileInputStream("c:/a.txt"));

            // 2.从输入流中读取一个对象并打印出来
            Object obj = ois.readObject();
            System.out.println("读取到的对象是：" + obj);

            // 3.关闭流对象并释放有关的资源
            ois.close();
        } catch(Exception e) {
            e.printStackTrace();
        }
    }
}
```

##### 经验分享

​	当需要写入多个对象到文件中时，建议先将多个对象放入一个集合对象中，然后将集合对象看做一个整体只需要调用一次`writeObject`方法就可以写入所有内容，此时只需要调用一次`readObject`方法就可以将所有内容读取出来，这样就避免了通过返回值来判断是否读取到文件的末尾。

### transient关键字

​	`transient`是Java语言的关键字，用来表示一个域不是该对象串行化的一部分当一个对象被策行化的时候，`transient`型变量的值不包括在行化的表示中然而非transient型的变量是被包括进去的。



# Java的多线程处理

### 一、线程

##### 基本概念

+ 程序	-  数据结构+算法，主要指存放在硬盘上的可执行文件。
+ 进程	- 主要指运行在内存中的程序。

​	目前主流的操作系统都支持多进程，为了使得操作系统能够同时执行多个任务，但进程是重量级的，新建进程对系统的资源消耗比较大，因此进程的数量比较局限。

​	线程是进程内部的程序流，也就是操作系统中支持多进程，而每个进程的内部又可以支持多线程，线程是轻量级的，新建线程会共享所在进程的系统资源，因此以后的开发中都采用多线程技术。

​	多线程技术采用时间片轮转法实现并发执行，所谓并发就是指宏观并行微观串行的技术。

#### 线程的创建

​	`java.lang.Thread`类用于描述线程，Java 虚拟机允许应用程序并发地运行多个执行线程，而线程的创建和启动方式如下：

​	（1）自定义类继承`Thread`类并重写`run`方法，创建该类的实例调用start方法

​	（2）自定义类实现`Runnable`接口并重写`run`方法，创建该类的实例作为实参来构造`Thread`类型的对象，然后使用`Thread`类型的对象调用`start`方法。

##### 相关方法的解析

​	`Thread()`	-  使用无参方式构造对象。

​	`Thread(String name)`	-  根据参数指定的名称来构造对象。

​	`Thread(Runnable target)`	-  根据参数指定的引用来构造对象

​	`void run()`	-  若使用Runnable类型的引用构造出来的对象调用该方法，则最终调用引用所指向对象的run方法，否则调用该方法啥也不做。

​	`void start()`	-  用于启动线程，Java虚拟机会自动调用该线程的run方法。

##### 原理分析

+ 执行main方法的线程叫做主线程，执行run方法的线程叫做子线程。
+ main方法是程序的入口，最开始只有主线程来依次执行main方法中的代码，当start方法调用成功后，线程的个数瞬间由1个变成了2个，其中子线程去执行run方法，主线程继续执行main方法的代码，两个线程各自独立运行互不影响。
+ 当run方法执行完毕后子线程结束，当main方法执行完毕后主线程结束，但两个线程0谁先执行没有明确的规定，取决于操作系统的调度算法。
