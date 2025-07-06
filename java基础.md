# 计算机的体系结构

## 	一、基本概念

​			计算机俗称“电脑”，是一种被广泛应用与各个领域的设备。

​			计算机主要是由：计算机硬件+计算机软件。

## 	二、常见的计算机硬件

​			**计算机中常见的硬件由：CPU、内存、硬盘、显卡、键盘、显示器、鼠标、.....**

​				**CPU：**

​					— 中央处理器，是计算机中最核心的部件，相当于人的大脑。

​					— 主要用于处理各种计算机的指令以及软件中的数据的哪个。

​				**内存：**

​					— 是计算机中存储部件。

​					— 主要用于临时存放CPU访问的数据内容，CPU直接访问且效率高。

​					— 容量小，一旦断电会造成数据的丢失。

​					— 时刻记得 ctrl+s 进行保存。

​				**硬盘：**

​					— 是计算机中的存储部件。

​					— CPU不能直接访问硬盘中的数据，因此效率比较低。

​					— 容量大，若断电不会造成数据的丢失。

​				其中键盘叫做标准输入设备，显示器叫做标准输出设备。

​			**科普：**

​				1Tb = 1024Gb

​				1Gb = 1024Mb

​				1Mb = 1024Kb

​				1Kb = 1024byte(字节)	通常一个英文字母占1个字节，一个汉字占用2个字节 

​				1byte = 8bit(二进制位)	在计算机的底层识别0和1组成的二进制序列

​			目前主流的硬件配置有：250G、320G、500G、1Tb，但如果您买了320G的硬盘显示却只有298G是因为硬件厂商是采用1000作为进率，而操作系统中是采用1024作为进率。因此会发生容量大小不一致的问题

# 计算机软件概念

## 	一、常见的计算机软件

​			计算中常见的软件主要分为两部分：系统软件和应用软件。

​			其中系统软件主要指操作系统，主流操作系统： <u>Windows/Unix/Linux/ios/Android</u>

​			其中应用软件主要指安装在操作系统之上的软件：<u>QQ、迅雷、火狐浏览器</u>....

## 	二、计算机软件的体系结构

​			使用者 => 应用软件 => 系统软件 => 硬件设备

​			其中系统软件分为：<u>内核(Kernel)和外壳(Shell)</u>

​			

# Java语言的概述(常识)

## 	一、Java语言的背景

​			Java语言诞生于1995年，该语言之父是詹姆斯-高斯林，之前隶属于sun公司，现在隶属于Oracle公司。

​			Java语言在编程语言排行榜占据重要的地位。

## 	二、Java发展历史

​			*1991年 Sun Green。

​			*1992年 James Gosling Oak。

​			*1995年 Java问世。

​			*1996年 Java1.0.

​			*1999年 Java1.2发布（<u>JAVA SE\JAVA EE\JAVA ME</u>）。

​			*... ... ...

​			*2004年 Tiger发布(JAVA5.0)，Java登录火星。

​			*2007年 Java6.0.

​			*2009年 Oracle以超过70亿美金的交易总值收购了Sun

​			*2011年 7月由Oracle正式发布Java7.0。

​			*2014年 3月19日，甲骨文公司发布Java8.0的正式版。

​			*2017年 9月21日，Java9.0正式发布。

​			*2018年 3月21日，Oracle官方宣布Java10正式发布。

​			*2018年9月25日，Oracle官方宣布Java11正式发布。

## 	三、Java语言的主要版本

​			（1）Java SE（Java Platform，Standard Edition）

​				— 称之为“Java平台标准版”，主要学习Java语言的语法规范和常见类。

​			（2）Java EE（Java Platform，Enterprise Edition）

​				— 称之为“Java平台企业版”，主要学习Java后台开发技术，编写B/S架构项目。

​			（3）Java ME（Java Platform，Micro Edition）

​				— 称之为Java平台微型版，随着Android平台的迅速普及已经走向淘汰。

## 	四、开发环境的搭建和使用（重点）

### 			1.jdk的下载和安装

​				（1）下载方式

​						方式一：通过官网下载：www.sun.com/www.oracle.com

​						方式二：通过搜索下载：www.baidu.com/www.sogou.com

​				（2）安装方式

​						若下载的是绿色版，则直接解压即可

​						若下载的是安装版，则直接一路点击下一步即可

​						切记jdk的安装路径中不要有中文！

### 			2.相关的概念（记住）

​				**jdk** - Java开发工具包，只要做Java开发就需要下载和安装该软件。

​				**jre** - Java运行时环境信息，只要运行Java程序就需要下载和安装该软件。

​				**jvm** - Java虚拟机，是Java程序与计算机操作系统之间的桥梁。

​				**javac.exe** - Java语言的编译器，主要用于将Java源代码进行编译生成字节码文件。

​				**java.exe** - Java语言的解释器，主要用于启动Java虚拟机对字节码文件进行解释执行

​			

## 	五、Java程序的编写流程

​		（1）新建文本文档，将文件名由xxx.txt修改为xxx.java；

​		（2）使用记事本的方式打开文件，编写Java代码后进行保存；

​		（3）启动dos窗口，切换到xxx.java文件所在路径中；

​		（4）使用javac xxx.java进行编译，生成xxx.class的字节码文件；

​		（5）使用java xxx进行解释执行，打印最终结果；

​		**注意：**当文件扩展名默认不显示时的处理方式

​			组织 => 文件夹和搜索选项 => 查看 => 隐藏已知文件类型的扩展名 => 去掉勾选 => 确定

​		当然目前不推荐这种写法，只作为一个基本流程讲解</u>

## 六、常用的快捷键

​		Ctrl+S 保存

​		Ctrl+C 复制

​		Ctrl+V 粘贴	

​		Ctrl+F 查找	

​		Ctrl+X 剪切	

​		Ctrl+Z 撤销	

​		Ctrl+A全选

​		Windows+D 回到桌面

​		Windows+R 打开运行，输入cmd后回车就可以启动dos窗口

​		Windows+Tab 切换任务

​		Alt+Tab 切换任务

​		Ctrl+Alt+Delete 启动任务管理器

​		Ctrl+Shift 切换输入法，若切换到中文后则使用Shift键进行中英文切换

## 七、环境变量的配置

#### 		（1）基本概念

​				通常情况下可执行文件只能在该文件所在的路径中访问，若希望该可执行文件可以在任意路径中使用则需要将该可执行文件的路径信息配置到环境变量Path中。

#### 		（2）实现方式

​				计算机 => 右键，选择属性 => 高级系统设置 => 高级 => 环境变量 => 系统变量 => 找到Path，点击编辑 => 将javac.exe<u>**所在的路径信息**</u>复制到Path变量值的最前面，加上英文版的分号 => 一路点击确定即可

​				切记Path变量值原来的内容不要改变，配置完毕后重新启动dos窗口！

### 八、跨平台原理（记住）

​		由于不同的操作系统中都提供了Java虚拟机进行翻译，因此同一份字节码文件可以在不同的操作系统中执行，从而赢得了“一次编译，到处运行”的美名。

​	

# 第一个Java程序

​	功能：打印一句话

​	作者：黄昱阳

​	版本：V1.0

​	所有者：好有经验

​	备注：请照顾好你的同桌噢！

```java
public class HelloWorld/*类名*/{
	public static void main/*main为主方法*/(String[] args){
		System.out.println("我就不");/*输出语句*/
	}
}
```

# 变量的基本概念与使用

## 	一、变量和注释(重点)

### 			1.基本概念

​						当需要在Java程序中纪律单个数据内容时，则声明一个变量即可，而声明变量的本质就是在内存空间中申请一块存储单元，由于该存					储单元的数值可以发生改变，因此得名为“变量”。

​						由于存放数据内容的大小不同导致所需存储单元的容量不同，在Java语言中使用的数据类型加以描述，为了便于下次访问还需要指定					变量的名称

## 	二、声明方式

​			（1）数据类型 变量 = 初始值；

​				如：

​					int age = 18;

​			（2）标识符（变量名）的命名规则（笔试题）

​					要求由字母、数字、下划线以及美元$组成，其中数字不能开头。

​				如：name、age、name2、age2

​			（3）不能使用Java中的关键字，所谓关键字就是Java中用于表示特殊含义的单词。

如：

|          |           |         |             |          |            |
| :------: | :-------: | :-----: | :---------: | :------: | :--------: |
| abstract |  boolean  |  break  |    byte     |   case   |   catch    |
|   char   |   class   |  const  |  continue   | default  |     do     |
|  double  |   else    | extends |    final    | finally  |   float    |
|   for    |   goto    |   if    | implements  |  import  | instanceof |
|   int    | interface |  long   |   native    |   new    |  package   |
| private  | protected | public  |   return    |  short   |   static   |
| strictfp |   super   | switch  | sychronized |   this   |   throw    |
|  throws  | transient |   try   |    void     | volatile |   while    |
|  assert  |   enum    |         |             |          |            |

如：

```java
public class VarTest {
    public static void main(String[] args){
        //声明一个初始值为10元素类型为int类型的变量
        int ia = 10;
        //打印变量的数值+字符串连接符，用于实现连接的功能
        System.out.println("ia="+ia);//ia = 10

		System.out.println("------------------");
        //变量在使用之前必须声明
        //System.out.println("sa="+sa);//错误：找不到该变量
        //String sa;
        //System.out.println("sa="+sa);//错误：可能尚未初始化变量sa
        String sa ="hello";
        System.out.println("sa="+sa);//sa = hello
        //变量不能重复声明
        //int ia =20;//错误：已在方法main(String[])中定义了变量ia
    }
}
```

​			总结：变量名必须先是标识符，标识符命名的一些规则：

​					必须是字母、数字、下划线、$等，其中数字不能开头。

​					不能是Java关键字，比如：public static class。

​					大小写敏感，长度没有限制，但不宜过长。

​					标识符尽量做到见名知意，可以是汉字，但不推荐使用。

​			标识符可以给类/变量/属性/方法/包，起名字

## 	三、Java的输入输出

示例：

```java
//导入java目录中util目录中的Scanner
import java.util.Scanner;
public class VarIO{
    public static void main(String[] args){
        //1.声明两个变量分别用于记录姓名和年龄
        String name;
        int age;
        
        //2.提示用户输入姓名和年龄并存到上述变量中
        System.out.println("请输入您的姓名和年龄：");
        //创建扫描器对象来扫描键盘的输入
        Scanner sc =new Scanner(System.in);
        name = sc.next();
        age = sc.nextInt();
        //3.打印变量的数值
        System.out.println("name="+name);
        System.out.println("age="+age);
        
    }
}
```

