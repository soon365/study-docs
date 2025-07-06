[TOC]



# Java程序开发入门

### 1.计算机的体系结构

#### 1.1 计算机的基本概念

- 计算机俗称“电脑”，是一种被广泛应用宇各个领域的设备

- 计算机主要是由 计算机硬件 + 计算机软件 组成

#### 1.2 计算机硬件（Computer Hardware）

计算机常见的硬件主要包括：中央处理器、内存、硬盘、输入输出设备、主板、机箱和电源等辅助设备。

​	① CPU — 中央处理器，是计算机最核心的部件。

​		— 主要用于处理各种计算机的指令以及软件中的数据等。

​	② 内存 — 是计算机的存储部件。

​		 — 主要用于临时存放CPU访问的数据内容，CPU直接访问且效率高。

​		— 缺点在于容量小，一旦断电会造成数据的丢失。

​		—所有时刻记得 **Ctrl+s **进行保存

​	③ 硬盘 — 是计算机的存储部件

​		— CPU不能直接访问硬盘中的数据，因此效率比较低。

​		— 容量大，断电不会造成数据的丢失。

​	④ 键盘叫做标准输入设备，显示器叫做标准输出设备

科普：
​	1Tb =1024Gb1Gb=1024Mb
​	1Mb =1024Kb
​	1Kb =1024byte(字节)   通常一个英文字母占1个字节，一个汉字占2个字节
​	1byte =8bit(二进制位)  在计算机的底层识别0和1组成的二进制序列
​思考:
​	目前主流硬盘配置有:250G、320G、500G、1Tb、...为啥1TB的计算机显示只有951G呢？

解析:
	硬件厂商是采用1000作为进率，而操作系统中是采用1024作为进率。

#### 1.3计算机软件

计算中常见的软件主要分为两个部分：**系统软件**和**应用软件**。

​	**系统软件**主要指操作系统，主流的操作系统：Windows/Unix/Linux/Ios/Android

​	**应用软件**主要指安装在操作系统之上的软件：QQ、迅雷、火狐浏览器、等...

#### 1.4计算机的体系结构

​	使用者=> 应用软件 =>  系统软件 =>  硬件设备
​		    => 其中信息系统软件分为：内核（Kernel）和外壳（shell）

### 2.Java语言的概述

#### 2.1 Java语言的背景

​	Java语言诞生于1995年，该语言之父是詹姆斯·高斯林，之前隶属于sun公司，先隶 属于Oracle公司。

#### 2.2 Java语言的主要版本

​	（1） Java SE （Java Platform，standard Editon）
​	     — 称之为“java平台标准版”，主要许欸小Java语言的语法规范和常见类。

​	（2）Java EE （Java Platform，Enterprise Editon）

​	     — 称之为“Java平台企业版”，主要学习Java项目的后台开发技术，编写B/S架构项目。

​	（3） Java ME （Java Platform，Micro Editon）

​	     — 称之为“Java平台微型版”，随着Android平台的迅速普及已经走向淘汰。

### 3.开发环境的搭建和使用

#### 3.1 jdk的下载和安装

​	（1）下载方式

​		  方式一：官网下载   www.sun.com / www.reacle.com

​	（2）安装方式

​		若下载的是绿色版，则直接解压

​		若下载的是安装版，则直接一路点击下一步即可

​		切记 JDK 的安装路径中不要有中文!

#### 3.2 相关的概念

​	jdk — Java开发工具包，只要做Java开发就需要下载和安装该软件。

​	jre — Java运行时环境信息，只要运行Java程序就需要下载和安装该软件。

​	jvm — Java虚拟机，是Java程序与计算机操作系统之间的桥梁。

​	javac.exe — Java语言的编译器，主要用于将Java源代码进行编译生成字节码文件。

​	java.exe — Java语言的解释器，主要用于启动Java虚拟机对字节码文件进行解释执行。

#### 3.3 Java程序的编写流程

​	（1）新建文本文档，将文件名由xxx.txt修改为xxx.java;

​	（2）使用记事本的方式打开文件，编写Java代码后进行保存;

​	（3）启动dos窗口，切换到xxx.java文件所在的路径中;

​	（4）使用javac xxx.iava进行编译，生成xxx.class的字节码文件;

​	（5）使用java xxx进行解释执行，打印最终结果;
注意:

​	当文件扩展名默认不显示时的处理方式:组织=〉文件夹和搜索选项=>查看=〉隐藏已知文件类型的扩展名=>去掉勾选=>确定

#### 3.4 常用的快捷键

​	ctrl+s 保存	ctrl+c 复制	ctrl+v粘贴	ctrl+x剪切	ctrl+z 撤销	ctrl+f 查询	ctrl+a全选

​	windows+d 回到桌面	windows+e 打开计算机	windows+l锁屏	

​	windows+r 打开运行，输入cmd后回车就可以启动dos窗口

​	windows+tab 切换任务

​	alt+tab 切换任务

​	ctrl+alt+delete 启动务管理器

​	ctrl+shift 切换输入法，若切换到中文后则使用shift键进行中英文切换。

#### 3.5环境变量的配置

​	（1）基本概念

​		通常情况下可执行文件只能在该文件所在的路径中访问，若希望该可执行文件可以在任意路径中使用则需要将该可执行文件的路径信息配置到环境变量Path中。

​	（2）实现方式
​		计算机=〉右键，选择属性=〉高级系统设置=>高级=〉环境变量=>系统变量=>找到Path，点击编辑=>将javac.exe所在的路径信息复制到Path变量值的最前面，加上英文版的分号=>一路点击确定即可。

​		切记Path变量值原来的内容不要改变，配置完毕后重新启动dos窗口!

#### 3.6 跨平台原理

​	由于不同的操作系统中都提供了Java虚拟机进行翻译，因此同一份字节码文件可以在不同的操作系统中执行，从而赢得了"一次编译，到处运行"的美名。



# Java语言的基本语法格式

### 1.变量和注释

#### 1.1 基本概念

​	当需要在Java程序中记录单个数据内容时，则声明一个变量即可，而声明变量的本质就是在内存空间中申请一块存储单元，由于该存储单元的数值可以发生改变，因此得名为”变量“。
​	由于存放数据内容的大小不同导致所需存储单元的容量不同，在Java语言中使用数据类型加以描述，为了便于下次访问还需要指定变量的名称。

#### 1.2 声明方式

​	数据类型 变量名 = 初始值;

如：

```java
public class VatTest {
    public static void main(String[] args) {
        //声明一个初始值为10元素类型的int类型的变量
        int a = 10;
        //打印变量的数值 + 字符串连接符，用于实现连接的功能
        System.out.println("a = " + a);//a = 10
        System.out.println("---------------------------");
        //变量在使用之前必须声明
        //System.out.println("sa=" +sa);//错误：找不到符号
        //变量在使用之前必须初始化
        //Stting sa；
        //System.out.println("sa=" +sa);//错误：可能尚未初始化变量sa
        String sa = "hello world";
        System.out.println("sa = " + sa);//sa=hello world
        //变量不能重复
        //int a =20;//错误：已在方法main（String[]）中定义了变量 a
    }
}
```

注意：

- Java是强类型语言，变量在使用必须声明，指明其数据类型。
- 编译器会根据变量的类型检测对变量的操作是否合法。

- java变量在使用前必须初始化，也就是赋以确定的初值。
- 属性系统辉自动初始

#### 1.3 标识符（变量名）的名字规则

（1）要求有字母、数字、下划线以及美元$组成，其中数字不能开头。

​	如：name、age、name2、age2等

（2）要求不能使用java中的关键字，所谓关键字就是Java中用于表示特殊含义的单词。

​	如: public、class、void、static等区分大小写。

（3）长度没有限制但不宜过长。

​	如: name 和 Name 代表不同的标识符，不推荐使用

（4）尽量做到见名知意，支持中文但不推荐使用。

​	如: year、month、size、length、time、shijian等

```java
/**
 * 编程实现姓名和年龄的输入输出
 */
public class VarI0 {
    public static void main(String[] args) {
        //1.声明两个变量分别用于记录姓名和年龄
        String name;
        int age;
        //2.提示用户输入姓名和年龄并存放上述变量中
        System.out.println("请输入您的姓名和年龄：");
        //创建扫描器对象来扫描键盘的输入
        Scanner sc = new Scanner(System.in);
        //通过骚猫其读取一个字符串存放到变量name中
        name = sc.next();
        //通过扫描器对象读取一个整数存放到变量age中
        age = sc.nextInt();
        //3.打印变量的数值
        System.out.println("姓名：" + name + "，年龄：" + age);
    }
}
```

#### 1.4 注释

​	//	表示单行注释，从 // 开始一直到本行末尾的使用内容都是注释

​	/******/    表示多行注释，从/*****开始一直到*****/之间的所有内容都是注释。

注意：

​	多行注释不允许嵌套使用！

### 2.数据类型

#### 2.1 基本分类

​	在java语言中奖数据类型分为两大类：

​	（1）基本数据类型

​		byte、short、int、long、float、double、boolean、char

​	（2）引用数据类型

​		数组、类、接口、注解、枚举

#### 2.2 常用的进制

​	在日常生活中采用十进制进行数据的描述，权重：10^0、10^1、10^2、...

​	在计算机地产采用二进制进行数据的描述，权重：2^0、2^1、2^2、...

​	由于现实生活中的数据具有正负数，因此二进制中采用最高为（最左边）代表符号位，若是0则代表非负数，若是1则代表负数。

#### 2.3 进制之间的转换（原理）

​	（1）正十进制转换为二进制发方式

​		  a.除2取余法，使用十进制整数不断的除以2直到商为0时将余数逆序排序即可

​		  b.差分法，将十进制整数差分为若干个二进制权重的和，若有该权重下面写1，否则写0

​		  如：

​			45 = 32 + 8 +4 + 1

​				128	64	32	16	8	4	2	1

​				   0	   0	  1	   0	1	1	0	2    = >    0010 1101

​	（2）正二进制转换十进制的方法

​		  a.加权法，使用二进制中的每个数字乘以当前位的权重在累加起来。

​		   如：

![image-20250629142724851](C:\Users\26803\AppData\Roaming\Typora\typora-user-images\image-20250629142724851.png)

​	（3）负十进制转换为二进制的方式

​		  a.先将十进制的绝对值转换为二进制，进行按位取反再加1.

​		    如：

​			- 45  = > 绝对值转换为二进制：0010 1101

​				 = > 按位取反：		   1101 0010

​				 = > 加1：			    1101 0011

​	（4）负的二进制转换为十进制的方式

​		  a.先减1在按位取反，然后合并为十进制整数后添加负号。

​			如：

​				1101 0011 => 先减1：                 1101 0010

​						    => 按位取反：           0010 1101

​						    => 合并为十进制：    45

​						    => 添加负号： 	  - 45



# Java语言的流程控制

### 1.分支结构

#### 1.1 基本概念

​	 特殊场合中需要进行判断并选择时，就需要使用分支结构

​	 三种程序结构：任何复杂的程序逻辑都可以通过  顺序、分支、循环三种基本的程序结构实现

#### 1.2 if 分支结构

​	（1）语法格式					（2）执行流程

​		if（条件表达式）{				  判断条件表达式是否成立

​			语句块；					  = > 若成立，则执行语句块；

​		}								= > 若不成立，则跳过语句块；

```java
/*
*   编程实现if分支结构的使用
* */
import java.util.Scanner;
public class ifTest {
    public static void main(String[] args) {
        //1.提示用户输入年龄信息并使用变量记录
        System.out.println("请输入你的年龄");
        Scanner sc = new Scanner(System.in);
        int age = sc.nextInt();

        //2.使用if分支结构判断用户是否成年并给出对应的提示
        if (age >= 18){
            System.out.println("你已成年");
        }
        //3.无论是否成年都打印一句话
        System.out.println("很抱歉，你网费不够，是否充值网费");
    }
}
```

#### 1.3 if-else分支结构

​	（1）语法格式					（2）执行流程

​		if（条件表达式1）{				判断条件表达时1是否成立

​			语句块1；						 = > 若成立，则执行语句块								

​		}else if（条件表达式2）{				= > 若不成立，则判断条件表达式2是否成立

​			语句块2；							= > 若成立，则执行语句2；

​		}										 = > 若不成立，则执行语句块n

```java
/*
* 编程实现if-else分支结构的使用
* */
import java.util.Scanner;
public class IfElseifelseTest {
    public static void main(String[] args){
        //1.提示用户输入身份信息并使用变量记录
        System.out.println("请输入您的身份信息：");
        Scanner sc = new Scanner(System.in);
        String str = sc.next();
        //2.使用if...else if...else结构判断身份信息并给出对应的提示
        if ("军人".equals(str)){
            System.out.println("请免费乘车！");
        }
        else if ("学生".equals(str)){
            System.out.println("请购买半票！");
        }
        else {
            System.out.println("请购买全价票！");
        }
    }
}
```

#### 1.4 switch—case分支结构

​	（1）语法格式

​		switch（变量/表达式）{

​			case 字面值1：语句块1：break；

​			case 字面值2：语句块2：break；

​			…

​			default：语句块n：

​		}

​	（2） 执行流程

​		计算变量/表达式的数值 => 判断是否匹配字面值1

​			=> 若匹配，则执行语句块1 => 执行break跳出当前结构

​			=> 若不匹配，则判断是否匹配字面值2

​				=> 若匹配，则执行语句块2 => 执行break跳出当前结构

​				=> 若不匹配，则执行语句块n

​	（3）注意事项

​		switch()中支持的数据类型有：byte、short、char以及int类型，从jdk1.5开始支持枚举类型，从jdk1.7开始支持String类型。

```java
/*
* 编程使用switch-case分支结构判断并打印考试成绩
* */
import java.util.Scanner;
public class TestSwitchcase {
    public static void main(String[] args) {
        //1.提示用户输入考试成绩并使用变量记录
        System.out.println("请输入您的考试成绩：");
        Scanner sc = new Scanner(System.in);
        int score = sc.nextInt();

        //2.使用switch-case分支结构判断并打印
        switch (score / 10) {
            case 10:
                System.out.println("太棒了");
                break;
            case 9:
                System.out.println("优秀");
                break;
            case 8:
                System.out.println("良好");
                break;
            case 7:
                System.out.println("一般");
                break;
            case 6:
                System.out.println("及格");
                break;
            default:
                System.out.println("不及格");
                break;
        }
        //打印一句经典语录
        System.out.println("“学习使人快乐”");
    }
}
```

### 2.循环结构

#### 2.1 基本概念

​	特殊场合中需要重复执行一段代码时，借助循环结构加以处理。

#### 2.2 for循环

​	（1）语法格式

​		for(初始化表达式；条件表达式；修改初始值表达式){

​		循环体；

​		}

​	（2）执行流程

​		执行初始化表达式 => 判断条件表达式是否成立

​			=> 若成立，则执行循环体  => 修改初始值表达式 =>判断条件表达式是否成立

​			=>若不成立，则循环结束					

```java
/*
*   编程实现for循环的使用
* */
public class ForTest {
    public static void main(String[] args) throws InterruptedException {
        for (int money = 1000; money >=100; money -= 100){
            System.out.println("当前账户余额："+ money+",正在清点，请你稍后。。。");
            Thread.sleep(1000);
            System.out.println("请取走您的钞票！\n");
        }
        System.out.println("取钱结束！");
    }
}
```

#### 2.3 break和continue关键字

​	break关键字可以用于循环中表示跳出当前循环；

​	continue关键字用于循环中表示结束本次循环继续下一次 循环；

```java
/*
*   编程实现break关键字和continue关键字的使用
* */
public class breakcontinueTest {
    public static void main(String[] args) {
        for (int i = 0; i <= 20; i++) {
            if (0 == i%5) {
                continue; //结束本次循环继续下一次循环 奔向i++
            }
            if (18 == i){
                break;//跳出当前循环
            }
            System.out.println("i="+i);
        }
        //break执行后跳到这里
    }
}
```

#### 2.4 特殊的循环

​	for（；；）- 这种没有循环条件的循环叫做无限循环

​	通常与break关键字搭配使用

```java
import java.util.Scanner;

/*
* 编程使用for循环来模拟聊天的过程
* */
public class ForChatTest {
    public static void main(String[] args) {

        //声明一个boolean变量作为标志位
        boolean flag = true;
        for (; ; ) {
            //1.提示用户输入聊天的内容并使用变量记
            System.out.println("请"+(flag?"张三":"李四")+"输入要发送的内容:");
            Scanner sc = new Scanner(System.in);
            String msg = sc.next();
            //2.判断用户输入的内容是否为“bye”，若时则聊天结束
            if ("bye".equals(msg)) {
                System.out.println("聊天结束");
                break;//跳出当前循环
            }
            //3.若不是则打印用户输入的内容
          // else {
                System.out.println((flag?"张三说":"李四说")+ msg);
          //}
            flag = !flag;
        }
        //跳到这里了，说明聊天结束
    }
}
```

#### 2.5 双重for循环

​	（1）语法格式

​		for（初始化表达式1；条件表达式2；修改初始值表达式3）{

​			for（初始化表达式4；条件表达式5；修改初始值表达式6）{

​				循环体；

​			}

​		}

​	（2）执行流程

​		执行表达式1 => 判断表达式2是否成立

​			=> 若成立，则执行表达式4 => 判断条件表达式5是否成立

​				=> 若成立，则执行循环体 => 执行表达式6 => 判断表达式5是否成立

​				=> 若不成立，则内层循环结束 => 执行表达式3 => 判断表达式2是否成立

​			=> 若不成立，则外层循环结束

​	（3）注意事项

​		a。外出循环变量动一下，则内层循环变量跑一圈；

​		b.当需要打印多行多列的数据内容时，可以使用双重for循环；

```java
/*
*   编程实现双重for循环的使用
* */
public class ForForTest {
    public static void main(String[] args) {
        //1.使用for循环打印5行字符串的内容
        for (int i = 0; i <= 5; i++) {
            System.out.print("太棒了！");
        }
        System.out.println();
        System.out.println("----------------------------");
        //2.使用for循环打印5行字符串的内容
        for (int j = 0; j <= 5; j++) {
            System.out.println("太棒了！");
        }
        System.out.println();
        System.out.println("----------------------------");
        //3.使用for循环打印5行5列字符串的内容
        for (int i = 0; i <= 5; i++) {
            for (int j = 0; j <= 5; j++) {
                //打印完毕不换行
                System.out.print("太棒了！");
            }
            //专门用于换行
            System.out.println();
        }
    }
}
```

#### 2.6 while循环

​	（1）语法格式					

​		while（初始化表达式）{	

​			循环体；					 

​		}								

​	（2）执行流程

​			判断条件表达式是否成立

​			 => 若成立，则执行循环体 =>  判断条件表达式是否成立

​			  => 若不成立，则循环结束

​	（3）注意事项

​		a. while循环和for循环可以完全呼唤

​		b. while(true)和for（；；）表示无限循环

​		c. while循环主要用于明确循环条件但不明确循环次数的场合中； for循环主要用于明确循环次数或范围的场合中；	

```java
/*
 * 编程实现while循环的使用
 * */
public class WhileTest {

    public static void main(String[] args) {
        // 1.使用for循环打印1～10之间的所有整数
        for(int i = 1; i <= 10; i++) {
            System.out.println("i = " + i);
        }

        System.out.println("--------------------------------");
        // 2.使用while循环打印1～10之间的所有整数
        int i = 1;
        while(i <= 10) {
            System.out.println("i = " + i);
            i++;
        }
    }
}
```