## 	四、Java的注释

​				注释用于解释代码，给程序员看但计算机会忽略注释，主要包括以下三种：

​					//单行注释，从//开始，到本行结束，都是注释。

​					/***/多行注释，从/*开始，到*/结束，中间所有都是注释。

​					/** */多行注释，从/**开始，到/结束，都是一种支持提取的注释。

​				注意：**多行注释不允许嵌套使用！**

# 数据类型与进制

## 	一、基本分类

​				在Java语言中将数据类型分为两大类：

​				（1）基本数据类型（记住）

​						byte、short、int、long、float、double、boolean、char

​				（2）引用数据类型（了解）

​						数组、类、接口、注解、枚举

## 	二、常用的进制

​				在日常生活中采用十进制进行数据的描述，权重：10^0、10^1、10^2、...

​				在计算机底层采用二进制进行数据的描述，权重：2^0、2^1、2^2、...

​				由于现实生活中的数据具有正负数，因此二进制中采用最高位(最左边)代表符号位，若是0则代表非负数，若是1则代表负数。

如：	

​						   10^3	   10^2	10^1	 10^0

​						      千               百              十              个

​			十进制整数：	1		2		3		4

## 	三、进制之间的转换（原理、尽量掌握）

### 		（1）正十进制转换为二进制的方式

​					a.除2取余法，使用十进制整数不断地除以2直到商为0时将余数逆序排序即可

​					b.拆分法，将十进制整数拆分为若干个二进制权重的和，若有该权重下面写1，否则写0

​			如：

​				45 = 32 + 8 + 4 + 1

​					128	64	32	16	8	4	2	1

​					   0	   0	  0	  0	 0	0	0	0	=>	0010 1101

### 		（2）正二进制转换为十进制的方式

​					a.加权法，使用二进制中的每个数字乘以当前位的权重再累加起来。

​						如：

​							0010 1101 = 0x2^7 + 0x2^6 + 0x2^5 + 0x2^4 + 0x2^3 + 0x2^2 + 0x2^1 + 0x2^0

​									    = 0 + 0 + 32 + 0 + 8 + 4 + 0 + 1

​									    = 45

### 		（3）负十进制转换为二进制的方式

​					a.先将十进制的绝对值转换为二进制，进行按位取反再加1。

​						如：

​							-45 => 绝对转换为二进制：0010 1101

​								=> 按位取反：	       1101 0010

​								=> 加1：			1101 0011

​						

​							-45 + 45 = 0

​								-45：1101 0011

​								 45：0010 1101

​							-------------------------------------

​									1 0000 0000（最高位溢出，丢弃） =>  0

### 		（4）负十进制转换为二进制的方式

​					a.先减1再按位取反，然后合并为十进制整数后添加负号。

​						如：

​							1101 0011 => 先减1：		1101 0010

​									    => 按位取反：	   0010 1101

​									    => 合并为十进制：    45 

​									    => 添加负号：	   -45   

## 	四、常见的进制

​				常见的进制有：二、八、十六进制和十进制。其中十六进制是用a到f代表10到15。八和十六进制其实都是二进制的简写。

​				正数的二进制转十进制只需要按照权重相加即可。

​				正数的十进制转二进制除2取余再反向输出。

​				负数的需要补码：按位取反，再加1。

# 分支结构的概念和使用

​	

## 	一、基本概念

​			在某些特殊场合中需要进行判断并作出选择时，就需要使用分支结构。

## 	二、if分支结构

​			（1）语法格式

​					if(条件表达式) {

​						语法快;

​					}

​			（2）执行流程

​					判断条件表达式是否成立

​						=> 若成立，则执行语句块;

​						=> 若不成立，则跳过语句块;

​		示例1：

```java
/*
	编程实现if分支结构的使用
*/

import java.util.Scanner;

public class IfTest {
    public static void main(String[] args) {
        // 1.提示用户输入年龄信息并使用变量记录
        System.out.println("请输入您的年龄：");
        Scanner sc = new Scanner(System.in);
        int age = sc.nextInt();
        
        // 2.使用if分支结构判断是否成年并给出对应的提示
        if(age >= 18) {
            System.out.println("开心地浏览器了网页...");
        }
        
        // 3.无论是否成年都打印一句话
        System.out.println("无奈地回家了！");
    }
}
```

​	示例2：

```java
/*
	编程使用if分支结构找到最大值并打印出来
*/

import java.util.Scanner;

public class IfMaxTest {
    public static void main(String[] args) {
        // 1.提示用户输入两个整数并使用变量记录
        System.out.println("请输入两个整数：");
   		Scanner sc = new Scanner(System.in);
        int ia = sc.nextInt();
        int ib = sc.nextInt();
        
        // 2.使用if分支结构找到最大值并打印出来
        if(ia >= ib) {
            System.out.println("最大值是:" +ia);
        }
        if(ia < ib) {
            System.out.println("最大值是:" +ib);
        }
        
        int max = ia;
        if(ib > max) {
            max = ib;
        }
        System.out.println("最大值是:"+max);
    }
}
```

## 	二、if-else分支结构

​			（1）语法格式

​				if(条件表达式) {

​					语句块;

​				}else{

​					语句块;

​				}	

​			（2）执行流程

​				判断条件表达式是否成立

​					=> 若成立，则执行语句块1;

​					=> 若不成立(否则)执行语句块2;

​	示例：

```java
/*
	编程实现if-else分支结构的使用
*/

import java.util.Scanner;
public class IfElesTest {
    public static void main(String[] args) {
        System.out.println("请输入您的考试成绩：");
   		Scanner sc = new Scanner(System.in);
        int score = sc.nextInt();
        
        // 2.使用if-else分支结构判断是否几个并给出对应的提示
        if(score >= 60) {
            System.out.println("恭喜你考试通过了！");
        } else {
            System.out.println("下学期来补考吧！");
        }
        
        // 3.打印一句经典语录
        System.out.println("世界上最遥远的距离不是生与死而是你在if我在else，看似相交却又永远分离！~");
    }
}
```

# Switch-case分支结构

## 	一、语法格式

​			switch(变量/表达式){

​				case 字面值1: 语句块1; break;

​				case 字面值2: 语句块2; break;	

​				...

​				default: 语句块n;

​			}

## 	二、执行流程

​			计算变量/表达式的数值 => 判断是否匹配字面值1 => 若匹配，则执行语句块1 => 执行break跳出当前结构 => 若不匹配，则判断是否匹配字面值2 => 若匹配，则执行语句块2 => 执行break跳出当前结构 => 若不匹配，则执行语句块n

​	示例：

​		

```java
/*
	编程使用switch-case分支结构来模拟菜单效果
*/
public class TestSwitchMenu{
    public static void main(String[] args) {
        //1.提示用户输入1~5之间的整数并使用变量记录
        System.out.println("请输入1~5之间的整数：");
        Scanner sc = new Scanner(System.in);
        int choose = sc.nextInt();
        
        //2.使用swithc-case分支结构根据不同的输入给出对应的提示
        switch(choose){
            case 1:System.out.println("显示所有用户"); break;
            case 2:System.out.println("添加新用户"); break;
            case 3:System.out.println("修改用户信息"); break;
        }
    }
}
```

# for循环的概念和使用

## 		一、基本概念

​				在某些特殊场合中需要重复执行一段代码，借助循环结构加以处理。

## 		二、for循环

​			（1）语法格式

​				for(初始化表达式; 条件表达式; 修改初始值表达式) {
​					循环体;

​				}

​			（2）执行流程

​				执行初始化表达式 => 判断条件表达式是否成立 => 若成立，则执行循环体 => 修改初始值表达式 => 判断条件表达式是否成立 => 若不成立，则循环结束

​	示例：

​			

```java
/*
	编程实现for循环的使用
*/
public class ForTest {
    public static void main(String[] args) throws Exception {
        for(int money = 500; money >= 10; money -= 100) {
            System.out.println("当前账户余额："+money+"，正在出钞，请稍后...")
            Thread.sleep(5000);//睡眠五秒的过程
        	System.out.println("请取走您的钞票！\n\n\n");
        }
        System.out.println("现在可以尽情地挥霍了...");
        	
    }
}
```

## 	三、break和continue关键字

​			break关键字用于循环中表示跳出当前循环;

​			continue关键字用于循环中表示结束本次循环继续下一次循环(会用);

​	示例：

​		

```java
/*
	编程实现break关键字和continue关键字的使用
*/
public class BreakContinueTest {
    public static void main(String[] args) {
        for(int i = 1; i <= 20; i++){
            if(0 == i%5) {
                continue; //结束本次循环继续下一次循环 奔向了i++
            }
            if(18 == i) {
                break; //跳出当前循环
            }
            System.out.println("i="+i); // 1 2 3 4 5 6 ... 17
        }
        // break执行后跳到这里了...
    }
}
```

## 	四、特殊的循环

​			for( ; ; ) - 这种没有循环条件的循环叫做无限循环，俗称”死循环“。

​			通常与break关键字搭配使用

​	示例：不断地提示用户输入聊天内容并输出，知道用户输入“bye”结束聊天。

​	

```java
/*
	编程使用for循环来模拟聊天的过程
*/

import java.util.Scanner;
public class ForChatTest {
    public static void main(String[] args) {
        // 1.提示用户输入聊天的内容并使用变量记录
        System.out.println("请输入要发送的内容：");
        Scanner sc = new Scanner(System.in);
        String msg = sc.next();
        
        // 2.判断用户输入的内容是否为“bye”，若是则聊天结束
        if("bye".equals(msg)) {
            System.out.println("聊天结束！");
            break;
        }
        // 3.若不是则打印用户输入的内容
        else{
            System.out.println("洪飞说：" +msg);
        }
        //跳到这里了
    }
}
```

## 	五、双重循环(难点)

​			（1）语法格式

​					for(初始化表达式1;  条件表达式2; 修改初始值表达式3) {

​						for(初始化表达式4; 条件表达式5; 修改初始值表达式6) {

​							循环体;

​						}

​					}

​			（2）执行流程

​					执行表达式1 => 判断表达式2是否成立 => 若成立，则执行表达式4 => 判断条件表达式5是否成立 => 若成立，则执行循环体 => 执行表达式6 => 判断表达式5是否成立 => 若不成立，则内层循环结束 => 执行表达式3 => 判断表达式2是否成立 => 若不成立，则外层循环结束

​	示例：实现双重for循环使用

​			（3）注意事项

​				a.外层循环变量动一下，则内层循环变量跑一圈;

​				b.当需要打印多行多列的数据内容时，可以使用双重for循环;

```java
/*
	编程实现双重for循环的使用
*/