​			Java语言的数组声明与应用

### 3.一维数组

#### 3.1 基本概念

​	当需要在程序中记录当个数据内容时，则声明一个变量即可；

​	当需要在程序中记录多个类型相同的数据内容时，则声明一维数组即可，一维数组的本质结束在内存中申请一段连续的存储单元。

#### 3.2 声明方式

​	（1）语法格式

​		数据类型 [] 数组的名称 = new 数据类型 [数组的长度]； 

​	（2）元素的初始化

​		数据类型 [] 数组的名称 = {元素值1，元素值2，…}；

```java
public class ArrayTest {
    public static void main(String[] args) {
        //1.声明一个长度为3元素类型为int类型的一维数组
        int[] arr = new int[3];
        //2.打印数组的长度以及每个元素的数值
        System.out.println("数组的长度是：" + arr.length);
        System.out.println("下标为0的元素是" + arr[0]);
        System.out.println("下标为1的元素是" + arr[1]);
        System.out.println("下标为2的元素是" + arr[2]);

        System.out.println("--------------------------------");
        //3使用循环实现数组中使用元素的打印
        for (int i = 0;i< arr.length;i++) {
            System.out.println("下标为" + i + "的元素是" + arr[i]);
        }
        System.out.println("--------------------------------");
        //4.声明一个长度为5元素类型为double类型的数组并打印默认值
        double[] arr1 = new double[5];
        for (int i = 0;i< arr1.length;i++){
            System.out.println("下标为" + i + "的元素是" + arr1[i]);
        }
        System.out.println("--------------------------------");
        //5.实现对数组arr中的元素一次赋值为11 22 33
//        arr[0]=11;
//        arr[1]=22;
//        arr[2]=33;
        for (int i = 0;i< arr.length;i++){
            arr[i] = (i+1)*11;
        }
        //使用循环实现数组中所有元素的打印
        for (int i = 0;i< arr.length;i++) {
            System.out.println(arr[i]);
        }
    }
}

```

```java
//编程实现数组的增删改查操作
public class ArrayTest {
    public static void main(String[] args) {
        //. 1.声明一个长度为5元素类型为int类型的一维数组
        int[] arr = new int[5];
        // 打印所有元素值
        System.out.println("数组中的元素初始化值为：");
        for (int i = 0; i < arr.length; i++){
            System.out.println(arr[i]+" ");
        }
        System.out.println();
        System.out.println("-----------------------");
        //2.使用10、20、30、40分别给数组中前四个元素赋值
        for (int i = 0; i < arr.length; i++){
            arr[i] = (i+1)* 10;
        }
        //打印使用元素
        System.out.println("数组赋值后的元素为：");
        for (int i = 0; i < arr.length; i++){
            System.out.println(arr[i]+" ");
        }
        System.out.println();
        System.out.println("-----------------------");
        //3.将数据50插入到数组中下边为0的位置，原有元素向后移动
        for (int i = 4; i > 0; i--){
            arr[i] = arr[i-1];
        }
        arr[0] = 50;
        //打印插入元素后的数组元素
        System.out.println("数组插入后的元素为：");
        for (int i = 0; i < arr.length; i++){
            System.out.println(arr[i]+" ");
        }
        System.out.println();
        System.out.println("-----------------------");
        //4.将数据50从数组中删除，后续元素向前移动
        for (int i = 0; i < arr.length-1; i++){
            arr[i] = arr[i+1];
        }
        arr[4] = 0;
        //再次打印元素
        System.out.println("数组删除后的元素为：");
        for (int i = 0; i < arr.length; i++){
            System.out.println(arr[i]+" ");
        }
        System.out.println();
        System.out.println("-----------------------");
        //5，查询数组中是否包含元素20，若包含将元素20改为200
        for (int i = 0; i < arr.length; i++){
            if (20 == arr[i]){
                arr[i] = 200;
            }
        }
        //再次打印所有
        System.out.println("数组改查后的元素为：");
        for (int i = 0; i < arr.length; i++){
            System.out.println(arr[i]+" ");
        }
        System.out.println();
    }
}
```

### 4 二维数组

#### 4.1基本概念

​	一维数组本质上结束一段连续的存储单元，用于存放多个类型相同的数据内容

​	二维数组本质上结束有多个一维数组组成（摞在一起）的数组，也就是说二维数组中的每一个元素都是一个一维数组，而一维数组中的每个元素才是数据内容；

#### 4.2 声明方式

​	（1）语法格式

​		数据类型 [ ] [ ] 数组名称 = new 数据类型 [行数] [列数]

​	（2）元素的初始化

​		数据类型 [ ] [ ] 数组名称 = {{初始化1，初始化2，…}，…}

```java
public class ArrayArrayTest {
    public static void main(String[] args) {
        //声明一个具有2行3列元素类型为int类型的二维数组
        int[][] array = new int[2][3];
        //打印二维数组中所有元素的数组
        //使用外层for循环用于控制打印的行数
        for (int i = 0; i < array.length; i++) {
            //使用内层for循环用于控制打印的列数
            for (int j = 0; j < array[i].length; j++) {
                //打印二维数组中的元素
                System.out.print(array[i][j] + "\t");
            }
            System.out.println();
        }
        System.out.println("--------------------------------");

        //3.二维数组中元素的初始化和打印
        int[][] array2 = {{1, 2, 3}, {4, 5, 6}};
        //使用外层for循环用于控制打印的行数
        for (int i = 0; i < array2.length; i++) {
            //使用内层for循环用于控制打印的列数
            for (int j = 0; j < array2[i].length; j++) {
                //打印二维数组中的元素
                System.out.print(array[i][j] + "\t");
            }
            System.out.println();
        }
    }
}
```

二维数组的分析：

​	array. length 表示二维数组的长度，也结束二维数组中元素的个数，也就是一维数组的个数，也就是行数

​	array[0]. length 表示二维数组中的第一个元素的长度，也就是第一行的长度和列数

​	array[0] [0] 表示二维数组中第一行第一列的数据

# 理解面向对象思想和概念

### 1.面向对象编程的概念

#### 1.1 什么是对象

​	**对象（Object）**是面向对象编程的基本单元，可以理解为现实世界中具体或抽象事物的软件表示。

- **现实类比**：比如“人”是一个抽象概念，而“张三”是一个具体的“人”对象，拥有年龄、姓名等属性，以及吃饭、走路等行为。
- **程序中的对象**：是 **数据（属性）** 和 **行为（方法）** 的封装体。

#### 1.2 什么是面向对象？

​	OOP 的核心思想是 **将数据和操作数据的方法（行为）封装在一起**，形成一个独立的实体（即 **对象**），并通过 **类（Class）** 来描述对象的共同特征。
它的主要目标是：

- **提高代码的可重用性**（通过继承、组合等方式）。
- **增强代码的可维护性**（通过封装、模块化）。
- **使代码更贴近现实世界的思维方式**（通过对象模拟现实实体）。

#### 1.3 什么是面向对象编程

​	面向对象编程（Object-Oriented Programming，OOP）是一种以**对象**为核心的编程范式，它将现实世界中的事物抽象为程序中的**对象**，并通过对象之间的交互来构建软件系统。OOP 是现代软件开发中最主流的编程范式之一，广泛应用于 Java、Python、C++、C# 等语言。

#### 1.4 如何学好面向对象编程？

​	深刻理解面向对象编程的三大特征：**封装、继承、多态**。

### 2.类、对象以及引用

#### 2.1 对象和类的概念

​	**对象 **是客观存在的实体，在java语言体现为内存空间的一块区域。

​	**类**     就是分类的概念，是对具有相同特征和行为的多个对象的抽象描述，在Java语言中包含描述特征的成员变量和描述行为的成员方法，是创建对象的模板。

#### 2.2 类的定义

​	（1）类定义的语法格式

​		class 类名 {

​		类体

​		}

​	注意：当类名由多个单词组成时，要求每个单词的首字母都要大写；

​	（2）成员变量定义的语法格式

​		class 类名{

​			数据类型 成员变量名 = 初始值；	— 其中=初始值通常省略，但分号不能省略

​		}

​	注意：当成员变量名由多个单词组成时，要求从第二个单词的首字母都要大写；

​	扩展：

​		  局部变量 — 主要指在方法体中声明的变量，作用方法从声明开始到方法体结束

​		  成员变量 —  主要指在方法体外类体内声明的变量，作用范围从声明到类体结束

#### 2.3 对象的创建

​	（1）语法格式

​		new 类名（）；

​	（2）注意事项

​		a. 当一个类定义完毕后，使用new关键字创建/构造对象的过程叫做 **类的实例化**；

​		b. 创建对象的本质结束在内存中的堆区申请存储空间，来存放该**对象**独有的特征信息

#### 2.4 引用

​	（1）基本概念

​		在Java语言中使用引用数据类型声明的变量叫做**引用型变量**，检查为“**引用**“。

​		**引用变量**主要用于记录**对象**在堆区的内存地址信息，便于下次访问。

​	（2）语法格式

​		类名   引用变量名；

​		如：

​			Person p； —表声明Person类型的引用变量p，本质上在栈区申请存储空间

​			Person p = new person();    — 表示声明引用变量p来记录Person类型对象的地址信息

​		引用变量名.成员变量名；

​		如：

​			p.name = "zhangsan";     —  表示使用引用变量p访问所指向堆区对象的姓名特征

```java
public class Person {
    String name;
    int age;
    public static void main(String[] args) {
        //声明Person类型的引用指向 创建Person类型的对象
        Person p = new Person();
        //修改成员变量的数值
        p.name = "Mike";
        p.age = 20;
        
        //打印该对象的成员变量信息
        System.out.println("我是"+p.name+ "今年" +p.age+ "岁l");
    }
}
```

### 3.成员方法

#### 3.1 语法格式

​	class 类名 {

​		返回值类型 成员方法名（形参列表）{

​			成员方法体；

​		}

​	}

注意：当成员变量由多个单词组成时，通常要求从第二个单词起每个单词首字母大写。

#### 3.2 格式的详细

​	（1）返回值类型：

​			返回值主要指从方法体内向方法体外返回的数据内容

​			但绘制类型主要指返回值的数据类型，可以是基本数据类型，也可以是引用数据类型;

​		如：

​			当返回值的数据内容是66时，则返回值类型写 int 即可；

​			当返回值的数据内容是3.14时，则返回值类型写 double 即可；

​			当返回值的数据内容是“hello”时 ，则返回值类型写 String 即可；

​		在方法体中使用return关键字来返回数据内容并结束当前方法。

​		如：

​			当返回的数据内容是66时，则方法体中写：return 66；

​			当返回的数据内容是num时，则方法体中写：return num；

​		若该方法不需要返回任何数据内容，则返回值类型写 Void 即可。

​	（2）形参列表

​		形式参数主要用于将方法体外的数据传入到方法体的内部，格式： 数据类型   形参名。

​		形参列表主要指多个形式参数组成的整体，格式如下：

​			数据类型  形参名1，数据类型  形参名2，…

​		如：

​			当传入的数据内容是66是，则形参列表写入：int i 即可；

​			当传入的数据内容是3.14时，则形参列表写入为： double  d 即可；

​			当传入的数据内容是“ hello ”时，则形参列表写入为：String s 即可；

​			当传入的数据内容是66和“ hello ”时，则形参列表写入为：int i,String s 即可；

​		若该方法不需要传入任何数据内容时，则形参列表微中子啥也不写即可；

​	（3）成员方法体

​		成员方法体主要编写描述该方法功能的语句。

​		如：

​			当该方法的功能返回打印时，则方法体中写  System. out. println("…");即可

​			当该方法的功能就是返回66时，则方法体中写 return 66；即可

#### 3.3 方法的调用

​	（1）语法格式

​		引用变量名.成员方法名（实参列表）

​	（2）注意事项

​		a.实际参数列表主要用于对形式参数列表进行初始化操作，因此参数的个数、类型、顺序等都必须与形参列表保存一致；

​	 	b.实参可以传递直接量、变量、表达式以及方法的调用等；

```java
public class Person {
    String name;
    int age;

    // 自定义成员方法打印所有特征的数值
    // 成员方法中允许直接访问成员变量
    void show() {
        System.out.println("我是" + name + "今年" + age + "岁了");
    }

    // 自定义成员方法实现将成员变量name修改为参数指定数值的行为
    void setName(String s) {
        name = s;
    }
    void setAge(int i) {
        age = i;
    }

    public static void main(String[] args) {
        // 声明Person类型的引用指向 创建Person类型的对象
        Person p = new Person();
        //打印该对象的成员变量信息
        p.show();
        System.out.println("------------------------------------");
        // 修改成员变量的数值
        p.name = "Make";
        p.age = 20;
        // 打印该对象的成员变量信息
        // System.out.println("我是"+p.name+ "今年" +p.age+ "岁了");
        p.show();
        System.out.println("------------------------------------");
        //调用成员方法实现姓名和年龄的修改
        p.setName("lisi");
        p.setAge(18);
        p.show();
        
    }
}

```



# 构造方法及方法重载

### 1.构造方法和方法重载

#### 1.1 构造方法

​	（1）语法格式

​		class 类名 {

​			类名（形参列表）{

​				构造方法体

​			}

​		}

```java
/*
*   编程实现Person类的定义
* */
public class Person2 {
    String name;        //用于描述姓名的成员变量
    int age;            //用于描述年龄的成员变量
    //自定义无参构造方法
    Person2() {

    }
    //自定义有参构造方法
    Person2(String name, int age) {
       // System.out.println("你到底会不会调用我呢？？？");
        // name = "张三";
        // /age = 18;
        this.name = name;
        this.age = age;
    }
    //实现打印使用特征的方法
    void show() {
        System.out.println("我是："+name+"，今年："+age+"岁了");

    }
    //自定义成员方法实现年龄增长一岁的行为
    void grow() {
        age++;
    }
    //自定义成员方法实现年龄增长参数指定数值的行为
    void grow(int age) {
        this.age += age;
    }
    public static void main(String[] args) {
        //声明Person类型的引用指向Person类型的对象
        Person2 p = new Person2();
        p.show();
        System.out.println("------------------------------------");
        Person2 p2 = new Person2("zhangsan",30);
        p2.show();
        System.out.println("------------------------------------");
        //调用上述重载的方法
        p2.grow();
        p2.show();      //zhangsan 31
        p2.grow(8);   //zhangsan 39
        p2.show();
    }
}
```

​	（2）注意事项

​		a.构造方法的名称与类名完全相同，没有返回值类型连void都不许有。

​		b. 当使用new关键字构造对象时会自动调用构造方法进行成员变量的初始化工作

​	（3）默认构造方法

​		a. 当一个类中没有自定义任何形式的构造方法时，编译器会自动添加一个无参的空构造方法，叫做默认/缺省构造方法，如：Person（）{ }

​		b. 若类中出现自定义构造方法，则编译器不在提供任何形式的构造方法

#### 1.2 方法的重载（Overload）

​	（1）基本概念

​		在Java语言中若方法的名称相同但参数列表不同，这样的方法之间构成重载关系。

​	（2）体现形式

​		方法重载的主要形式有：参数的个数不同、参数的类型不同、参数的顺序不同，与形参变量名和返回值类型无关，但建议返回值类型最好相同。

​		判断方法是否重载的核心：调用能否区分

​	（3）实际意义

​		对于调用者来说只需要记住一个方法名就可以调用各种不然的版本实现不然的效果。

```java
public class Point2 {
    int x;      //用于描述横坐标的成员变量
    int y;      //用于描述纵坐标的成员变量
    //无参构造
    Point2(){

    }
    //有参构造
    Point2(int x,int y){
        this.x = x;
        this.y = y;
    }

    void show(){
        System.out.println("横坐标x="+x+" ："+"纵坐标y="+y);
    }
    //自定义成员方法纵坐标减1的功能
    void up(){
        y--;
    }
    //自定义成员方法实现纵坐标减去参数指定数值的功能
    void up(int y){
       this.y-=y;
    }
    public static void main(String[] args) {
        Point2 p = new Point2();
        p.x = 10;
        p.y = 20;
        p.show();
        System.out.println("------------------");
        Point2 p2 = new Point2(30,40);
        p2.show();
        System.out.println("------------------");
        p2.up();
        p2.show();
        p2.up(3);
        p2.show();
    }
}
```

### 2.this关键字

#### 2.1 基本概念

​	在构造方法中this关键字代表当前正在构造的对象。

​	在成员方法中this关键字代表当前正在构造的对象。

​	原理分析：

​		当成员方法中访问创元变量是默认会加上this.(相当于汉语中“我们”)，当不同的引用调用同一个成员方法是会导致成员方法中的this不同，那么this.访问的结构随之不同。

#### 2.2 使用方法

​	（1）当形参变量和成员变量同名是，在构造方法或成员方法中通常优先使用形参变量，若希望使用成员变量就需要在变量名的前面加上this.进行说明。

​	（2）在构造方法的第一行使用this（实参）的方式可以调用本类中的其他构造方法

```java
public class Boy {
    String name;
    Boy(){
        //this("wuming");
        System.out.println("无参构造方法");
    }
    Boy(String name){
        //在构造方法的第一行可以调用奔类中的其他构造方法
        this();
        this.name = name;
        System.out.println("有参构造方法");
    }
    void show(){
        System.out.println("name= " + this.name);
    }
    public static void main(String[] args) {
        Boy b1 = new Boy("Tom");
        b1.show();

        System.out.println("------------------");
        Boy b2 = new Boy("Cat");
        b2.show();

        System.out.println("------------------");
        Boy b3 = null;
        //b3.show();    编译ok，运行发生NullPointerException 空指针异常

    }
}
```

### 3.方法的传参和递归调用

#### 3.1 方法的传参过程

​	（1）main方法是程序的入口，为main方法中的局部变量开辟内存空间并初始化；

​	（2）调用max方法是为max方法的形参变量开辟内存空间；

​	（3）使用实参变量给形参变量进行赋值操作，执行max方法的方法体；

​	（4）当max方法结束后释放形参变量内存空间；

​	（5）main方法中的res得到max方法的返回值然后继续向下执行；

​	（6）当mian方法结束后释放局部变量的内存空间；

​	掌握内容：

​		a.当基数数据类型的变量作为方法的参数传递时，形参变量的改变不会影响到实参；

​		b.当引用数据类型的变量作为方法的参数传递时，形参变量指向的内容发生改变后会影响到实参变量指向的内容；

​		c. 当引用数据类型的变量作为方法的参数传递时，形参变量改变指向后在改变指向的内容时不会影响到实参变量指向的内容；

#### 3.2 递归调用

​	（1）基本概念

​		 在一个方法体的内部调用当前方法自身的方式，叫做递归。

```java
/*
*   编程使用递归和递推两种方式实现费事数列中第n项数值的计算并返回
* */
public class FeeTest {
    //自定义成员方法实现递归方式计算第n项数值的计算并返回，n有参数指定
    //1 1 2 3 5 8 13 21 …
    int show (int n){
        //使用递归的方式计算并返回
        //从第三项器每项都是前两项数值的和，当n=1 或 n=2 时 返回1
      /*  if (1 == n || 2 == n) {
            return 1;
        } else {
            return show(n - 1) + show(n - 2);
        }
       */
        //使用递推的方式计算并返回
        int a = 1;
        int b = 1;
        for (int i = 3; i <= n; i++) {
            int c = a + b;
            a = b;
            b = c;
        }
        return b;
    }
    public static void main(String[] args) {
        //创建对象
        FeeTest ft = new FeeTest();
        //调用成员方法
        int n = ft.show(55);
        System.out.println(n);
    }
}

```