public class ForForTest {
    public static void main(String[] args) {
        // 1.使用for循环打印5行字符串内容”厉害了我的哥“
        for(int i =1; i <=5; i++) {
            System.out.println("厉害了我的哥！");
        }
        System.out.println("---------------------------");
        // 2.使用for循环打印5列字符串内容“厉害了我的哥”
        for(int j = 1; j <= 5; j++) {
            // 打印完毕不换行
            System.out.print("厉害了我的哥！");
        }
        // 专门用于换行
        System.out.println();
        
        System.out.println("-------------------------------");
        // 3.使用for循环打印5行5列字符串内容“厉害了我的哥”
        for(int i = 1; i <= 5; i++) {
            for(int j = 1; j <=5; j++) {
                // 打印完毕不换行
                System.out.print("厉害我的哥！");
            }
            // 专门用于换行
            System.out.println();
        }
    }
}
```

## 	六、while循环(重点)

​			（1）语法格式

​				while(条件表达式) {

​					循环体;

​				}

​			（2）执行流程

​				判断条件表达式是否成立 => 若成立，则执行循环体 => 判断条件表达式是否成立 => 若不成立，则循环结束

​			（3）注意事项

​				a.while循环和for循环可以完全互换;

​				b.while(true)和for( ; ; )表示无限循环;

​				c.while循环主要用于明确循环条件但不明确循环次数的场合中;

​					for循环主要用于明确循环次数或范围的场合中;

​	示例：

```java
/*
	编程实现while循环的使用
*/
public class WhileTest {
    public static void main(String[] args) {
        // 1.使用for循环打印1~10之间的所有整数
        for(int i = 1; i <= 10; i++){
            System,out,println("i ="+i);
        }
        System.out.println("----------------------");
        // 2.使用while循环打印1~10之间的所有整数
        int i =1;
        while(i <= 10) {
            System,out,println("i ="+i);
            i++;
        }
    }
}
```

# 数组的基本概念与使用

## 	一、一维数组

#### 		1.基本概念

​				当需要在程序中记录单个数据内容时，则声明一个变量即可;

​				当需要在程序中记录多个类型相同的数据内容时，则声明一维数组即可，一维数组的本质就是在内存中申请一段连续的存储单元。

​				数组是相同数据类型的多个元素的容器，元素按线性顺序排列。

​				所有的线性顺序就是指除第一个元素外，每一个元素都有唯一的前驱元素；除最后一个元素外，每一个元素都有唯一的后继元素（“一个跟一个”）。

​				数组的操作其实就是对下标的控制，可以通过下标方式访问数组中的每个元素

#### 		2.声明方式

​			（1）语法格式

​				数据类型[] 数组名称 = new 数据类型[数组的长度];

​			如：

​				int[] arr = new int[5];	- 表示声明一个长度为5元素类型为int类型的一维数组

​				int num = 5;			- 表示声明一个初始值为5的变量

​				int arr[] = new int[5];	- 不推荐使用

​	示例：

```java
/*
	编程实现数组的声明和打印
*/
public class ArrayTest {
    public static void main(String[] args) {
        // 1.声明一个长度为3元素类型为int类型的一维数组
        int[] arr = new int[3];
        
        // 2.打印数组的长度以及每个元素的数值
        System.out.println("数组的长度是："+arr.length)；
        System.out.println("下标为0的元素是："+arr[0]);
        System.out.println("下标为1的元素是："+arr[1]);
        System.out.println("下标为2的元素是："+arr[2]);
        System.out.println("下标为3的元素是："+arr[3]);
    }
}
```

​			（2）元素的初始化

​				数据类型[] 数组名称 = {元素值1，元素值2，...};

​			如：

​				int[] arr = {10,20,30,40,50};

## 	二、二维数组(会用即可)

#### 		1.基本概念

​			一维数组本质上就是一段联系的存储单元，用于存放多个类型相同的数据内容;

​			二维数值本质上就是由多个一维数组组成(摞在一起)的数组，也就是说二维数组中的每个元素都是一个一维数组，而一维数组中的每个元素才是数据内容;

![1751438907144](D:\微信记录\WeChat Files\wxid_o6mrlo0bscgz22\FileStorage\Temp\1751438907144.png)

#### 		2.声明方式

​			（1）语法格式

​				数据类型[] [] 数组名称 = new 数据类型[行数]

​			如：

​				int[] [] brr = new int[2] [3]; -声明一个具有2行3列元素类型为int类型的二维数组

​				其中行下标的范围是：0~1;

​				其中列下标的范围是：0~2;

​	示例：

​	

```java
/*
	编程实现二维数组的声明和打印
*/
public class ArrayArrayTest {
    public static void main(String[] args) {
        // 1.声明一个具有2行3列元素类型为int类型的二维数组
        int[][] arr = new int[2][3];
        
        // 2.打印二维数组中所有元素的数值
        // 使用外层for循环用于控制打印的行数
       for(int i = 0; i < 2; i++) {
           // 使用内层for循环用于控制打印的列数
           for(int j =0; j<3; j++) {
           		System.out.print(arr[i][j] + " "); //0
        }
           System.out.print();
       }
        
    }
}
```

# 算数运算符的概念和使用

## 		一、运算符（重点）

​				表示加法运算符		- 表示减法运算符		* 表示乘法运算符		/ 表示除法运算符		% 表示取模/取余运算符

#### 			（1）在Java语言中两个整数相除时，结果只保留整数部分丢弃小数部分;

#### 			（2）若希望保留小数部分，则处理方式如下：

​						a.将其中任意一个操作数强转为double类型进行运算即可；

​						b.让其中任意一个操作数乘以1.0后进行运算即可（推荐）;

#### 			（3）0不能做除数，0.0可以做除数但结果是无穷

#### 			（4）+既可以作为算数运算符也可也作为字符串连接符，区分方式如下：

​					只要+两端的操作数中有一个是字符串类型，则按照字符串连接符对待，结果字符串

```java
/*
	编程实现算数运算符的使用
*/
public class ArithmeticTest {
    public static void main(String[] args) {
        //1.声明两个int类型的变量ia和ib，分别初始化为10和2
        //int ia = 10， ib = 2;
        int ia = 10;
        int ib = 2;
        //2.使用算术运算符进行计算
        //表示计算ia与ib的和赋值给变量ic，
        //其中ia+ib这个整体叫做表达式，ia和ib叫做操作数，+叫做操作/运算符
        int ic =ia + ib;
        System.out.println("ic = "+ic);//ic = 12
        System.out.println(ia + ib);//12
        System.out.println(ia - ib);//8
        System.out.println(ia * ib);//20
        System.out.println(ia / ib);//5
        System.out.println(ia | ib);//12
        System.out.println(ia % ib);//0
        
        System.out.println("---------------------------------------");
        //3.算数运算符的注意事项
       	ia = 5;
        System.out.println(ia / ib);//2
    }
}
```

#### 			（5）数字0作为除数的注意事项

​				加（+）、减（-）、乘（*）、除（/）、取余（%）

​				整数相除，只能取整数部分，小数部分被舍弃。

​				整数运算时，0不能做除数；浮点运算时，0.0可以，但结果是无穷的。

​				算数运算看起来简单，其实有难度。

​				int a =121;					int a =5;

​				int b =15;					System.out.println(a % 2);

​				int c = a / b;

​				结果是8，整数除法会取整			计算a除以2取余数，结果是1。

​		案例：

```java
/*
	编程使用算数运算符实现时间的转换和打印
*/
public class TimeArithmetic {
    public static void main(String[] args) {
        //1.提示用户输入整数类型的秒数并使用变量记录
        System.out.println("请输入一个整数类型的秒数：");
        Scanner sc =new Scanner(System.in);
        
        //2.将秒数转换为时分秒并使用变量单独记录
        //3666秒 => 1小时1分钟6秒钟
        //3666 / 3600 =1小时	3666 % 3600 = 66 / 60 = 1分钟
        //3666 % 60 = 6秒钟
        int hour = number / 3600;			//拆分小时数
        int minute = number % 3600 / 60;	//拆分分钟数
        int second = number % 60;			//拆分秒数
        
        //3.打印最终的转换结果
        System.out.println(number + "秒拆分为："+ hour + "时" + minute + "分" + second + "秒");
        System.out.println("--------------------------------------------");
        //4.+作为算数运算符和字符串连接符的区别
        System.out.println(""+hour+minute+second);//116
        System.out.println(hour+""+minute+second);//116
        System.out.println(hour+minute+""+second);//26
        System.out.println(hour+minute+second+"");//8
        System.out.println(hour+(minute+second)+"");//8
        System.out.println(hour+minute+(second+""));//26
    }
}
```

## 		二、关系/比较运算符

​			> 表示是否大于运算符			>= 表示是否大于等于运算符

​			< 表示是否小于运算符			<= 表示是否小于等于运算符

​			== 表示是否等于运算符		       != 表示是否不等于运算符

​			所有以关系运算符作为最终运算的表达式结果一定是boolean类型，只有true和false

​	示例：

```java
/*
	编程实现关系运算符的使用
*/
public class RelationTest {
    public static void main(String[] args) {
        int ia = 3;
        int ib = 2;
        System.out.println("ia="+ia);//ia=3
        System.out.println("ib="+ib);//ib=2
        
        System.out.println("-----------------------------");
        //使用关系运算符进行比较并打印结果
        System.out.println(ia>ib);	//true
        System.out.println(ia>=ib);	//true
        System.out.println(ia<ib);	//false
        System.out.println(ia<=ib);	//false
        System.out.println(ia!=ib);	//true
    }
}
```

​			注：Java关系运算符用于判断数据之间的大小关系。

​				>大于    <小于     >=大于等于    <=小于等于    ==等于    !=不等于

​				关系表达式的结果为boolean类型(true或false)

​					int a = 100;

​					boolean b1 = a >100;	false

​					boolean b2 = (a+1) >= 100;	true 

## 	三、自增减运算符

​			+ 表示加法运算符		++ 表示自增运算符，主要用于使得变量自身的数值加1

​			- 表示减法运算符		  --  表示自减运算符，主要用于使得变量自身的数值减1

​		注意：

​			（1）对于变量自身来说，++ia和ia++都实现变量自身数值的加1效果，是等价的;

​			（2）ia++表示先让ia的数值作为整个表达式的结果，然后再让ia自身的数值加1;

​				   ++ia表示先让ia自身的数值加1，然后再作为整个表达式

​			（3）自增（++）、自减（--）

​				  只能用于变量，常数不可以

​	示例：

```java
/*
	编程实现自增减运算符的使用
*/
public class MyselfTest {
    public static void main(String[] args)	{
        int ia = 10;
        System.out.println("ia = "+ia); //ia = 10
        
        //实现变量ia自身的数值加1的功能
        ++ia;
        System.out.println("ia =" +ia); //ia = 10
        
        System.out.println("-------------------------------------");
        // 接下来的代码要求尽量掌握
        // ia++这个整体叫做表达式，其中ia叫做操作数，其中++叫做操作符
        // 表达式和变量各自拥有独立的内存空间
        System.out.println(ia++);	//12
        System.out.println("ia =" +ia);//13
        System.out.println(++ia);	//14
        System.out.println("ia =" +ia);//14
    }
}
```

## 	四、逻辑运算符

​			&& 表示逻辑与运算符，相当于“并且”，同真为真，一假为假。

​			|| 表示逻辑或运算符，相当于“或者”，一真为真，同假为假

​			！表示逻辑非运算符，相当于“取反”，真为假，假为真。

​			逻辑运算符两端的操作数都是boolean类型的，结果应该是boolean类型的

```java
/*
	编程实现逻辑运算符的使用
*/
public class LogicTest {
	public static void main(String[] args) {
        boolean b1 = true;
        boolean b2 = false;
        System.out.println("b1 ="+b1);//b1 = true
        System.out.println("b2 ="+b2);//b1 = false
        
        System.out.println("------------------------------");
        
        //实现逻辑运算符的使用
        System.out.println(b1 && b2);	//并且 同真为真，一假为假
        System.out.println(b1 || b2);	//或者 一真为真，同假为假
        System.out.println(!b1);		//取反 真为假，假为真
        System.out.println(!b2);		//取反 真为假，假为真
    }
}
```

​	注：“&&”、“||”具备“短路”的特性：如果通过第一个表达式的值即可得出最后的结果，则不计算第二个表达式。

## 	五、条件/三目运算符

​			条件运算符又称“三目”运算符，其结构为：

​				条件表达式 ? 表达式1 : 表达式2

​				=> 判断条件表达式是否成立

​					=> 若成立，则执行表达式1;

​			先计算boolean表达式的值，如果为true，则整个表达式的值为表达式1的值；

​			如果为false，则整个表达式的值为表达式2的值。

​		示例：

```java
/*
	编程使用关系运算符进行判断并打印
*/
import java.util.Scanner;
public class RelationJudgeTest {
    public static void main(String[] args) {
        //1.提示用户输入一个整数并使用变量记录
        System.out.println("请输入一个整数：");
        Scanner sc = new Scanner(System.in);
        int number = sc.nextInt();
        
        //2.使用关系运算符进行判断并打印
        //大于等于100 并且 小于等于999
        //System.out.println(100 <= number <= 999); error
        System.out.println(100 <= number && number <= 999);
        System.out.println((100 <= number && number <= 999)? "是三位数":"不是三位数");
    }
}
```

## 	六、赋值运算符

#### 		（1）简单赋值

​				= 表示复制运算符，主要用于将=右边的数据赋值给=左边的变量，覆盖原来的数值。

​			如：

​				ia = 2; - 表示使用数据2给变量ia赋值，覆盖该变量ia原来的数值

​			笔试题：

​				ia == 2; - 判断ia的数值是否等于2

​				2 == ia; - 判断2是否等于ia的数值，结果与上述方式等价，但推荐该方法

​				ia == 2; - 将数据2赋值给变量ia，覆盖原来的数值

​				2 = ia; - 编译报错

#### 		（2）复合赋值

​				+=、-=、*=、.....

​			如：

​				int ia = 2;

​				ia = ia + 3;	从结果上等价于:	ia+=3;

## 	七、运算符的优先级

#### 		a.()的优先级极高;

#### 		b.= 的优先级极低;

#### 		c.若实在不确定运算符的优先级，则可以借助()加以确定;

## 	八、移位运算符

​			<< 表示左移运算符，用于将数据的二进制位向左移动，右边使用0补充

​			>> 表示右移运算符，用于将数据的二进制位向右移动，左边使用符号位补充

​			>>> 表示逻辑右移运算符，用于将数据的二进制位向右移动，左边使用0补充

​	示例：

```java
/*
	编程实现移位运算符的使用
*/
public class TestMove{
    public static void main(String[] args){
        byte bl = 10;
        System.out.println("bl = "+bl); //bl = 10
        //表示将b1的数值的二进制向左移动2位，右边使用0补充
        //10: 0000 1010 => 0010 1000 =>
        System.out.println(b1 << 2);	//40
        //10: 0000 1010 => 0000 0010
        System.out.println(b1 >> 2);	//2
        System.out.println(b1 >>> 2);	//2
    }
}
```

## 	九、位运算符

​			& 表示按位与运算符，就是按照二进制位进行与运算，同1为1，一0为0（1-真 0-假）

​			| 表示按位或运算符，就是按照二进制位进行或运算，一1为1，同0为0。

​			~ 表示按位取反运算符，按照二进制位进行取反，1为0，0为1。

​			^ 表示按位异或运算符，按照二进制位进行异或运算，相同为0，不同为1。

​	示例：

```java
/*
	编程实现位运算的使用
*/
public class TestBit{
    public static void main(String[] args){
        byte b1 = 11;
        byte b2 = 13;
        System.out.println("b1="+b1);	//b1 = 11
        System.out.println("b2="+b2);	//b2 = 13
        
        System.out.println("----------------------------");
        //11:0000 1011
        //13:0000 1101
        System.out.println(b1 & b2); //0000 1001 => 9
        System.out.println(b1 | b2); //0000 1111 => 15
        System.out.println(b1 ^ b2); //0000 0110 => 6
        //0000 1011 => 1111 0100 => 1111 0011 => 0000 1100 => 12 => -12
        System.out.println(~b1);
    }
}
```

# 面向对象编程的概念

## 	一、什么是对象

​			万物皆对象

## 	二、什么是面向对象

​			面向对象就是指以特征（属性）和行为的观点去分析现实世界中事物的方式。

## 	三、什么是面向对象编程

​			面向对象编程就是指先使用给面向对象的方式进行分析，再使用任意一门面向对象的编程语言进行翻译的过程。

​			其中C语言是一门面向过程的编程语言。

​			其中C++语言是一门既面向过程又面向对象的编程语言。

​			其中Java语言是一门纯面向对象的编程语言。

## 	四、如何学好面向对象编程？

​			深刻理解面向对象编程的三大特征：封装、继承、多态。

## 	五、类、对象以及引用（抽象、难点、重中之重）

#### 		1.对象和类的概念

​				对象是客观存在的实体，在Java语言体现为内存空间的一块区域。

​				类就是分类的概念，是对具有相同特征和行为的多个对象共性的抽象描述，在Java语言中包含描述特征的成员变量和描述行为的成员方法，是创建对象的模板。

#### 		2.类的定义

​			（1）类定义的语法格式

​				class 类名 {

​					类体;

​				}

​			如：

​				class Person {

​				}

​			注意：

​				当类名由多个单词组成时，要求每个单词的首字母都要大写;

​			（2）变量变量定义的语法格式

​				class 类名{

​					数据类型 成员变量名 = 初始值;	- 其中=初始值通常省略，但分号不能省略

​				}

​			如：

​				class Person{

​					String name;

​					int age;

​				}

​			注意：

​				当成员变量名由多个单词组成时，要求从第二个单词起每个单词首字母大写;

​			扩展：

​				局部变量 - 主要指在方法体中声明的变量，作用范围从声明开始到方法结束

​				成员变量 - 主要指在方法体外类体内声明的变量，作用范围从声明到类体结束

#### 		3.对象的创建

​			（1）语法格式

​				new 类名();

​			如:

​				new Person(); - 创建Person类型的对象，由于该对象没有名字因此叫做"匿名对象"

​			（2）注意事项

​				a.当一个类定义完毕后，使用new关键字创建/构造对象的过程叫做 类的实例化;

​				b.创建对象的本质就是在内存中的堆区申请存储空间，来存放该对象独有的特征信息

#### 		4.引用

​			（1）基本概念

​				在Java语言中使用引用数据类型声明的变量叫做引用型变量，简称为“引用”。

​				引用变量主要用于记录对象在堆区中的内存地址信息，便于下次访问。

​			（2）语法格式

​				类名 引用变量名；

​			如：

​				Person p; - 表示声明Person类型的引用变量p，本质上在栈区申请存储空间

​				Person p = new Person(); - 表示声明引用变量p来记录Person类型对象的地址信息

​				引用变量名.成员变量名;

​			如：

​				p.name = "zhangsan"; - 表示使用引用变量p访问所指向的堆区对象的姓名特征

​	示例：

​	

```java
/*
	编程实现Person类的定义和使用
*/
public class Person {
    String name;	//用于描述姓名的成员变量
    int age;		//用于描述年龄的成员变量
    