​	（2）注意事项

​		a.必须找到递归的规律和退出条件；

​		b.使用递归是得问题简单化而不是副组长化；

​		c.若递归影响到程序的执行性能则使用递推取代之；



# 面向对象的封装特性和static关键字

### 1.封装

#### 1.1基本概念

​	通常情况下测试类可以对封装类中的成员变量进行赋值，若赋值的数据合法但不合理时，无论是编译阶段话说运行阶段都不会报错或者给出提示，此时与实现生活不符。

​	为了避面上述错误的发生，就需要对成员变量进行密封包装处理，该机制就叫做封装，换句话说，封装就是一种保证长远变量值合理性的机制。

#### 1.2 实现流程

​	（1）私有化成员变量，使用private关键字修饰；

​	（2）提供公有的get和set方法，在方法体中进行合理值的判断；

​	（3）在构造方法中调用set方法进行合理值的判断

### 2.static关键字

#### 2.1 基本概念

​	通常情况下成员变量隶属于对象层级，每个创建一个对象就需要申请独立的内存空间来存放该对象独立的成员变量信息，若所有对象的某个成员变量数值完全一样却又单独存放会造成内存空间的浪费。

​	为了解决上诉问题，则使用static关键字修饰成员变量，此时该成员变量由对象层级提示为类层级被所有对象共享，该成员变量随着类的加载准备就绪，与是否创建对象无关。

​	static关键字也可以修饰成员方法，推荐使用  类名.  的方式访问。

#### 2.2 使用方法

​	（1）在非静态的成员方法中既能访问非静态的成员也能访问静态的成员；

​		（成员：成员变量+成员方法）

​	（2）在静态的成员方法中只能访问静态的成员不能访问非静态的成员；

​		（成员：成员变量+成员方法）

​	（3）只有隶属于类层级被所有对象共享的内容才可以使用static修饰；

​		（不能滥用static关键字）

#### 2.3 单例设计模式

​	（1）基本概念

​		在某些特殊的场合中一个类对外提供且只提供一个对象，这样的类叫做单列类。而设计单列类的思想和模式叫做单列设计模式，主要用于固定的场合。

​	（2）实现流程

​		a.私有化构造方法，使用peivate关键字修饰；

​		b.声明本类类型的引用指向本类类型的对象，使用private static共同修饰；

​		c.提供公有的get方法负责将成员变量的数值返回回去，使用static关键字修修饰；

​	（3）实现方式

​		单列设计模式的实现方法有两种：饿汉式 和 懒汉式

### 3.继承

#### 3.1 基本概念

​	当多个类之间有相同的特征和行为是，可以将相同的内容提取出来组成一个公共类，让多个类吸收公告类中已有特征和行为而在多个类的内部编写之间独有特征和行为的方式，叫做  **继承**。

​	使用 **继承** 可以提高大妈的复用性和扩展性以及可维护性。

​	在Java语言中使用  **extend（扩展）**关键字来表达继续关系。

如：

​	public class Student extend Person {  }  — 表示Student类继承Person类

​	其中Person类叫做基类、父类、超类

​	其中Student类叫做派生类、子类、孩子类

#### 3.2 注意事项

​	（1）子类可以继承父类的成员变量和成员方法，其中私有成员变量可以继承但不可以直接使用，子类不可以继承父类的构造方法和私有方法

​	（2）无论使用何种方式构造子类对象时，都会自动调用父类中的无参构造方法来初始化从父类中继承下来的成员变量，相当于在子类构造方法第一行增加代码：super（）的效果

​	（3）使用继承必须满足 子类 is a 父类 的逻辑关系，也就是不能滥用继承

​	（4）Java语言中只支持单继承不支持多继承，也就是一个子类只能有一个父类，但一个父类可以有多个子类。

#### 3.3方法的重写（override）

​	（1）基本概念

​		若从父类中继承下来的方法不满足子类的需求时，就需要在子类中重新写一个与父类中方法一样的方发来覆盖从父类中继承的版本，这种方法加载重写。

​	（2）重写原则

​		a.要求方法名相同、参数列表相同、返回值类型相同、从jdk1.5开始允许返回子类类型

​		b.要求方法的访问权限不能变小，可以相同或者变大。

​		c.要求不能抛开更大的异常（异常机制）。

### 4.访问控制

#### 4.1 常用的访问控制符

![image-20250702194613870](C:\Users\26803\AppData\Roaming\Typora\typora-user-images\image-20250702194613870.png)

掌握内容：

​	a.public修饰的内容可以在任意位置使用；

​	b.private修饰的内容只能在类中使用；

​	c.通常情况下，成员变量都在使用private修饰，成员方法都使用public修饰；

#### 4.2 包的定义

​	package 包名；

​	package 包名1.包名2...包名n；	— 便于管理，避免命名冲突的问题

### 5.final关键字

#### 	5.1 基本概念

​		final本意为“最终的，不可更改的”，该关键字可以修饰类、成员方法、成员变量等。

#### 	5.2 使用方法

​		final关键字修饰类表示该类不能被继承。

​			— 为了防止滥用继承带来的危害

​			— 如：java.lang.String类等

​		final关键字修饰成员方法表示该方法不能被重写凡可以被继承

​			— 为了防止不经意间造成的方法重写

​			— 如：java.text.DateFormat类中的format方法等

​		final关键字修饰成员变量表示该成员变量必须初始化而且不能更改。

​			— 为了防止不经意见造成数值的更改。

​			— 如：java.lang.Thread类中的MAX_PRIORTTY等

​		扩展：

​			在以后的开发中很少单独使用static关键字或final关键字修饰成员变量，通常都是使用public static final共同修饰成员变量来表达常量的含义，常量的含义，常量的命名规则是：要求所有字母大写，不同单词之间采用下划线连接，如：	public static final double PI = 3.14；

​	

# 面向对象的多态特性及抽象类和接口

### 1.多态

#### 1.1 基本概念

​	多态主要指用一种事务表现出来的多种形态。

#### 1.2 语法格式

​	父类类型 引用变量名  =   new  子类型类型（）；

​	如：

​		Person pw = new Worker（）；

​		pw.show();

​	解析：

​		编译阶段调用Person类中show方法，在运行阶段调用Worker类中重写以后的show方法

#### 1.3 多态的效果

​	（1）当父类的引用指向子类的对象时，父类的引用可以直接调用父类独有的方法；

​	（2）当父类的引用指向子类的对象时，父类的引用不可以直接调用子类独有的方法；	

​	（3）对于父子类都有的非静态成员方法来说，编译和运行阶段调用父类版本，隶属于类层级，因此与指向的对象无关；

#### 1.4 引用数据类型之间的转换

​	（1）引用数据类型之间的转换分为：自动类型转换  和  强制类型转换。

​		其中自动类型转换主要只从小范围到大范围之间的转换，也就是子类到父类的转换

​		其中强制类型转换主要只从大范围到小范围之间的转换，也就是父类到子类的转换

​	（2）引用数据类型之间的转换必须发送在父子类之间，否则编译报错。

​	（3）若转换到的目标类型是子类类型但不是该引用正真指向的子类类型，则编译通过，运行阶段发生类型转换异常。

​	（4）为了避免上述错误的发生，可以使用instanceof进行判断，具体格式如下：

1.5 多态的意义

​	多态的实际意义在于可以屏蔽不同子类的差异性实现通用的编程，但可以调用不同的方法带来不同的结果。

### 2.抽象类

#### 2.1抽象方法的概念

​	抽象方法就是指不能具体实现的方法，也就是没有方法体并使用abstract关键字修饰

​	语法格式：

​		访问控制符abstract 返回值类型 方法名称（形式列表）

#### 2.2抽象类的概念

​	抽象类就是指不能具体实例化的类，也就是不能创建对象并使用abstract关键字修饰

#### 2.3注意事项

​	（1）抽象类中可以有成员变量、构造方法以及成员方法；

​	（2）抽象类中可以有抽象方法也可以没有抽象方法；

​	（3）拥有抽象方法的类必须是抽象类，因此严格来说，具有抽象方法并且使用abstract关键字修饰的类才算真正意义上的抽象类。

#### 2.4 实际意义

​	抽象类的意义不在与自身创建对象而在与被继承，当一个类继承抽象类后必须重写抽象类中的抽象方法，否则该类也变成抽象类。

​	也就是是抽象类对子类具有强制性和规范性，因此叫做模板设计模式。

​	分享：

​		在开发中推荐使用对台的语法格式，当父类的引用指向子类的对象时，那么父类引用直接调用的所有方法一定时父类拥有的方法，若希望更好子类时，只需要将new关键字多么的类型修改而其他地方无需更改立即生效，从而提高了代码的可维护性。

​		该方法的确定就是：父类引用不能直接放完子类独有的方法，若访问则需要强转。

### 3. 接口

#### 3.1 基本概念

​	接口技术一种比抽象类还抽象的类，体现为所有成员方法都是抽象方法。

​	定义类的关键字class，而定义接口的关键字是interface。

​	继承类的关键字是extends，而实现接口的关键字是implements。

#### 3.2 类和接口之间的关系

​	类和类之间的关系	使用extends关键字表达继承的关系	支持单继承

​	类和接口之间的关系	使用implements关键字表达实现的关系	支持多实现

​	接口和接口之间的关系	使用extends关键字表达继承的关系	支持多继承

#### 3.3 抽象类和接口之间的区别

​	（1）定义抽象类的关键字是abstract class，而定义接口的关键字是interface。

​	（2）继承抽象类的关键字是extends，而实现接口的关键字是implements。

​	（3）继承同性恋支持单继承，而实现接口可以多实现

​	（4）抽象类中可以有构造方法，而接口不可以有构造方法。

​	（5）抽象类中可以有成员变量，而接口中只可以有常量。

​	（6）抽象类中可以有成员方法，而接口中只可以有抽象方法。

​	（7）抽象类中增加方法可以不影响子类，而接口中增加方法通常影响子类。

​	（8）从jdk1.8开始允许接口中出现非抽象方法，但需要使用default关键字修饰。

### 4.内部类

#### 4.1 基本概念

​	 当一个类的定义出现在另外一个类的类体中时，那么这个类叫做内部类，而这个内部类所在的类叫做外部类。

​	类中的内容：成员变量、成员方法、构造方法、静态成员、构造块和恶静态代码块、内部类

#### 4.2 语法格式

​	class 外部类名{

​		class 内部类名{

​			内部类的类体

​		}

​	}

#### 4.3 实际作用

​	当一个类存在的价值仅仅是为了摸一个类单独服务时，那么就可以将这个类定义为使用服务类中的内部类，这样可以隐藏该类的实现细节并且可以方便的访问问外部类的私有成员而不再需要提供公有的 get和set方法。

4.4 基本分类

​	普通内部类  —  直接将一个类的定义放在另外一个类的类体中。

​	静态内部类  —  使用static关键字修饰的内部类

​	局部内部类  —  直接将一个类的定义放在方法体的内部时。

​			     —  作用 范围是从声明开始一直到方法体结束。

# Java的各种数据类型对象库的处理应用

### 1.Object类

#### 1.1 常用的包

​	java.lang包  — 该包是Java语言中的核心包，该包中的内容有Java虚拟机自导入

​			      — String类、System类等

​	java.util包    —该包是Java语言中的工具包，里面包含了大量的工具类和集合类等

​			      —如：Scanner类、Random类等

​	java.net包    — 该包是Java语言中的网络包，里面 包含了大量网络编程的类等

​			      — 如：ServerSocket类、Socket类等 

​	java.sql包     —该包是操作数据库的使用类和接口。

​	java.io包       —该包是输入输出包，包括读写各种设备。

#### 1.2 Object类

（1）基本概念 

​	java.lang.Object类是所有类层次结构的根类，任何类都是该类的直接或间接子类。

（2）常用的方法

​	Object()  —  使用无参方法构造对象。

​	boolean equals（Object  obj）— 用于判断调用对象是否与参数对象相等。

​		— 该方法默认比较两个对象的地址，与 == 运算符结构相同。

​		— 为了使得该方法比较两个对象的内容，则需要重写该方法。

​		— 若该方法重写后，则应用重写hashCode方法来维护hashCode方法的常规协定

​	int hashCode（）—  用于获取调用对象的哈希码值（内存地址的编号）。

​		— 若调用equals方法的结果相等，则各自调用hashCode方法的结果相同。

​		— 若调用equals方法的结果不相等，则各自调用hashCode方法的结果不相同。

​		— 为了维护上述的常规协定与equals方法结果保持一致，就需要重写该方法。

### 2.包装类的数学处理类

#### 2.1包装类的概念

​	由于Java语言是一门纯面向对象编程语言，而8中基本数据类型 声明的变量并不是对象，为了满足Java语言的特性就血药对这些变量进行对象化处理，而实现该功能的相关类就叫做包装类。

#### 2.2 包装类的分类

​	int => java.lang.Integer类

​	char => java.lang.Character类

​	其他类型对应的包装类就是将首字母变成大写

#### 2.3 Integer类

（1）基本概念

​	java.lang.Integer类是int类型的包装类，里面包含了一个int类型的成员变量。

​	该类由final关键字修饰表示不能被继承。

（2）常用方法

​	Integer（int value）—根据参数指定的整数构造对象

​	Integer（String s）—根据参数指定的字符串构造对象

​	该类重写了equals（）、hashCode（）、toString（）方法

​	int intValue（）—用于获取调用对象中的整数数据并返回

​	static Integer valueOf（int i）—根据参数指定的整数返回对应的Integer对象

​	static int parseInt（String s）—用于将String类型转换为int类型并返回

#### 2.4 BigDecimal类

（1）基本概念

​	由于float类型和double类型的运算可能会有误差，为了实现精确运算则需要借助Java.math.BigDecimal类型加以描述，

（2）常用方法

​	BigDecimal（String val）— 根据参数指定的字符串构造对象

​	BigDecimal add（BigDecimal augend）—用于计算调用对象和参数对象的和并返回

​	BigDecimal subtract（BigDecimal subtrahend）— 用于计算调用对象和参数对象的差并返回

​	BigDecimal multiply（BigDecimal multiplicand）—用于计算调用对象和参数对象的积并返回

​	BigDecimal divide（BigDecimal divisor）—用于计算机调用对象和参数对象的商并返回。

### 3.String类

#### 3.1基本概念

​	java.lang.string类用与描述字符串，java应用程序中使用字符串字面值都可以作为String类型 的对象加以描述，如“abc“等。

​	该类描述的字符串内容是个常量，一旦常见完毕后则不能更改，因此可以被共享。

#### 3.2 常量池

​	由于String类型描述的字符串内容是个常量不可改变，因此Java虚拟机提供了一个常量池，当Java程序中出现字符串内容是就可以放入常量池，若后续出现重复的字符串内容则直接使用池中已有对象而不需再次创建，从而提高了性能。



# Java字符串和日期处理

### 1.String类的常用方法

①String定义有charAt方法：

- char charAt（int index）—方法charAt用于返回字符串位置的字符。参数index表示指定的位置

- int length（）—返回字符串字符序列的长度

②String类的基本方法

- boolean contains（CharSequences）	—用于判断当前字符串是否包含参数指定的内容

- String toLowerCase（）		—返回字符串的小写形式

- String toUpperCase（）		—返回字符串的大写形式

- String trim（）				—返回去掉前导和后续空白的字符串

- boolean startsWith（String prefix）—判断字符串是否以参数字符串开头

- boolean endsWith（String suffix） —判断字符串是否以参数字符串结尾

③String类中的equals方法

- String类重写了继承自Object的equals方法，其逻辑为：字符序列相同的String对象equals返回true。

- 通常使用equals方法判断两个字符串的字符序列是否相同。

- String还提供了equalslanoreCase方法，该方法在判断是将忽略大小写。

④方法indexOf

- indexOf方法用于实现在字符串中检索例外一个字符串。

- String提供几个重载的indexOf方法：

  int indexOf（String str）	—在字符串中检索str,返回其第一次出现的位置，如果找不到则返回-1

  int indexOf（string str，int fromlndex）—类似indexOf（String），但是是从字符串的fromlndex位置开始检索

⑤方法substring

- substring方法用于返回一个字符串的子字符串。

- substring常用重载方法定义如下：

  String subString（int beginlndex，int endlndex）—返回字符串从下标beginlndex（包括）开始到endindex（不包括）结束的子字符串

  String subString（int beginlndex）—返回字符串中从下标beginlndex（包括）开始到字符串结尾的子字符串。

### 2.StringBuilder类和StringBuffer类

#### 2.1基本概念

​	由于String类型描述的字符串内容是个常量不可更改，当程序中出现大量雷士的字符串时需要单独存放从而浪费内存空间，若希望使用一块内存空间进行存储并可以修改字符串内容，则应该使用StingBullder类和StringBuffer类。

​	其中StringBuffer类从jdk1.0开始存在，该类支持线程安全，因此访问的效率要比较。

​	其中StringBuilder类从jdk1.5开始存在，该类不支持线程安全，访问的效率比较高。

#### 2.2 常用方法

​	①StringBuffer类的常用构造方法：

​		StringBuffer()	—构造一个字符串缓冲区，其中没有字符，初始容量为16个字符。

​		StringBuffer(CharSequence seq)	—构造一个包含与指定字符相同的字符串缓冲区。

​		StringBuffer(int capacity)	—构造一个字符串缓冲区，其中没有字符，但是包含指定的初始容量capacity。

​		StringBuffer(String str)	—构造一个指定字符串内容的字符串缓冲区。

​	②StringBuilder类的常用方法：

​		StringBuilder append(String str)	—追加字符串

​		StringBuilder insert（int offset，String str）—插入字符串

​		Stringbuilder delete（int start，int end）—删除字符串

​		Stringbuilder replace（int start，int end，String str）—替换字符串

​		StringBuilder reverse（）—字符串反转

### 3.日期相关的类

#### 3.1Date类

​	（1）基本概念

​		java.util.Date类用于描述特定的瞬间，可以精确到毫秒。

​	（2）构造方法

​		Date（）—分配Date对象并初始化此对象，以表示分配它的时间

​		Date（long date）分配Date对象并初始化此对象，以表示自从标准基准时间。

#### 3.2 SimpleDatFormat类

​	（1）基本概念

​	java.text.SimpleDateFormat类主要用于实现日期和文本之间的相关转换。

​	（2）构造方法

​	SimpleDateFormat（String pattern）—参数用于说明给是的模式匹配字符串

#### 3.3 Calendar类

​	（1）基本概念 

​		java.util.Calender类用于封装日历信息，其主要作用在于其方法可以对时间分量进行运算。

​		Calender是抽象类，其具体子类针对不同国家的日历系统，其中应用最广泛的是GregorianCalendar（格里高利历），对应世界上绝大部分大数国家/地区使用的标准日历系统。

​	（2）基本用法

​		Calendar c = Calendar.getinstance();

​		—通常使用Calender的静态方法getinstance获取Calendar对象，getinstance方法将根据系统地域信息返回不同的Calendar类的实现。



# 包装类、集合、数据结构

### 1.集合（容器）框架

#### 1.1集合的由来

​	当需要在程序中记录单个数据内容是，则声明一个变量即可；