    public static void main(String[] args) {
        // 声明Person类型的引用创建Person类型的对象
        Person p = new Person();
        // 打印该对象的成员变量信息 null 0
        System.out.println("我是"+p.name+"，今年"+p.age+"岁了！");
        
        System.out.println("-----------------------------");
        // 修改成员变量的数值
        p.name = "zhangfei";
        p.age = 30;
        // 打印该对象的成员变量信息 null 0
        System.out.println("我是"+p.name+"，今年"+p.age+"岁了！");
    } 
}
```

## 	六、成员方法（重中之重）

#### 		1.语法格式

​				class 类名 {

​					返回值类型 成员方法名(形参列表) {

​						成员方法体;

​					}

​				}

​		如：

​			class Person {

​				void show() {
​					System.out.println("没事出来秀一下！");

​				}

​			}

​		注意：

​			当成员变量名由多个单词组成时，通常要求从第二个单词起每个单词首字母大写

#### 		2.格式的详解

​			（1）返回值类型

​					返回值主要指从方法体内向方法体外返回的数据内容;

​					返回值类型主要指返回值的数据类型，可以是基本数据类型，也可以是引用数据类型。

​				如：

​					当返回的数据内容是66时，则返回值类型些int即可;

​					当返回的数据内容是3.14时，则返回值类型些double即可;

​					当返回的数据内容是"hello"时，则返回值类型些String即可;

​				在方法体中使用return关键字来返回数据内容并结束当前方法。

​				如：

​					放返回的数据内容是66时，则方法体中写：return 66;

​					当返回的数据内容是num时，则方法体中写：return num;	

​				在方法体中使用return关键字来返回数据内容并结束当前方法。

​			（2）形参列表

​					形式参数主要用于将方法体外的数据传入方法体的内部，格式：数据类型 形参名。

​					形参列表主要指多个形式参数组成的整体，格式如下：

​						数据类型 形参名1，数据类型 形参名2，...

​				如：

​					当传入的数据内容是66时，则形参列表写为：int i即可;

​					当传入的数据内容是3.14时，则形参列表写为：double d 即可;

​					当传入的数据内容是“hello”时，则形参列表写为：String s 即可;

​					当传入的数据内容是66和"hello"时，则形参列表写为：int i,String s 即可;

​				若该方法不需要传入任何数据内容是，则形参列表位置啥也不写 即可;

​			（3）成员方法体

​					成员方法体主要编写描述该方法功能的语句。

​				如：

​					当该方法的功能就是打印时，则方法体中写System.out.println("..."); 即可

​					当该方法的功能就是返回66时，则方法体中写 return 66; 即可

​		示例：

```java
/*
	编程实现Person类的定义和使用
*/
public class Person {
    String name;// 用于描述姓名的成员变量
    int age;// 用户描述年龄的成员变量
    
    //自定义成员方法打印所有特征的数值
    //返回值类型 成员方法名(形参列表) {
    	//成员方法体;
	//}
    void show() {
        System.out.println("我是"+p.name+"，今年"+p.age+"岁了!");
    }
    
    public static void main(String[] args) {
        // 声明Person类型的引用指向 创建Person类型的对象
        Person p = new Person();
        // 打印该对象的成员变量信息 null 0
        System.out.println("我是"+p.name+"，今年"+p.age+"岁了!");
        System.out.println("---------------------------------------");
        // 修改成员变量的数值
        p.name = "zhangfei";
    }
}
```

## 	六、方法的调用

#### 		（1）语法格式

​				引用变量名.成员方法名(实参列表);

​			如：

​				p.show();	- 表示使用引用变量p调用show方法

#### 		（2）注意事项

​				a.实际参数列表主要用于对形式参数列表进行初始化操作，因此参数的个数、类型、顺序等都必须与形参列表保持一致;

​				b.实参可以传递直接量、变量、表达式以及方法的调用等;

![image-20250703204421404](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250703204421404.png)

# 构造方法和方法重载

## 	一、构造方法（重中之重）

​			如：

​				Person p =new Person();	- 声明Person类型的引用指向Person类型的对象

​				p.show();				    - 使用引用变量p调用show方法

​		（1）语法格式

​				class 类名 {

​					类名(形参列表){

​						构造方法体;

​					}

​				}

​			如：

​				class Person {

​					Person() {

​					}

​				}

​		（2）注意事项

​				a.构造方法的名称与类名完全相同，美誉返回值类型连void都不许有

​				b.当使用new关键字构造对象时会自动调用构造方法进行成员变量的初始化工作。

​		（3）默认构造方法

​				a.当一个类中没有自定义任何形式的构造方法时，编译器会自动添加一个无参的空构造方法，叫做默认/缺省构造方法，如:Person(){}

​				b.若类中出现自定义构造方法，则编译器不再提供任何形式的构造方法。

![image-20250703205206567](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250703205206567.png)

## 	二、方法的重载(Overload)

​			（1）基本概念

​				在Java语言中若方法的名称相同但参数列表不同，这样的方法之间构成重载关系

​			（2）体现形式

​				方法重载的主要形式有：参数的个数不同、参数的类型不同、参数的顺序不同，与形参变量名和返回值类型无关，但建议返回值类型最好相同。

​				判断方法是否重载的核心：调用能否区分。

​		示例：

```java
/*
	编程实现重载体现形式的测试
*/
public class OverloadTest {
    void show() {
        System.out.println("show()");
    }
    void show(int i) {
        System.out.println("show()");
    }
    public static void main(String[] args) {
        //声明本类类型的引用 指向本类的对象
        OverloadTest ot = new OverloadTest();
        //调用成员方法
        ot.show();
        ot.show(66);
        ot.show(66, 3.14);
        ot.show(66, 118);
    }
}
```

​			（3）实际意义

​				对于调用者来说只需要记住一个方法名就可以调用各种不同的版本实现不同的效果。

​			如：

​				char c = 'a';

​				System.out.println(c);

​				int i = 10;

​				System.out.println(i);

​				double d = 3.14;

​				System.out.println(d);

​				...

![image-20250703210038997](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250703210038997.png)

# this关键字（原理、理解）

​	一、基本概念

​			在构造方法中this关键字代表当前正在构造的对象。

​			在成员方法中this关键字代表当前正在调用的对象。



​		原理分析：

​			当成员方法中给访问成员变量时默认会加上this.（相当于汉语中”我的“），当不同的引用调用同一个成员方法时会导致成员方法中的this不同，那么this.访问的结果随之不同。

​	二、使用方式

​		（1）当形参变量和成员变量同名时，在构造方法或成员方法中通常优先使用形参变量，若希望使用成员变量就需要在变量名的前面加上this.进行说明（重中之重）。

​		（2）在构造放啊的第一行使用this(实参)的方法可以调用本类中的其他构造方法(了解)

![image-20250704092905382](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20250704092905382.png)

​	三、方法的传参和递归调用

​		（1）main方法是程序的入口，为main方法中局部变量开辟内存空间并初始化;

​		（2）调用max方法时为max方法的形参变量开辟内存空间;

​		（3）使用实参变量给形参变量进行赋值操作，执行max方法的方法体;

​		（4）当max方法结束后释放形参变量的内存空间;

​		（5）main方法中的res得到max方法的返回值然后继续向下执行;

​		（6）当main方法结束后释放局部变量的内存空间;

​	示例：

```java
/*
	编程实现参数传递过程的测试
*/
public class ArgumentTest {
    void show(int i) {
        i = 200;
        System.out.println("i ="+i); //200
    }
    void show(int[] brr) {
        brr[0] = 200;
        System.out.println("brr[0]"+brr[0]); //200
    }
    public static void main(String[] args) {
        ArgumentTest at = new ArgumentTest();
        int num = 10;
        at.show(num);
        System.out.println("num ="+num); //10
        
        System.out.println("------------------------");
        int[] arr =new int[]{10,20};
        at.show(arr);
        System.out.println("arr[0] =" +arr[0]);//200
    }
}
```

​		掌握内容：

​			a.当基础数据类型的变量作为方法的参数传递时，形参变量的改变不会影响到实参;

​			b.当引用数据类型的变量作为方法的参数传递时，形参变量指向的内容发生改变后会影响到实参变量指向的内容;

​			c.当引用数据类型的变量作为方法的参数传递时，形参变量改变指向后再改变指向的内容时不会影响到实参变量指向的内容;

​	四、递归调用

​		（1）基本概念

​			在一个方法体的内部调用当前方法自身的形式，叫做递归。

​		如：

​			void show(){

​				show();			

​			}

# 封装的基本概念与实现

## 	一、封装

​			1.基本概念

​				通常情况下测试类可以对封装类中的成员变量进行赋值，若赋值的数据合法但不合理时，无论时编译阶段还是运行阶段都不会报错或者给出提示，此时与现实生活不符。

​				为了避免上述错误的发生，就需要对成员变量进行密封包装处理，该机制就叫做封装，换句话说，封装就是一种保证成员变量值合理性的机制。

​	示例：

​			2.实现流程

​			（1）私有化成员变量，使用private关键字修饰;

​			（2）提供公有的get和set方法，在方法体中进行合理值的判断;

​			（3）在构造方法中调用set方法进行合理值的判断

```java
/*
	编程实现Car类的定义
*/
public class Car {
    //1.私有化成员变量，使用private关键字修饰
    // private修饰成员变量表示私有的含义，该成员变量只能在
	private String brand;// 用于描述品牌的成员变量
    private String color;// 用于描述颜色的成员变量
    private int price;// 用于描述价格的成员变量
    
    //无参构造
    Car() {
    }
    // 三个参数的构造
    Car(String brand, String color, int price) {
        //this.brand = brand;
        //this.color = color;
        //this.price = price;
        setBrand(brand);
        setColor(color);
        setPrice(price);
    }
    
    //打印所有特征的行为
    void show(){
        System.out.println("品牌："+brand+"，颜色："+color+"价格："+price);
    }
    // 2.提供公有的get和set方法，在方法体中进行合理值的判断;
    // public修饰成员方法表示公有的，该方法可以在任意位置调用
    // 若方法的在前面啥也不加表示默认权限，访问级别低于public，具体以后再讲
    // 获取品牌并返回的行为
    public String getBrand() {
        return brand;
    }
    // 获取颜色并返回的行为
    public String getColor() {
        return color;
    }
    // 获取价格并返回的行为
    public int getPrice() {
        return price;
    }
    // 设置品牌为参数指定的数值
    public void setBrand(String brand) {
        this.brand = brand;
    }
    // 设置颜色为参数指定的数值
    public void setColor(String color) {
        this.color = color;
    }
    // 设置价格为参数指定的数值
    public void setPrice(int price) {
        if(price >= 0) {
            this.price = price;
        } else {
            System.out.println("价格不合理！！！");
        }
    }
    // 实现价格增长1000元的行为
   	public void grow() {
        price += 1000;
    }
    // 实现价格增长参数指定数值的行为
    public void grow(int price) {
        this.price += price;
    }
}
```

​	

# static关键字

## 	一、基本概念

​			通常情况下成员变量隶属于对象层级，每创建一个对象就需要申请独立的内存空间来存放该对象独立的成员变量信息，若所有对象的某个成员变量数值完全一样却又单独存放会造成内存空间的浪费。

​			为了解决上述问题，则使用static关键字修饰成员变量，此时该成员变量由对象层级提升为类层级被所有对象共享，该成员变量随着类的加载准备就绪，与是否创建对象无关

​			static关键字也可以修饰成员方法，推荐使用 类名. 的方式访问。

​	示例：

```java
/*
	编程实现static关键字的使用
*/
public class StaticTest {
    private int cnt = 1; //隶属于对象层级，每个对象都拥有一份
    private static int snt = 2; //隶属于类层级，所有对象共享同一份
    