​	当需要在程序中记录多个数据相同的数据内容是，则声明一个一维数组即可；

​	当需要在程序中记录多个类型不同的数据内容，则构造一个对象即可；

​	当需要在程序中记录多个类型相同的对象时，则声明一个对象数组即可；

​	当需要在程序中记录多个类型不同的对象时，则声明一个集合即可；

#### 1.2框架结构

- 在java语言中集合框架的顶层是：java.util.collection集合 和 java.util.Map集合

- 其中Collection集合中操作元素的基本单位是：单个元素。

- 其中Map集合中操作元素的基本单位是：单对元素

  

  在以后的开发中很少直接使用Collection集合，而是使用该集合的子集合：List集合、Queue集合、Set集合等。

### 2.Collection集合

#### 2.1 基本概念

​	java.util.Collection集合是集合框架的跟接口，其他接口是该接口的子接口。

#### 2.2常用方法

​	boolean add(Ee)	—向集合中添加对象

​	boolean contains（Object o） —判断是否包含指定对象

​	boolean remove（Object o）—从集合中删除对象

​	void clear（）—清空集合

​	int size（）—返回包含对象的个数

​	boolean isEmpty（）—判断是否为空

### 3.list结合

#### 3.1基本概念

​	Java.util.List集合是Collection集合的子集合，该集合中元素有先后次序其允许重复

- 该集合的主要实现类有：ArrayList类、LinkedList类、Stack类、Vector类等
- 其中ArrayList类的底层是采用动态数组进行数据管理，访问方便，增删不方便。
- 其实中LinkedList类的底层是采用链表进行数据管理，增删方便，访问不方便。
- 其中Stack类主要用于描述具有后进先出特征的数据结构，叫做栈，last in first out

该类的底层是采用数组进行数据的管理

- 其中vector类的地产采用数组进行数据的管理，与ArrayList类相比属于线程安全的类，因此效率比较低，在以后的开发中推荐使用ArrayList类取代之。

#### 3.2 常用方法

- LIst除了继承Collection定义的方法外，还根据其线性标的数据结构定义了一系列方法，其中最常用的就是基于下标的get和set方法。

​	void add（int index,E elemrnt）—向集合中指定位置添加元素

​	boolean addAll(int index,Collection<?extends E>c)  — 向集合中添加所有元素

​	E get(int index)  —从集合中获取指定元素

​	E set(int index,E element)  —修改指定位置的元素

- LIst还提供有类似与String的indexOf和lastlndexOf方法，用于在集合中检索某个对象，其判断逻辑为：（o==null?get(i)==null:o.equals(get(i))）
- toArrag方法是继承自Collection的方法，可以将集合中的对象序列以对象数组的返回式返回。
- List的subList方法用于获取子List。
- 需要注意的是，subList获取的List与原List占有相同的存储空间，对子List的操作会影响到原LIst。

### 4.泛型机制

#### 4.1基本概念

​	通常情况下集合中可以存放不同类型的对象，本质上是将这些对象全部看做Object类型放入的，因此从集合中取出元素是也是Object类型，为了表达元素最真实的数据类型就需要 强制类型转换，而强制类型转换可能发生类型转换异常。

​	为了避免上述错误的发生，从jdk1.5开始提出泛型机制，也就是在集合名称的右侧使用<数据类型>的方式明确要求该集合可以存放的元素类型，若放入其它类型则编译报错

- 泛型是Java SE 1.5 引入的特性，泛型的本质是参数化类型。在类、接口和方法的定义过程中，所操作的数据类型被传入的参数指定。

#### 4.2原理分析

​	泛型的本质检索参数化类型，也就是让数据类型作为参数传递，集合定义中的E相当于形式参数负责占位，而使用集合是<>中的数据类型相当于实际参数负责给形式参数初始化、当初始化完毕后使用E被替换成实际参数表示的类型进行使用。

如：

​	其中i叫做形式参数，负责占位					其中E叫做形式参数，负责占位

​	int i = 5；									E = String；

​	int i = 10；								      E = Student；

​	public void show（int i）{					       public interFace LIst<E>{

​		…											…	

​	}											}

​	其中5叫做实际参数，用于给形式参数初始化		其中String叫做实际参数

​	show（5）；								List<String>  lt1   = …；

​	show（10）；							       List<String>  lt2  = …；

# Java中的数据结构

### 1.Queue集合

#### 1.1 基本概念

​	java.util.Queue集合是Collection集合的子集合，与LIst集合是评级关系。

​	该集合的主要实现类是：LinkedLIst类，因为该类在增删方面有一定的优势。

​	该集合用于描述具有先进先出特征的数据类型，叫做队列（first in first out）。

#### 1.2 主要方法

​	boolean offer（E e）—将一个对象添加至队尾，若添加成功则返回ture

​	E poll（）—从队首删除并返回一个元素

​	E peek（）—返回队首的元素（但并不删除）

### 2.Set集合

#### 2.1基本概念

​	Java.util.Set集合是Collection集合的子集合，让List集合以及Queue集合平级关系

​	该集合与LIst集合的主要区别在于：元素没有先后次序并且不允许重复的元素

​	该集合的主要实现类有：HashSet类和TreeSet类。

​	其中HashSet类的底层采用哈希表进行数据管理的。

​	其中TreeSet类的底层采用二叉树进行数据管理的。

#### 2.2 Set集合的遍历

- 所有Collection的实现类都实现了其Iterator方法，该方法返回了一个Iterato接口类型的对象，用于实现对集合元素的迭代遍历。

​	Iterator接口的主要方法有：

​	booleanhasNext（）	  — 判断集合中是否有可以迭代/访问的元素

​	E next（）			    — 用于取出一个元素并指向下一个元素

​	void remove（）		 — 用于删除访问到的最后一个元素

#### 2.3 增强班的for循环（for each结构）

（1）语法格式

​	for（元素类型 变量 ： 数组名/集合名）{

​		循环体

​	}

（2）执行流程

​	不断地从数组或集合和中取出一个元素并赋值给变量并执行循环体，知道处理完毕所有元素为止。

​	总结：

​		遍历Set集合的方式有三种：toString（）、for each结构、迭代器方式

​		遍历List集合的方式有四种：除了上诉三种方式外，还有get方式。

### 3.Map集合

#### 3.1 基本概念

​	java.util.Map<K,V>集合中操作元素的基本单位是：单对元素，其中类型参数如下：

​		K — 此映射所维护的键（key）的类型

​		V — 映射值（value）的类型

​	该集合中不允许出现重复的键，每个键最多只能映射到一个值。

​	该集合的主要实现类有：HashMap类 和 TreeMap类。

​	其中HashMap类的底层是采用哈希表进行数据管理的。

​	其中TreeMap类的底层是采用二叉树进行数据管理的。

#### 3.2 常用方法

​	V put （K key，V value） —将key-Value对存入Map，若集合中已经包含该key，则替换该Key所对应的Value，返回值为该Key原来所对应的Value，若没有则返回null

​	V get （Object key）—返回与参数Key所对应的Value对象，如果不存在则返回null

#### 3.3 Map集合的性能调优

- Capacity：容量，hasj表里bucket（桶）的数量，也就是散列数组大小。
- Initial capacity：初始容量，创建hash表时初始bucket的数量，默认构建容量是16，也可以使用特定容量。
- Size：大小，当前散列表中存储数据的数量。
- Load factor：加载因子，默认值0.75（75%），当向散列表增加数据时如果size/capacity的值大于Load factor则发生扩容并且重新散列（rehash）
- 性能优化：加载因子较小时候散列查找性能会提高，同时也浪费了散列桶空间容量。0.75是性能和空间相对平衡结果。在创建散列表时候指定合理容量，减少rehash提高性能。

#### 3.4 Map集合的实际应用

- Map集合是面向查询优化的数据结果，在大数据量情况下有着优良的查询性能
- 经常用于根据key检索Value的业务场景
- 用户登录数据缓存：用户名是Key，用户对象是value，在登录验证时候根据用户名快速查询用户信息。
- 登录会话状态保持：在网站编程中，用户会话状态保持矜持采用Map存储，可以快速在数以万计的信息中快速确定用户是否已经登录。

# Java的异常处理机制和文件流

### 1.异常机制

#### 1.1基本概念

​	异常就是“不正常”的含义，在Java语言中使用表示运行阶段发生的错误。

​	Java.lang.Throwable类是Java语言中所有错误（Error）和异常（Exception）的超类。

​	其中Error类主要用于描述比较严重无法编码解决的问题，如：JVM挂了。

​	其中Exception类主要描述比较轻微可以编码解决的问题，如：0作为除数。

#### 1.2 基本分类

​	Java.lang.Exceptionl类是属于异常类的超类，主要分为以下两大类：

​		RuntimeException - 运行时异常，也叫作非检测行异常

​		IOException和其他异常 - 其它异常，也叫做检测型异常

​			-所谓检查行异常就是在编译阶段能够被编译器检查出来的异常

​	其中RuntimeException类的主要子类：

​		ArithmeticException - 算术异常

​		ArrayIndexOutOfBoundsException - 数组下标越界异常

​		NullPointerException - 空指针异常

​		ClassCastException - 类型转换异常

​		NumberFormatException - 数字给是异常

​	注意：

​		当程序执行过程中发生异常单没有手动处理时，有Java虚拟机采用默认方式处理，而默认处理方式就是：打印异常名称、异常原因、异常发生的位置等并终止程序。

#### 1.3 异常的避免

​	在以后的开发中尽量使用if条件判断来避免异常的发生

#### 1.4 异常的捕获

（1）语法格式

​	try{

​		编写可能发生异常的语句

​	}

​	catch（异常类型 变量名）{

​		编写针对该类异常的处理语句

​	}

​	…

​	finally{

​		编写无论是否发生异常都应该执行的语句；

​	}