    // 下面的方法没有static修饰，隶属于对象层级
    public void show() {
		System.out.println("cnt ="+cnt); //cnt = 1	
        System.out.println("snt ="+snt); //snt = 2	
    }
    
    public static void main(String[] args) {
        StaticTest st = new StaticTest();
        st.show();
    }
}
```

## 	一、基本概念

​			（1）在非静态的成员方法中既能访问非静态的成员也能访问静态的成员;

​				（成员：成员变量 + 成员方法，静态成员被所有对象共享）

​			（2）在静态的成员方法中只能访问静态的成员不能访问非静态的成员;

​				（成员：成员变量+成员方法，调用静态方法时可能还没创建对象）

​			（3）只能隶属于类层级被所有对象共享的内容才可以使用static修饰;

​				（不能滥用static关键字）

# 单例设计模式

​	一、基本概念

​		在某些特殊场合中一个类对外提供且只提供一个对象，这样的类叫做单例类。

​		而设计单例类的思想和模式叫做单例设计模式，主要用于固定的场合。

​	二、实现流程

​		a.私有化构造方法，使用private关键字修饰;

​		b.声明本类类型的引用指向本类类型的对象，使用private static共同修饰;

​		c.提供公有的get方法负责奖成员变量的数值返回出去，使用static关键字修饰;

​	三、实现方式

​		单例设计模式的实现方式有两种：饿汉式和懒汉式，在以后的开发中推荐饿汉式

​	示例：

```java
/*
	编程实现Singleton类的封装
*/
public class Singleton {
    //2.提供本类类型的引用指向本类类型的对象
    //Person p =new Person();
    private static Singleton sin = new Singleton(); //饿汉式
    private static Singleton sin = null;//懒汉式
    
    //1.私有化构造方法，使用private关键字修饰
    //private修饰构造方法表示该方法只能在本类的内部使用
    private Singleton(){}
    
    //3.提供公有的get方法负责将成员变量返回出去
    public static Singleton getInstance() {
        //return sin;
        if(null == sin) {
            sin = new Singleton();
        }
        return sin;
    }
}
```

# 继承

​		人类：

​			特征：姓名、年龄

​			行为：吃饭、娱乐

​		学生类 吸收 人类：

​			特征：学号

​			行为：学习

​		教师类 吸收 人类：

​			特征：工号

​			行为：讲课

​		工人类 吸收 人类：

​			特征：薪水

​			行为：工作

​		....

## 		一、基本概念

​				当多个类之间有相同的特征和行为时，可以将相同的内容提取出来组成一个公共类，让多个类吸收公共类中已有特征和行为而在多个类的内部编写自己独有特征和行为的方式，叫做继承。

​				使用继承可以提高代码的复用性和扩展以及可维护性。

​				在Java语言中使用extends(扩展)关键字来表达继承关系。

​			如：

​				public class Student extends Person {}	- 表示Student类继承自Person类

​					其中Person类叫做基类、父类、超类

​					其中Student类叫做派生类、子类、孩子类

## 	二、注意事项

​				（1）子类可以继承父类的成员变量和成员方法，其中私有成员变量可以继承但不可以直接使用，子类不可以继承父类的构造方法和私有方法。

​				（2）无论使用何种方式构造子类对象时，都会自动调用父类中的无参构造方法来初始化从父类中继承下来的成员变量，相当于在子类构造方法第一行增加代码：super()的效果

![QQ_1751618546149](C:\Users\Administrator\AppData\Local\Temp\QQ_1751618546149.png)

​	示例：

```java
/*
	编程实现Person类的封装
*/
public class Person {
	//1.私有化成员变量，使用private关键字修饰
    private String name;
    private int age;
    
    //3.在构造方法中调用set方法进行合理值的判断
    public Person() {
        
    }
    public Person(String name, int age) {
        setName(name);
        setAge(age);
    }
    
    //2.提供公有的get和set方法，在方法体中进行合理值的判断	
    public String getName(){
        return name;
    }
}
```

​				（3）使用继承必须满足 子类 is a 父类的逻辑关系，也就是不能滥用继承。

​				（4）Java语言中只支持单继承不支持多继承，也就是一个子类只能有一个父类，但yige父类可以有多个子类。

## 	三、方法的重写(override)

​			（1）基本概念

​					若从父类中继承下来的方法不满足于子类的需求时，就需要在子类中重新写一个与父类中一样的方法来覆盖从父类中继承的版本，这种方式就叫做重写。

​			（2）方法重写的原则：

​					1.相同的方法名称，相同的参数列表，相同的返回值类型或者返回子类。

​					2.访问权限不能变小，可以变大。

​					3.不能抛出更大的异常。

​				在子类重写的方法中，可以通过super关键字调用父类的“原始”方法。

​				static的方法重写以后还是static的。

## 	四、访问控制

​				常见的访问控制符

​					访问控制符	访问权限	本类	本包中的类	子类	其他包中的其他类

------------------------------------------------------------------------------------------------------------------------------

​					     public	      公有的	    ok	         ok                 ok		     ok

​					  protected	   保护的	    ok		ok	 	 ok		     no

​				a.public修饰的内容可以在任意位置使用;

​				b.private修饰的内容只能在本类中使用;

​				c.通常情况下，成员变量都使用private修饰，成员方法都使用public修饰;

## 	五、包的定义

​			package 包名;

​			package 包名1.包名2...包名m;	- 便于管理，避免命名冲突的问题

# final关键字

​	一、基本概念

​		final本意为“最终的，不可更改的”，该关键字可以修饰类、成员方法、成员变量等。

​	二、使用方式

​		final关键字修饰类表示该类不能被继承。

​			- 为了防止滥用继承带来的为好

​			- 如：java.lang.String类等

​		final关键字修饰成员方法表示该方法不能被重写但可以被继承。

​			- 为了防止不经意间造成的方法重写

​			- 如：java.text.DateFormat类中的format方法等

# 多态的基本概念和语法格式

## 	一、基本概念

​				多态主要指同一种事务表现出来的多种形态。

​				饮料：可乐、雪碧、脉动、乐虎、红牛、...

​				宠物：狗、猫、鸟、乌龟、鱼、...

​				人：学生、教师、工人、...

## 	二、语法格式

​				父类类型 引用变量名 = new 子类类型();

​			如：

​				Person pw =new Worker();

​				pw.show();

## 	三、多态的特点

​				Person p = new Student(); p究竟是当父亲用，还是子类用呢？

​				其实是被当成父类的对象使用。

​					1.只能使用父类中定义的属性和方法

​					2.不能直接使用子类中扩展的属性和方法。

​					3.如果子类重写了方法，静态方法调父类的，非静态方法调子类的。

​				原因：

​					编译时，p被任务是Person类型; 但在运行时是Student类型。在内存中其实是子类对象。

​				多态时能不能把扩展的属性和方法调出来？

​					能，但需要做类型转换，Person类型的变量无法调用Student扩展的成员。

​					引用类型的类型转换：

​						必须发生在父子类之间。

​						父类转子类需要做强制类型转换（向下造型），子类转父类可以自动完成（向上造型）。

​					所谓的强制类型转换，Student s = (Student)p;不是把p的类型转换了，是定义了一个新的变量s，s的类型是Stundent，p还是Person。

​					对象强制类型转换是一种还原行为，必须内存中是该类型的对象才能成功。	

## 	四、多态的效果

​			（1）当父类的引用指向子类的对象时，父类的引用可以直接调用父类独有的方法;

​			 （2）当父类的引用指向子类的对象时，父类的引用不可以直接调用子类独有的方法;

​			（3）对于父子类都有的非静态成员方法来说，编译阶段调用父类版本，运行阶段调用子类重写以后的版本;

​			 （4）对于父子类都有的静态方法来说，编译和运行阶段调用父类版本，隶属于类层级，因此与指向的对象无关;

## 	五、引用数据类型之间的转换

​			（1）引用数据类型之间的转换分为：自动类型转换	和	强制类型转换。

​				  其中自动类型转换主要指从小范围到大范围之间的转换，也就是子类到父类的转换

​				  其中强制类型转换主要指从大范围到小范围之间的转换，也就是父类到子类的转换

​			（2）引用数据类型之间的转换必须发生在父子类之间，否则编译报错

​			（3）若转换到的目标类型是子类类型但不是该引用真正指向的子类类型，则编译通过，运行阶段发生类型转换异常

​			（4）为了避免上述错误的发生，可以使用instanceof进行判断，具体格式如下：

​				if(引用变量名 instanceof 数据类型)  -  判断引用变量指向的对象是否为后面类型

​				instanceof就是判断对象的类型，如果是该类型返回true，不是返回false。

​				语法格式：对象 instanceof 类型

​				obj instanceof Object 或 p instanceof Person

​				严格来说，对象进行强制类型转换之前，都应该instanceof一下。

​				instanceof判断支持本类和父类类型。

## 	六、多态的意义

​				多态的实际意义在于可以屏蔽不同子类的差异性实现通用的编程，但可以调用不同的方法带来不同的结果。

​				

# 抽象类

## 	一、抽象方法的概念

​				抽象方法就是指不能具体实习的方法，也就是没有方法体并使用abstract关键字修饰

​				语法格式：

​					访问控制符 abstract 返回值类型 方法名称(形参列表);

​				如：

​					public abstract void cry();

## 	二、抽象类的概念

​				抽象类就是指不能具体实例化的类，也就是不能创建对象并使用abstract关键字修饰

## 	三、注意事项

​			（1）抽象类中可以用成员变量、构造方法以及成员方法;

​			（2）抽象类中可以有抽象方法也可也没有抽象方法;

​			（3）拥有抽象方法的类必须是抽象累，因此严格来说，具有抽象方法把那个且使用abstract关键字修饰的类才算真正意义上的抽象类。

# java语言中的常用类与包	

​				java.lang包 - 该包是Java语言中的核心包，该包中的内容由Java虚拟机自动导入

​						    - 如：String类、System类等

​				java.util包   -  该包是Java语言中的工具包，里面包含了大量的工具类和集合类等

​						     - 如：Scanner类、Random类等

​				java.io包      - 该包是Java语言中输入输出包，里面包含了大量读写文件的类等

​						      - 如：FileOutputStream类、FileInputStream类等

​				java.net包    - 该包是Java语言中的网络包，里面包含了大量网络编程的类等

​						      - 如：ServerSocket类、Socket类等

​				java.sql包     - 该包是Java语言中操作数据库的数据库包，里面包含了数据库的所有类和接口

​				Java程序员在编程，可以使用大量的类库，因此，Java编程需要记很多，对编程能力的本身要求不是特别的高。

## 	一、Object类

#### 			1.基本概念

​					java.lang.Object类是所有类层次结构的根类，任何类都是该类的直接或间接子类。

#### 			2.常用的方法

​					Object() - 使用无参方式构造对象。

​					boolean equals(Object obj) - 用于判断调用对象是否与参数对象相等。	

​						- 该方法默认比较两个对象的地址，与 == 运算符结果相同。

​						- 为了使得该方法比较两个对象的内容，则需要重写该方法。

​						- 若该方法重写后，则应该重写hashCode方法来维护hashCode方法的常规协定

​					int hashCode() - 用于获取调用对象的哈希码值(内存地址的编号)

​						- 若调用equals方法的结果相等，则各自调用hashCode方法的结果相同。

​						- 若调用equals方法的结果不相等，则各自调用hashCode方法的结果不相同。

​						- 为了维护上述的常规协定与equals方法结果保持一致，就需要重写该方法。

​					String toString() - 用于获取对象的字符串形式。

​						- 该方法默认返回的字符串为：包名.类名@哈希码值的十六进制形式。

​						- 为了返回更有意义的数据内容则需要重写该方法。

​						- 当字符串内容与引用进行连接时，自动调用toString方法。

​						- 当使用print或println方法打印引用时，会自动调用toString方法。

## 		二、包装类和数学处理类

​						如：

​							Person p = new Person();	- 声明Person类的引用指向Person类型的对象

​							int num = 10;			     - 声明一个int类型的变量num初始值为10

​							Java语言是一门纯面向对象的编程语言

#### 					1.包装类的概念

​								由于Java语言是一门纯面向对象编程语言，而8种基本数据类型声明的变量并不是对象，为了满足Java语言的特性就需要对这些变量进行对象化处理，而实现该功能的相关类就叫做包装类。

#### 					2.包装类的分类

​								int => java.lang.Integer类

​								char => java.lang.Character类

​								long => java.lang.Long类

​								double =>  java.lang.Double类

​								boolean =>  java.lang.Boolean类

​								byte =>  java.lang.Byte类

​								float =>  java.lang.Float类

​								short =>  java.lang.Short类

​							**Integer类**

​							（1）基本概念
​								java.lang.Integer类是int类型的包装类，里面包含了一个int类型的成员变量。

​								该类由final关键字修饰表示不能被继承。

​							（2）常用的方法

​								Integer(int value) - 根据参数指定的整数构造对象

​								Integer(String s) - 根据参数指定的字符串构造对象

​								该类重写了equals()、hashCode()、toString()方法

​								int intValue() - 用于获取调用对象中的整数数据并返回。

​								static Integer valueOf(int i) - 根据参数指定的整数返回对应的Integer对象。

​								static int parseInt(String s) - 用于将String类型转换为int类型并返回。

#### 					3.装箱和拆箱

​							JDK 5发布之前使用包装类对象进行运算时，需要较为繁琐的”拆箱“和“装箱”操作;即运算前先将包装类对象拆分为基本类型数据，运算后再将结果封装成包装类对象。

​								Integer i = Integer.valueOf(100);

​								Integer i = Integer.valueOf(200);

​								Integer k = Integer.valueOf(i.intValue()+j.intvalue());

​							JDK 5增加了自动"拆箱"和"装箱"的功能。

​								Integer i = 100;

​								Integer j = 200;

​								Integer k = i+j;

#### 					4.BigDecimal类

​							（1）基本概念

​								由于float类型和double类型的运算可能会有误差，为了实现精确运算则需要借助java.math.BigDecimal类型加以描述。

​							（2）常用的方法

​								BigDecimal(String val) - 根据参数指定的字符串构造对象。

​								BigDecimal add (BigDecimal augend) 

​									- 用于计算调用对象和参数对象的和并返回。

​								BigDecimal subtract(BigDecimal subtrahend)

​									- 用于计算调用对象和参数对象的差并返回。

​								BigDecimal multiply(BigDecimal multiplicand)

​									- 用于计算调用对象和参数对象的积并返回。

​								BigDecimal divide(BigDecimal divisor)

​									- 用于计算调用对象和参数对象的商并返回。

#### 					5.String类(重中之重)

​							（1）基本概念

​								java.lang.String类用于描述字符串，Java应用程序中所有字符串字面值都可以作为String类型的对象加以描述，如：“abc”等。

​								该类描述的字符串内容是个常量，一旦创建完毕后则不能更改，因此可以被共享。

​							如：

​								String str1 = "abc";

​								str1 = "123";	- 改变str1的指向而不是指向的内容。

​							（2）常量池（原理、尽量理解）

​								由于String类型描述的字符串内容是个常量不可改变，因此Java虚拟机提供了一个常量池，当Java程序中出现字符串内容时就放入常量池中，若后续出现重复的字符串内容则直接使用池中已有的对象而不需再次创建，从而提高了性能。

# String类型的各种使用

## 	一、String类的常用方法（重中之重、练熟、记住）

​				String定义有charAt方法：

​					char charAt(int index)	- 方法charAt用于返回字符串指定位置的字符。参数index表示指定的位置

​					int length()	-返回字符串字符序列的长度

​	示例：

```java
/*
	返回字符串字符序列的长度以及内容
*/
package cn.learn.day12;

public class StringCharTest {
    public static void main(String[] args) {
        // 1.构造String类型的对象
        String str1 = new String("hello");
        // 2.获取字符串的长度以及每个字符的内容
        System.out.println("字符串的长度是："+str.length());//5
        System.out.println("字符串的长度是："+str.charAt(0));//h
        System.out.println("字符串的长度是："+str.charAt(1));//e
        System.out.println("字符串的长度是："+str.charAt(2));//l
        System.out.println("字符串的长度是："+str.charAt(3));//l
        System.out.println("字符串的长度是："+str.charAt(4));//o
        System.out.println("字符串的长度是："+str.charAt(5));//越界异常
        
        System.out.println("----------------------------------");
        // 3.使用for循环打印所有字符
        for(int i = 0; i< str1.length(); i++) {
            System.out.println("下标为"+i+"的字符是："+str1.charAt(i));
        }
    }
}
```

​	示例：

```java
/*
	String类型向int类型转换
*/
public class StringToIntExample {
    public static void main(String[] args) {
        // 示例字符串
        String str = "123";

        try {
            // 使用 Integer.parseInt() 将 String 转换为 int
            int num1 = Integer.parseInt(str);
            System.out.println("使用 Integer.parseInt() 转换结果: " + num1);

            // 使用 Integer.valueOf() 将 String 转换为 Integer 对象，自动拆箱为 int
            int num2 = Integer.valueOf(str);
            System.out.println("使用 Integer.valueOf() 转换结果: " + num2);
        } catch (NumberFormatException e) {
            System.out.println("转换失败：输入的字符串不是有效的整数");
        }
    }
}
```

## 	二、String类的基本方法

​	String类的基本方法如下：

|              方法名               |                   作用                   |
| :-------------------------------: | :--------------------------------------: |
| boolean contains(CharSequence s)  | 用于判断当前字符串是否包含参数指定的内容 |
|       String toLowerCase()        |           返回字符串的小写形式           |
|       String toUpperCase()        |           返回字符串的大写形式           |
|           String trim()           |      返回去掉前导和后继空白的字符串      |
| boolean startsWith(String prefix) |      判断字符串是否以参数字符串开头      |
|  boolean endsWith(String suffix)  |      判断字符串是否以参数字符串结尾      |

​	示例：

```java
/*
	String类基本方法的使用
*/
public class StringMethodsExample {
    public static void main(String[] args) {
        // 原始字符串，前后有空格
        String str = "  Hello World!  ";

        // 使用 trim() 去除两端空格
        String trimmedStr = str.trim();
        System.out.println("trim(): \"" + trimmedStr + "\"");

        // 转换为小写
        String lowerStr = str.toLowerCase();
        System.out.println("toLowerCase(): \"" + lowerStr + "\"");

        // 转换为大写
        String upperStr = str.toUpperCase();
        System.out.println("toUpperCase(): \"" + upperStr + "\"");

        // 判断是否包含子字符串
        boolean containsHello = str.contains("Hello");
        System.out.println("contains(\"Hello\"): " + containsHello);

        // 判断是否以 "Hello" 开头
        boolean startsWithHello = str.trim().startsWith("Hello");
        System.out.println("startsWith(\"Hello\"): " + startsWithHello);

        // 判断是否以 "World!" 结尾
        boolean endsWithWorld = str.trim().endsWith("World!");
        System.out.println("endsWith(\"World!\"): " + endsWithWorld);
    }
}
```

## 	三、String类中equals方法的使用

​			equals()是定义在 Object 类中的方法，String 类对其进行了**重写**，用于**比较两个字符串对象的内容是否相等**，而不是比较它们的引用地址。

​			String类重写了继承自Object的equals方法，其逻辑为：字符序列相同的String对象equals返回true。

​			通常使用equals方法判断两个字符串的字符序列是否相同。

​			String还提供equalslgnoreCase方法，该方法在判断时将忽略大小写。

​	示例：

```java
/*
	String类中equals方法的使用
*/
public class StringEqualsExample {
    public static void main(String[] args) {
        // 创建两个字符串对象
        String str1 = "Hello";
        String str2 = "Hello";
        String str3 = new String("Hello");
        String str4 = "hello";

        // 使用 equals() 方法比较字符串内容
        System.out.println("str1.equals(str2): " + str1.equals(str2)); // true
        System.out.println("str1.equals(str3): " + str1.equals(str3)); // true
        System.out.println("str1.equals(str4): " + str1.equals(str4)); // false

        // 使用 == 比较引用地址（对比一下区别）
        System.out.println("str1 == str2: " + (str1 == str2)); // true（字符串常量池优化）
        System.out.println("str1 == str3: " + (str1 == str3)); // false（不同对象）
    }
}
```

## 	四、String类中indexof方法的使用

​			indexOf()是String类中的一个常用方法，用于**查找某个字符或子字符串在字符串中第一次出现的位置（索引）**。如果找不到，则返回-1。

​	示例：

```java
public class StringIndexOfExample {
    public static void main(String[] args) {
        String str = "Hello, welcome to the world of Java programming.";

        // 1. indexOf(char ch)
        int index1 = str.indexOf('w');
        System.out.println("indexOf('w'): " + index1); // 输出：7

        // 2. indexOf(String substring)
        int index2 = str.indexOf("Java");
        System.out.println("indexOf(\"Java\"): " + index2); // 输出：26

        // 3. indexOf(char ch, int fromIndex)
        int index3 = str.indexOf('o', 5);
        System.out.println("indexOf('o', 5): " + index3); // 输出：8（从索引5开始查找'o'）

        // 4. indexOf(String substring, int fromIndex)
        int index4 = str.indexOf("world", 20);
        System.out.println("indexOf(\"world\", 20): " + index4); // 输出：21
    }
}
```

# stringbuilder类和stringbuffer类的概念

## 	一、基本概念

​			由于String类描述的字符串内容是个常量不可更改，当程序中出现大量类似的字符串时需要单独存放从而浪费内存空间，若希望使用一块内存空间进行存储并且可以修改字符串内容，则应该使用StringBuilder类和StringBuffer类。

​			其中StringBuffer类从jdk1.0开始存在，该类支持线程安全，因此访问的效率比较低

​			其中StringBuilder类从jdk1.5开始存在，该类不支持线程安全，访问的效率比较高

​			和String对象不同，StringBuilder封装可变的字符串，对象创建后可以通过调用方法改变其封装的字符序列。

​			StringBuilder和StringBuffer在手册上基本一样。

​			区别就是StringBuilder是非线程安全的，效率较高。而StringBuffer是线程安全的，效率较低

​	示例：

```java
/*
	stringbuilder类实现对象创建和字符串的插入操作示例
*/
public class StringBuilderExample {
    public static void main(String[] args) {
        // 1. 创建一个空的 StringBuilder 对象
        StringBuilder sb1 = new StringBuilder();

        // 2. 创建一个带有初始内容的 StringBuilder 对象
        StringBuilder sb2 = new StringBuilder("Hello");

        // 3. 使用 append() 方法添加字符串
        sb1.append("Welcome to ");
        sb1.append("Java programming!");

        sb2.append(" World"); // 在 "Hello" 后追加内容

        System.out.println("sb1 内容: " + sb1.toString());
        System.out.println("sb2 内容: " + sb2.toString());

        // 4. 使用 insert() 方法在指定位置插入字符串
        sb1.insert(11, "the wonderful ");
        sb2.insert(5, ", there");

        System.out.println("插入后 sb1: " + sb1);
        System.out.println("插入后 sb2: " + sb2);
    }
}
```

​	示例：

```java
/*
	stringbuilder类实现增删改查操作
*/
public class StringBuilderCRUDExample {
    public static void main(String[] args) {
        // 创建一个初始字符串
        StringBuilder sb = new StringBuilder("Hello World");

        System.out.println("原始字符串: " + sb);

        // ✅ 增：添加和插入操作
        sb.append(" and Java"); // 在末尾追加
        sb.insert(5, ", there"); // 在索引5处插入字符串

        System.out.println("增加内容后: " + sb);

        // ✅ 删：删除部分字符
        sb.delete(5, 12); // 删除从索引5到11之间的字符（不包含12）

        System.out.println("删除部分内容后: " + sb);

        // ✅ 改：替换部分字符
        sb.replace(6, 11, "Java"); // 将索引6到10的字符替换成"Java"

        System.out.println("替换部分内容后: " + sb);

        // ✅ 查：查找字符或子串
        char ch = sb.charAt(4); // 获取索引4处的字符
        int index = sb.indexOf("Java"); // 查找"Java"第一次出现的位置

        System.out.println("字符位置4的字符是: " + ch);
        System.out.println("子串\"Java\"的索引位置是: " + index);

        // ✅ 其他常用操作
        System.out.println("当前长度: " + sb.length());
        System.out.println("当前容量: " + sb.capacity());
        System.out.println("反转字符串: " + sb.reverse()); // 反转字符串
    }
}
```

​	示例：

```java
/*
	stringbuilder类实现反转和相互转换示例
*/
public class StringBuilderConversionExample {
    public static void main(String[] args) {
        // 1. 创建一个 StringBuilder 对象
        StringBuilder sb = new StringBuilder("Java Programming");

        System.out.println("原始 StringBuilder 内容: " + sb);

        // 2. 使用 reverse() 方法进行反转操作
        sb.reverse();
        System.out.println("反转后的内容: " + sb);

        // 3. StringBuilder 转 String
        String str = sb.toString();
        System.out.println("StringBuilder 转 String: " + str);

        // 4. String 转 StringBuilder
        StringBuilder sb2 = new StringBuilder(str);
        System.out.println("String 转 StringBuilder: " + sb2);

        // 5. StringBuilder 转 StringBuffer
        StringBuffer stringBuffer = new StringBuffer(sb);
        System.out.println("StringBuilder 转 StringBuffer: " + stringBuffer);

        // 6. StringBuffer 转 StringBuilder
        StringBuilder sb3 = new StringBuilder(stringBuffer);
        System.out.println("StringBuffer 转 StringBuilder: " + sb3);
    }
}
```

# data类的概念和使用方法

## 	一、基本概念

​			java.util.Date类用于描述特定的瞬间，可以精确到毫秒。

## 	二、常用的方法

|           方法名            | 返回值类型 |                    描述                    |
| :-------------------------: | :--------: | :----------------------------------------: |
|          getTime()          |    long    |        返回此 Date 对象表示的毫秒数        |
|     setTime(long time)      |    void    |   设置此 `Date` 对象的时间为指定的毫秒数   |
|      before(Date when)      |  boolean   |        判断此日期是否在指定日期之前        |
|      after(Date when)       |  boolean   |        判断此日期是否在指定日期之后        |
|     equals(Object obj)      |  boolean   |         判断两个 Date 对象是否相等         |
|         toString()          |   String   |     将日期转换为可读字符串（默认格式）     |
| compareTo(Date anotherDate) |    int     | 比较两个日期（实现 Comparable<Date> 接口） |

​	示例：

```java
/*
	data类的示例代码
*/
import java.text.SimpleDateFormat;
import java.util.Date;