（2）注意事项

​	a.当需要编写多个catch分支时，切记小型类的异常应该放在大类型异常的上面。

​	b.finally主要用于编写善后处理的语句。

（3）执行流程

​	try{

​		a；

​		b； —可能发生的异常的语句

​		c；

​	}catch（…）{

​		d；

​	}finally{

​		e；

​	}

​	当上诉程序执行过程没有发生异常时的执行流程：a b c e;

​	当上诉程序执行过程发生异常时的执行流程：a b d e;

#### 1.5 异常的抛出

（1）基本概念

- 程序中会定义许多方法，这些方法中可能会因某些错误而引发异常，但你不希望直接在这个方法中处理这些异常，而希望交给调用他的方法统一处理，这时候可以使用“throws”关键字来声明这个方法将会抛出异常

（2）语法格式

​	访问权限 返回值类型 方法名称（形参列表） throws 异常类型1，异常类型2，…{}

（3）方法的重写原则

​	a.要求方法名相同、参数列表相同、返回值类型相同，从idk1.5开始允许返回子类类型	

​	b.要求方法的访问权限不能变小，可以相同或者变大

​	c.要求不能抛出更大的异常

#### 1.6 自定义异常

（1）基本概念

​	虽然Java官方提供了大量的异常类，但一定不会包含所有开发中可能出现的异常，在Java程序中若需要表达特定问题的特定异常时，就需要程序员自定义异常来描述。

（2）实现流程

​	a.自定义xxxxException继承自Exception类或者其子类:

​	b.提供两个版本的构造方法:无参构造方法和字符串作为参数的构造方法;

### 2.1 File类

#### 2.1 基本概念

​	java.io.File类主要用于描述文件和目录的路径信息，可以获取名称、大小等属性信息

#### 2.2 常用方法

​	boolean delete()	—用于删除文件，当文件目录时要求是空目录

​	boolean createNewFile（）	—用于创建新的空文件

​	boolean madir（）	—用于创建目录

​	Boolean mkdirs（）	—用于创建多级目录



# Java的IO流处理

### 1. IO流

#### 1.1 基本概念

​	I/O就是Input/Output的简写，也就是输入输出的含义。

​	I/O流就是像流水一样不间断地进行输入输出的状态。

#### 1.2 基本分类

​	按照数据读写的基本单位不同分为:字节流和字流。

​	其中字节流主要指以字节为单位进行读写的流，可以处理任意类型的文件；

​	其中字符流主要指以字符(2个字节)为单位进行读写的流，只能处理文本文件;



​	按照数据流动的方向不同分为:输入流  和  输出流(站在程序的角度)。

​	其中输入流主要指从文件中读取数据内容输入到程序中，也就是读文件;

​	其中输出流主要指将程序中的数据内容输出到文件中，也就是写文件;

#### 2.3FileOutputStream类

（1）基本概念

​	java.io.FileOutputStream类主要用于将图像数据之类的原始字节流写入输出流中。

（2）常用方法

​	java.io.FileOutputStream类主要用于将像数据之类的原始字节流写入到输出流。

​	常用的构造方法如下:

​		FileOutputStream(Stringname)  —根据参数指定的文件名来构造对象。

​		FileOutputStream(Stringname, boolean append)

​				—表示以追加的方式根据参数指定的文件名来构造对象。

#### 1.4 BufferedWriter类

（1）基本概念
		java.io,BufferedReader类主要用于从输入流中读取单个字符、字符数组以及一行字符串内容。

（2）常用方法

​		BufferedReader(Readerin) —根据参数指定的引用来构造对象。
​			—其中Reader类是个抽象类，实参需要传递子类的对象。

（3）常用成员方法

​	int read（）	—用于读取单个字符并返回，若读取到文件末尾则返回-1，否则返回实际读取到字符的整数值

​	int read（char[]cbuf,int off,int len）—用于从输入流中读取len个字符放入数组cbuf中下标从off开始的位置上，若读取到未尾则返回1，否则返回实际读取到的字符个数

​	int read（char[]cbuf）—用于从输入流中读满整个数组cbuf

​	String readLine（）—用于读取一行字符串并返回

​	void close（）—用于关闭文件输出刘并释放有关的资源

#### 1.5 PrintStream类

（1）基本概念

​	java.io.PrintStream类主要用于方便地打印各种数据内容并且自动刷新。

（2）常用方法
	PrintStream(OutputStreamout)	—根据参数指定的引用来构造对象。
		—其中OutputStream类是个抽象类，实参需要传递子类的对象。	

#### 1.6 0bjectOutputStream类

(1)基本概念

​	java.io.0bject0utputStream类主要用于将Java语言中的对象整体写入输出流中。

​	只能将支持 java.io.Serializable 接口的对象写入流中。

​	类通过实现 java.io.Serializable 接口以启用其序列化功能。

​	所谓序列化就是指将一个对象相关的所有信息有效组织成字节序列的转化过程。

#### 1.7 bjectInputStream类

(1)基本概念

​	java.io.0bjectInputStream类主要用于从输入流中一次性将一个对象的内容读取出来实现了从字节序列到对象的转化过程，叫做反序列化。

（2）常用方法

​	ObjectlmputStream(lnputStream in)	—根据参数指定的引用来构造对象

​										其中InputStream类是个抽象类，实参需要传递子类的对象

​	Object readObject()		—主要用于从输入流中读取一个对象并返回无法通过返回值来判断是否读取到文件的末尾

​	void close()		—用于关闭文件输出流并释放有关的资源

经验:
	当需要写入多个对象到文件中时，建议先将多个对象放入一个集合对象中，然后将集合对象看做一个整体只需要调用一次write0bject方法就可以写入所有内容，此时只需要调用一次read0biect方法就可以将所有内容读取出来，这样就避免了通过返回值来判断是否读取到文件的末尾。

#### 1.8transieht关键字

​	transient是Javá语言的关键字，用来表示一个域不是该对象串行化的一部分当一个对象被串行化的时候，transient型变量的值不包括在串行化的表示中然而非transient型的变量是被包括进去的。

# Java的多线程处理

### 1.线程

#### 1.1基本概念

​	程序 - 数据结构 + 算法，主要指存放在硬盘上的可执行文件。
​	进程 - 主要指运行在内存中的程序。
​	目前主流的操作系统都支持多进程，为了使得操作系统能够同时执行多个任务，但进程是重量级的，新建进程对系统的资源消耗比较大，因此进程的数量比较局限。

​	线程是进程内部的程序流，也就是操作系统中支持多进程，而每个进程的内部又可以支持多线程，线程是轻量级的，新建线程共享所在进程的系统资源，因此以后的开发中都采用多线程技术。

​	多线程技术采用时间片轮转法实现并发执行，所谓并发就是指宏观并行微观串行。

#### 1.2 线程的创建

（1）创建和启动的方式

​	java.lang.Thread类用于描述线程，Java 虚拟机允许应用程序并发地运行多个执行线程，而线程的创建和启动方式如下:

​	①自定义类继承Thread类并重写run方法，创建该类的实例调用start方法。

​	②自定义类实现Runnable接口并重写run方法，创建该类的实例作为实参来构造Thread类型的对象，然后使用Thread类型的对象调用start方法。
(2)相关方法的解析
​	Thread()-使用无参方式构造对象。

​	Thread(String name)-根据参数指定的名称来构造对象。

​	Thread(Runnable target)-根据参数指定的接口引用来构造对象。

​	Thread(Runnable target，String name)-根据参数指定的引用和名称构造对象。
​	void run()	—若使用Runnable类型的引用构造出来的对象调用该方法，则最终调用引用所指向对象的run方法，否则调用该方法啥也不做。
​	void start	—用于启动线程，Java虚拟机会自动调用该线程的run方法。

（3）原理分析

​	a.执行main方法的线程叫做主线程，执行run方法的线程叫做子线程。

​	b.main方法是程序的入口，最开始只有主线程来依次执行main方法中的代码，当start方法调用成功后，线程的个数瞬间由1个变成了2个，其中子线程去执行run方法，主线程继续执行main方法的代码，两个线程各自独立运行互不影响。

​	c.当run方法执行完毕后子线程结束，当main方法执行完毕后主线程结束，但两个线程正.谁先执行没有明确的规定，取决于操作系统的调度算法。

注意:

​	线程创建和启动的方式一相对来说代码简单，但Java语言中只支持单继承，若该类继承Thread类后则无法继承其它类;而方式二相对来说代码复杂，但不影响该类继承其它类以及实现其它接口，因此以后开发中推荐方式二。	

#### 1.3 线程的编号和名称

（1）基本概念

​	线程指在程序执行过程中，能够执行程序代码的一个执行单位，每个程序至少都有一个线程，也就是程序本身。 Java中的线程有四种状态分别是：运行、就绪、 挂起 、结束。 一个程序中可以有多条执行线索同时执行，一个线程就是程序中的一条执行线索，每个线程上都关联有要执行的代码，即可以有多段程序代码同时运行，每个程序至少都有一个线程，即main方法执行的那个线程。

（2）常用方法

longgetld))					—用于获取调用对象所表乐线程的编号
String getName()			     —用于获取调用对象所表示线程的名称
void setName(Stringname)	   —用于设置线程的名称为参数指定的数值
static Thread currentThread()        —获取当前正在执行线程的引用

#### 1.4 Thread类

（1）基本概念

​	java.lang.Thread 类实现了Runnable接口，这意味着线程可以通过实现Runnable接口来定义其任务。

（2）常用方法

​	static voidsleep(times)	—当前线程让出处理器(离开Running状态)，使前线程进入Runnable状态等待
​	static void sleep （times）—使当前线程从 Running放弃处理器进入Block状态,休眠times毫秒,再返回到Runnable如果其他线程打断当前线程的Block(sleep),就会发生InterruptedException.

​	

​	

​	