public class DateExample {
    public static void main(String[] args) {
        // 1. 创建一个表示当前时间的 Date 对象
        Date currentDate = new Date();
        System.out.println("默认格式的日期: " + currentDate);

        // 2. 使用 SimpleDateFormat 格式化日期
        SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        String formattedDate = sdf.format(currentDate);
        System.out.println("格式化后的日期: " + formattedDate);

        // 3. 获取自 1970-01-01 00:00:00 GMT 以来的毫秒数（时间戳）
        long timeInMillis = currentDate.getTime();
        System.out.println("当前时间的时间戳（毫秒）: " + timeInMillis);

        // 4. 创建一个指定时间的 Date 对象（通过时间戳）
        long specificTimeInMillis = 1609459200000L; // 表示 2021-01-01 00:00:00
        Date specificDate = new Date(specificTimeInMillis);
        System.out.println("指定时间的 Date 对象: " + sdf.format(specificDate));

        // 5. 比较两个日期（先后顺序）
        if (specificDate.before(currentDate)) {
            System.out.println(sdf.format(specificDate) + " 在 " + sdf.format(currentDate) + " 之前");
        } else if (specificDate.after(currentDate)) {
            System.out.println(sdf.format(specificDate) + " 在 " + sdf.format(currentDate) + " 之后");
        } else {
            System.out.println("两个时间相等");
        }
    }
}
```

# 集合的框架

## 	一、集合的由来

​			当需要在程序中记录单个数据内容时，则声明一个变量即可;

​			当需要在程序中记录多个类型相同的数据内容时，则声明一个一维数组即可;

​			当需要在程序中记录多个类型不同的数据内容时，则构造一个对象即可;

​			当需要在程序中记录多个类型相同的对象时，则声明一个对象数组即可;

​			当需要在程序中记录多个类型不同的对象时，则声明一个集合即可;

## 	二、集合框架结构

​			在Java语言中集合框架的顶层是：java.util.Collection集合 和 java.util.Map集合

​			其中Collection集合中操作元素的基本单位是：单个元素。

​			其中Map集合中操作元素的基本单位是：单对元素。



​			在以后的开发中很少直接使用Collection集合，而是使用该集合的子集合：List集合、Queue集合、Set集合等。

## 	三、Collection集合

#### 			1.基本概念

​					java.util.Collection集合是集合框架的根接口，其他接口是该接口的子接口。

#### 			2.常用的方法

| 方法签名                                    | 描述                                                         |
| ------------------------------------------- | ------------------------------------------------------------ |
| `boolean add(E e)`                          | 添加指定元素到此集合中（如果尚未存在）。返回值表示操作是否改变了集合。 |
| `boolean addAll(Collection<? extends E> c)` | 将指定集合中的所有元素添加到此集合中。返回值表示操作是否改变了集合。 |
| `void clear()`                              | 移除此集合中的所有元素。                                     |
| `boolean contains(Object o)`                | 如果此集合包含指定的元素，则返回 `true`。                    |
| `boolean containsAll(Collection<?> c)`      | 如果此集合包含指定集合的所有元素，则返回 `true`。            |
| `boolean isEmpty()`                         | 如果此集合不包含任何元素，则返回 `true`。                    |
| `Iterator<E> iterator()`                    | 返回在此集合中元素上进行迭代的迭代器。                       |
| `boolean remove(Object o)`                  | 从此集合中移除指定元素（如果存在）。返回值表示是否成功移除了元素。 |
| `boolean removeAll(Collection<?> c)`        | 从该集合中移除包含在指定集合中的所有元素。返回值表示操作是否改变了集合。 |
| `boolean retainAll(Collection<?> c)`        | 仅保留该集合中包含在指定集合中的元素。换句话说，移除那些不在指定集合中的元素。返回值表示操作是否改变了集合。 |
| `int size()`                                | 返回该集合中的元素数量。                                     |
| `Object[] toArray()`                        | 返回一个包含该集合中所有元素的数组。                         |
| `<T> T[] toArray(T[] a)`                    | 返回一个包含该集合中所有元素的数组；返回数组的运行时类型是指定数组的类型。 |
