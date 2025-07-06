[TOC]



# 1.计算机的体系结构

#### 1.计算机基本概念

- 计算机俗称电脑，是现代一种用于高级计算，使用非常广泛的设备，主要由**计算机硬件和计算机软件；**两个部分组成。

- 计算机硬件是客观存在的各种计算机相关设备，而计算机软件是用于控制各种硬件设备完成各种功能。
- 计算机中常见的硬件有：CPU、内存、硬盘、主板、机箱、显卡、键盘、显示器、鼠标、........
- 键盘叫做标准输入设备，显示器叫做标准输出设备。

#### 2.CPU的概念和作用

- **CPU概念：**中央处理器，是计算机中最核心的部件，相当于人的大脑。
- **CPU作用：**主要用于处理各种计算机的指令以及软件中的数据等。

#### 3.内存的概念和作用

- **内存：**计算机中的存储部件，主要用于临时存放CPU访问的数据内容，CPU直接访问且效率高。
- **优点：**速度快、随机访问、低功耗。
- **缺点：**断电会造成数据的丢失、价格昂贵、容量限制。

**科普：**

1Tb = 1024Gb

1Gb = 1024Mb

1Mb = 1024Kb

1Kb = 1024byte(字节)   

1byte = 8bit(二进制位) 

**字节：**通常一个英文字母占一个字节，一个汉字占2个字节。

**二进制位：**是一种在计算机技术中广泛使用的数制，它使用0和1两个数码来表示数据。每个二进制位（bit）表示一个二进制数码0或1，是计算机存储和处理信息的最基本单位。

**思考：**

目前主流的硬盘配置有：250G、320G、500G、1Tb、..........为啥我的计算机只有298G？？？

解析：

硬件厂商是采用的1000作为进率，而操作系统中是采用1024G作为进率。

#### 4.硬盘的概念和作用

- **硬盘：**计算机中的存储部件，CPU不能直接访问硬盘中的数据，因此效率比较低。
- **优点：**容量大，断电数据不会丢失。
- **缺点：**效率相对较低。

#### 5.常用的计算机软件

- 计算中常见的软件主要分为两部分：系统软件 和 应用软件
- 系统软件主要指操作系统，主流操作系统：Windows / Unix / Linux / ios /Android
- 应用软件主要是指安装在操作系统之上的软件：QQ、迅雷、火狐浏览器、.......

#### 6.计算机的体系结构

​	使用者 => 应用软件 => 系统软件 => 硬件设备

​		    => 其中系统软件分为：内核(Kernel) 和 外壳(Shell)

**计算机体系结构图：**

![image-20250629124403189](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629124403189.png)

# 2.Java语言的基本概念

#### 1.Java语言的背景

​	Java 语言最早诞生于 1991 年，最初被称为 OAK 语言，是 SUN 公司为一些消费性电子产品而设计的一个通用环境。当时的目标是开发一种独立于平台的软件技术。随着网络的出现，OAK 的命运发生了改变，并最终在 1995 年以 Java 的名字正式推出。

#### 2.Java语言的主要版本

- Java SE（Java Platform，Standard Edition）称之为“Java平台标准版”，主要学习Java语言的语法规范和常见类。
- Java EE（Java Platform， Enterprise Edition）称之为“Java平台企业版”，主要学习Java后台开发技术，编写B/S架构项目。
- Java ME（Java Platform， Micro Edition）称之为Java平台微型版，随着Android平台的迅速普及已经走向了淘汰。
- **B/S：**浏览器/服务器架构，是一种网络架构模式，将系统功能实现的核心部分集中到服务器上，简化了系统的开发、维护和使用。客户端只需要安装一个浏览器，通过Web服务器与数据库服务器进行数据交互。B/S架构利用了Web浏览器技术和Internet协议，实现了异构系统的连接和信息的共享。

# 3.java环境的搭建和编写

#### 1.jdk的下载和安装

- **下载方式：**

  ​	方式一：通过官网[下载](https://www.oracle.com/java/technologies/downloads/)（ctrl点击进入网站下载）

  ​	方式二：通过idea直接下载方式，如图：

  ![image-20250629132329739](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629132329739.png)

- **安装方式：**

​		若下载的是绿色版（压缩包版），则直接加压即可

​		若下载的是安装版，则直接点击一路下一步进行安装即可（自行设置安装路径切记jdk安装路劲不可有中文！）

#### 2.jdk相关概念

- jdk一般默认安装的路径在：C:\Program Files\Java目录下
- jdk的个个目录文件，如图：

![image-20250629133618449](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629133618449.png)

**作用：**

- **bin**：存放Java开发和运行所需的可执行文件和工具，例如javac（编译器）、java（解释器）和jar（打包工具）。这是开发者最常使用的目录。
- **lib**：包含JDK运行时所需的库文件和支持文件，如tools.jar等。这些文件主要用于支持Java基础功能。
- **include**：提供C/C++头文件，用于JNI（Java Native Interface）开发，允许Java程序与本地代码交互。
- **jre**：Java运行环境目录，包含运行Java应用程序所需的核心组件，如虚拟机和类库。
- **mods**：模块化系统相关文件，适用于Java 9及以上版本，支持模块化开发。
- **jvm：**Java虚拟机，是Java程序与计算机操作系统之间的桥梁。
- **javac.exe：**Java语言的编译器，主要用于将Java源代码进行编译生成字节码文件。
- **java.exe：**Java语言的解释器，主要用于启动Java虚拟机对字节码文件进行解释执行。

#### 3.Java程序的编写流程

- 新建文本文档，将文件名的后缀由xxx.txt修改成xxx.java；
- 使用记事本的方式打开文件，编写java代码后进行保存；
- 启动dos窗口，切换到xxx.java文件所在的路径中；
- 使用javac xxx,java进行编译，生成xxx.class的字节码文件
- 使用java xxx进行解释执行，打印最终结果；

**注意：**

​	当文件扩展名不显示是的处理方式：

​		找到查看 => 显示 => 文件扩展名 => 勾上

![image-20250629140035982](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629140035982.png)

#### 4.helloworld代码的编写和运行

##### 4.1.代码组成

![image-20250629140900151](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629140900151.png)

##### 4.2.**环境变量的配置：**

- **基本概念：**通常情况下可执行文件只能在该文件所在的路径中访问，若希望该可执行文件可以在任意路径中使用则需要将该可执行文件的路径信息配置到环境变量Path中。

- 运行代码还需进行环境变量的配置，将默认路径C:\Program Files\Java\bin或者你的自定义安装路径添加到环境变量当中

  ​            右键计算机 => 选中属性 => 找到并点击高级系统设置 => 点击环境变量

  ​                                => 找到系统变量 => 找到并点击path 

  ​                                =>添加路径C:\Program Files\Java\bin

  ![image-20250629143030423](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629143030423.png)

##### 4.3**运行流程：**

**流程图：**

![image-20250629143805060](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629143805060.png)

- 先javac 文件名（带后缀） 进行编译这个java代码（不报错则编译成功，报错则代码写的有问题）

![image-20250629143205128](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629143205128.png)

- java 文件名（不带后缀）进行解释执行

![image-20250629143509466](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629143509466.png)

#### 5.常用的快捷键

| CTRL+S 保存                        | CTRL+C 复制                     | CTRL+V 粘贴                                | CTRL+F 查找            |
| ---------------------------------- | ------------------------------- | ------------------------------------------ | ---------------------- |
| **CTRL+X 剪切**                    | **CTRL+Z 撤销**                 | **CTRL+A 全选**                            | **Windows+D 回到桌面** |
| **Windows+E 打开计算机**           | **Windows+L 锁屏**              | **windows+R 打开运行，输入cmd进入dos窗口** | **alt+tab 切换任务**   |
| **CTRL+ALT+DELETE 启动任务管理器** | **CTRL+shift 切换中英文输入法** |                                            |                        |

####  6.跨平台原理

 ![image-20250629144711007](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629144711007.png)

**Java字节码可以通过JVM翻译为具体平台能够执行的机器指令。由于Sun定义了JVM规范，而且不同的操作系统大多提供了JM实现，才使得相同的一个字节码文件可以在不同的系统上运行，从而使Java赢得了“一次编译，到处使用”的美名。**

#### 7.Java常见的开发工具

- 编辑器

  记事本、Notepad++、EditPlus、UltraEdit

- 集成开发环境

  JBuilder、NetBeans、Eclipse/MyEclipse、Idea

# 2.Java语言的基本概念

#### 1.Java语言的背景

​	Java 语言最早诞生于 1991 年，最初被称为 OAK 语言，是 SUN 公司为一些消费性电子产品而设计的一个通用环境。当时的目标是开发一种独立于平台的软件技术。随着网络的出现，OAK 的命运发生了改变，并最终在 1995 年以 Java 的名字正式推出。

#### 2.Java语言的主要版本

- Java SE（Java Platform，Standard Edition）称之为“Java平台标准版”，主要学习Java语言的语法规范和常见类。
- Java EE（Java Platform， Enterprise Edition）称之为“Java平台企业版”，主要学习Java后台开发技术，编写B/S架构项目。
- Java ME（Java Platform， Micro Edition）称之为Java平台微型版，随着Android平台的迅速普及已经走向了淘汰。
- **B/S：**浏览器/服务器架构，是一种网络架构模式，将系统功能实现的核心部分集中到服务器上，简化了系统的开发、维护和使用。客户端只需要安装一个浏览器，通过Web服务器与数据库服务器进行数据交互。B/S架构利用了Web浏览器技术和Internet协议，实现了异构系统的连接和信息的共享。

# 3.java环境的搭建和编写

#### 1.jdk的下载和安装

- **下载方式：**

  ​	方式一：通过官网[下载](https://www.oracle.com/java/technologies/downloads/)（ctrl点击进入网站下载）

  ​	方式二：通过idea直接下载方式，如图：

  ![image-20250629132329739](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629132329739.png)

- **安装方式：**

​		若下载的是绿色版（压缩包版），则直接加压即可

​		若下载的是安装版，则直接点击一路下一步进行安装即可（自行设置安装路径切记jdk安装路劲不可有中文！）

#### 2.jdk相关概念

- jdk一般默认安装的路径在：C:\Program Files\Java目录下
- jdk的个个目录文件，如图：

![image-20250629133618449](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629133618449.png)

**作用：**

- **bin**：存放Java开发和运行所需的可执行文件和工具，例如javac（编译器）、java（解释器）和jar（打包工具）。这是开发者最常使用的目录。
- **lib**：包含JDK运行时所需的库文件和支持文件，如tools.jar等。这些文件主要用于支持Java基础功能。
- **include**：提供C/C++头文件，用于JNI（Java Native Interface）开发，允许Java程序与本地代码交互。
- **jre**：Java运行环境目录，包含运行Java应用程序所需的核心组件，如虚拟机和类库。
- **mods**：模块化系统相关文件，适用于Java 9及以上版本，支持模块化开发。
- **jvm：**Java虚拟机，是Java程序与计算机操作系统之间的桥梁。
- **javac.exe：**Java语言的编译器，主要用于将Java源代码进行编译生成字节码文件。
- **java.exe：**Java语言的解释器，主要用于启动Java虚拟机对字节码文件进行解释执行。

#### 3.Java程序的编写流程

- 新建文本文档，将文件名的后缀由xxx.txt修改成xxx.java；
- 使用记事本的方式打开文件，编写java代码后进行保存；
- 启动dos窗口，切换到xxx.java文件所在的路径中；
- 使用javac xxx,java进行编译，生成xxx.class的字节码文件
- 使用java xxx进行解释执行，打印最终结果；

**注意：**

​	当文件扩展名不显示是的处理方式：

​		找到查看 => 显示 => 文件扩展名 => 勾上

![image-20250629140035982](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629140035982.png)

#### 4.helloworld代码的编写和运行

##### 4.1.代码组成

![image-20250629140900151](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629140900151.png)

##### 4.2.**环境变量的配置：**

- **基本概念：**通常情况下可执行文件只能在该文件所在的路径中访问，若希望该可执行文件可以在任意路径中使用则需要将该可执行文件的路径信息配置到环境变量Path中。

- 运行代码还需进行环境变量的配置，将默认路径C:\Program Files\Java\bin或者你的自定义安装路径添加到环境变量当中

  ​            右键计算机 => 选中属性 => 找到并点击高级系统设置 => 点击环境变量

  ​                                => 找到系统变量 => 找到并点击path 

  ​                                =>添加路径C:\Program Files\Java\bin

  ![image-20250629143030423](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629143030423.png)

##### 4.3**运行流程：**

**流程图：**

![image-20250629143805060](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629143805060.png)

- 先javac 文件名（带后缀） 进行编译这个java代码（不报错则编译成功，报错则代码写的有问题）

![image-20250629143205128](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629143205128.png)

- java 文件名（不带后缀）进行解释执行

![image-20250629143509466](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629143509466.png)

#### 5.常用的快捷键

| CTRL+S 保存                        | CTRL+C 复制                     | CTRL+V 粘贴                                | CTRL+F 查找            |
| ---------------------------------- | ------------------------------- | ------------------------------------------ | ---------------------- |
| **CTRL+X 剪切**                    | **CTRL+Z 撤销**                 | **CTRL+A 全选**                            | **Windows+D 回到桌面** |
| **Windows+E 打开计算机**           | **Windows+L 锁屏**              | **windows+R 打开运行，输入cmd进入dos窗口** | **alt+tab 切换任务**   |
| **CTRL+ALT+DELETE 启动任务管理器** | **CTRL+shift 切换中英文输入法** |                                            |                        |

####  6.跨平台原理

 ![image-20250629144711007](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250629144711007.png)

**Java字节码可以通过JVM翻译为具体平台能够执行的机器指令。由于Sun定义了JVM规范，而且不同的操作系统大多提供了JM实现，才使得相同的一个字节码文件可以在不同的系统上运行，从而使Java赢得了“一次编译，到处使用”的美名。**

#### 7.Java常见的开发工具

- 编辑器

  记事本、Notepad++、EditPlus、UltraEdit

- 集成开发环境

  JBuilder、NetBeans、Eclipse/MyEclipse、Idea

# 4.Java语言的基本语法格式

#### 1.变量的基本概念

##### 1.1 基本概念

​	当需要在Java程序中记录单个数据内容时，则声明一个变量即可，而声明变量的本质就是在内存空间中申请一块存储单元，由于该存储单元的数值可以发生改变，因此得名为“变量”。

​	由于存放数据内容的大小不同导致所需存储单元的容量不同，在Java语言中使用数据类型加以描述，为了便于下次访问还需要指定变量的名称。

##### 1.2 变量的声明方式

- Java变量在使用前必须初始化，也就是赋以确定的初值。
- 属性系统会自动初始化

![image-20250630191002990](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630191002990.png)

- 数据类型 变量名 = 初始值；

**举例：**

​	int age = 18；

![image-20250630173554194](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630173554194.png)

![image-20250630173628082](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630173628082.png)

#### 1.3 标识符的命名法则

- 变量名必须显示标识符，标识符命名的一些规则：

  1.必须是字母、数字、下划线、$等组成，其中数字不能开头

     如：

  ​	name、age、name2、age2....

  2.不能是Java关键字，比如：public static class......

  ![image-20250630191728542](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630191728542.png)

  3.大小写敏感，长度没有限制，但不宜过长

  如：

  ​	name和Name代表不同的标识符，不推荐使用

  4.标识符尽量做到见名知意，可以是汉字，但是不推荐使用

  如：

  ​	year、month、size、length、time等

- 标识符可以给类/变量/属性/方法/包起名字。

#### 1.4 变量的输入输出

##### 										项目案例

- 提示用户输入姓名和年龄信息 ，最后打印出来

​	![image-20250630192248094](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630192248094.png)

![image-20250630192343061](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630192343061.png)

- 变量的输出的优化

  ![image-20250630192551887](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630192551887.png)

#### 1.5 注释的概念和注意事项

**注释用于解释代码，给程序员看但计算机会忽略注释，主要包括以下三种：**

-  //  表示单行注释，从 // 开始一直到本行的末尾的所有内容都是注释。
-  /******/ 多行注释，从 /*开始，到 */结束，中间所有都是注释。
-  /** */多行注释，从 /**开始，到 */结束，是一种支持提取的注释。

**注意：**

​	多行注释不能嵌套使用！

#### 1.6 数据类型的分类和常用进制

1. **基本分类**

   在Java语言中将数据类型分为两大类：

   （1） 基本数据类型

   ​	byte、short、int、long、float、double、boolean、char

   （2） 引用数据类型

   ​	数组、类、接口、注释、枚举

2. **常用的进制**

   在日常生活中采用十进制进行数据的描述，权重：10^0、10^1、10^2、·············

   在计算机底层采用二进制进行数据的描述，权重：2^0、2^1、2^2············

   由于现实生活中的数据具有正负数，因此二进制中采用最高位（最左边）代表符号位，若是0则代表非负数，若是1则代表负数。

如：				千（10^3）	百（10^2）	十（10^1）	  个（10^0）

​	十进制整数： 	1			2			3				4

3. **进制之间的转换**

   （1）正十进制转换为二进制的方式

   ​	   a.除2取余法，使用十进制整数不断的除以2直到商为0时，将余数逆序排序即可

   ![image-20250630194425707](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630194425707.png)

   ​	   b.拆分法，将十进制整数拆分为若干个二进制权重的和，若有该权重下面写1，否则写0

   ​		如：

   ​			45 = 32 + 8 + 4 + 1

   ​				128	64	32	16	8	4	2	1

​					 0	    0	   1	  0	 1	1	0	1	=> 	0010  1101

​	（2）正二进制转换为十进制的方式

​		a.加权法，使用二进制中的每个数字乘以当前位的权重再累加起来。

​		如：

​		0010  1101 = 0 * 2^7 + 0 * 2^6 + 1 * 2^5 + 0 * 2^4 + 1 * 2^3 + 1*2^2 + 0 *2^1 + 1 * 2^3

​				    = 0+0+32+0+8+4+0+1

​				    =45

​	（3） 负十进制转换为二进制的方式

​		a.先将十进制的绝对值转换为二进制，进行按位取反再加1.

​		如：

​			-45	=> 绝对值转换为二进制：0010  1101

​				      => 按位取反：		    1101  0010		

​				      => 加1：		    	  1101  0011	

​	（4） 负二进制转换为十进制的方式

​		a.先减一再按位取反，然后合并为十进制整数后添加负号。

​		如：

​			1101  0011 => 先减一：		1101  0010

​					      => 按位取反：    	1101  0010

​					      => 合并为十进制：     45

​					      => 添加负号：     	-45

![image-20250630200500052](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630200500052.png)

# 5.Java语言的流程控制

#### 1.分支结构

##### 1.1 基本概念

​	在某些特殊场合中需要进行判断并作出选择时，就需要使用分支结构

![image-20250701100038522](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250701100038522.png)

##### 1.2 if分支结构

(1)语法格式

​	if(条件表达式){

​			语句块;

}
(2)执行流程

​	判断条件表达式是否成立

​				=>若成立，则执行语句块:

​				=>若不成立，则跳过语句块;

```
import java.util.Scanner;
public class IfTest{
	public static void main(String[] args){
	//1.提示用户输入年龄信息并使用变量记录
	System.out.println("请输入您的年龄:”);
	Scanner sc =newScanner(System.in);
	int age = sc.nextInt();
	//2.使用if分支结构判断是否成年并给出对应的提示
	if(age >= 18){
	System. out.println("开心地浏览起了网页...")
	}
	//3.无论是否成年都打印一句话
	System.out.println("无奈的回家")
	}
}

```

##### 1.3 if-else分支结构

(1)语法格式

​	if(条件表达式){

​			语句块1;

​			}else{

​				语句块2;

}

(2)执行流程

​	判断条件表达式是否成立

​			=>若成立，则执行语句块1;

​			=>若不成立(否则)执行语句块2:

```
public class IfElseTest{
	public static void main(String[] args){
	//1.提示用户输入考试成绩并使用变量记录
	System.out.println("请输入您的考试成绩:”);
	Scanner sc =newScanner(System.in);
	int score = sc.nextInt();
	//2.使用if-else分支结构判断是否及格并给出对应的提示
	if(score >=60){
	System.out.println("恭喜您考试通过了!");
	}else{
	System.out.println("下学期来补考吧!");
	}
	//3.打印一句经典语录
	System.out.println("世界上最遥远的距离不是生和死，而是你在if我在else，看似相交却永远分离！");
	}
}

```

##### 1.4 if-else if-else

```
(1)语法格式
if(条件表达式1){
	语句块1;
}
else if(条件表达式2){
	语句块2;
}else{
	语句块n;
}

```

```
(2)执行流程
		判断条件表达式1是否成立
			=>若成立，则执行语句块1;
			=>若不成立，则判断条件表达式2是否成立
			=>若成立，则执行语句块2;
			=>若不成立，则执行语句块n;
```

```
import java.util.Scanner;
public class IfElseifElseTestf{
public static void main(Stringll args){
	//1.提示用户输入身份信息并使用变量记录
	System.out.println("请输入您的身份信息”)；
	Scanner sc=newScanner(System.in);
	String str = sc.next();
	//2.使用if-else if-else分支结构判断身份信息并给出对应的提示
	if("军人".equals(str)){
	System.out.println("请免费乘车!");
	}else if("学生”.equals(str)){
	System.out.println("请购买半价票!");
	}else{
	System. out.printhn("全价票等着您!");
	}
	//3.打印一句话
	System.out.println("坐上了火车去拉萨，去看那美丽的布达拉!");
}

```

##### 2 for循环的概念和使用

##### 2.1 基本概念

在某些特殊场合中需要重复执行一段代码时，借助循环结构加以处理。

![image-20250701102138267](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250701102138267.png)

```
public class ForTest{
public static void main(String args)throws Exception{
	for(int money=500;money>=100;money-=100){
	System.out.println("当前账户余额:“+money +”，正在出钞，请稍后.....”）
	Thread.sleep(5000);//休眠5秒的过程
	System.out.println("请取走您的钞票!\n\n\n”);
	}
	System. out.println("现在可以尽情地挥霍了...”);
}
}

```

##### 2.2 for循环实现累加

**练习:**

​	使用for循环计算1~100之间所有整数的累加和并打印

```
public class ForSumTest{
	public static void main(String args){
	//声明局部变量记录累加的结果
	int sum=0;
	for(int i=1;i<= 10000;i++){
	sum +=i;//sum=sum +i;13 6....
	}
	System.out.println("最终的累加结果是:”+ sum);//50005000
	}
}

```

##### 2.2.1 break和continu关键字的使用

**continu关键字**

- continue语句用在循环体中，用于结束本次循环而开始下一次循环。

```
for (inti=0;i<10; i++){
if(i%5==0) continue;
System.out.print(i+" ");
}
//输出的结果是:12346789当i==5时，结束本次循环继续下一次循环，因此5没有输
```

**break关键字**

- break关键字用于循环中表示跳出当前循环:

**实现continu关键字break关键字**

```
public class BreakContinueTest{
	public static void main(String[] args){
	for(int i=1;i<=20;i++){
	if(0 == i%5){
	continu;//结束本次循环继续下一次循环
	}
	if(18 == i){
		break;//跳出当前循环
	}
	System.out.println("i="+i);//1 2 3 4 6........
	}
	//break执行后跳到这里了......
	}
}

```

##### 2.2.2 双重循环

```
(1)语法格式
for(初始化表达式1;条件表达式2;修改初始值表达式3){
	for(初始化表达式4;条件表达式5;修改初始值表达式6){
		循环体;
	}
}	
(2)执行流程
		执行表达式1=>判断表达式2是否成立
		=>若成立，则执行表达式4=>判断条件表达式5是否成立
		=>若成立，则执行循环体=>执行表达式6=>判断表达式5是否成立
		=>若不成立，则内层循环结束=>执行表达式3=>判断表达式2是否成立
		=>若不成立，则外层循环结束
```



```
public class ForForTest{
	public static void main(Stringl args){
	//1.使用for循环打印5行字符串内容"厉害了我的哥”
	for(int i=l:i<=5:i++){
	System.out.println("厉害了我的哥!")
	}

	//2.使用for循环打印5列字符串内容"厉害了我的哥"
	for(int i=1:i<= 5:i++){
	//打印完毕不换行
	System.out.print("厉害了我的哥!");
	}
	// 专门用于换行
	System.out.println();
	System.out.println("--------------")
	//3.使用for循环打印5行5列字符串内容"厉害了我的哥"
	for(int i=1;i<=5;i++){
		for(int j=1;j<=5;j++){
		//打印完毕不换行
		System.out.print("厉害了我的哥!");
		}
		// 专门用于换行
		System.out.println();
	}
}

```

##### 3.while循环的概念和使用

```
(1)语法格式
	while(条件表达式){
	循环体;
	}
(2)执行流程判断条件表达式是否成立
		=>若成立，则执行循环体=>判断条件表达式是否成立
		=>若不成立，则循环结束
```

```
public class Whilelest{
	public static void main(Stringll args){
	//1.使用for循环打印1~10之间的所有整数
	for(int i=1:i<= 10:i++){
	System.out.println("i=”+ i)
	}
	System. out.println("------“)
	//2.使用while循环打印1~10之间的所有整数
	int i =l;
	while(i<= 10){
	System.out.println("i="+ i);
	i++;
}
}

```

###### 3.1 switch_case分支结构

```
(1)语法格式
switch(变量/表达式){
	case 字面值1;语句块1;break;
	case字面值2;语句块2;break;
	....
	default:语句块n;
(2)执行流程
		计算变量/表达式的数值=>判断是否匹配字面值1
		=>若匹配，则执行语句块1=>执行break跳出当前结构
		=>若不匹配，则判断是否匹配字面值2
		=>若匹配，则执行语句块2=>执行break跳出当前结构
		=>若不匹配，则执行语句块n
```

```
import java.util.Scanner;
public class TestSwitchMenu{
	public static viod main(String[] argvs){
	//1.提示用户输入1~5之间的整数并使用变量记录
	System.out.println("请输入1~5之间的整数：");
	Scanner sc = New Scanner(System.in);
	int choose = sc.nextInt();
	//2.使用switch-case分支结构根据不同的输入给出对应的提示
	switch(choose){
		case1: System.out.println("显示所有用户");break;
		case2: System.out,println("增加新用户");break;
		case3: System.out.println("修改用户信息");break;
		case4: System.out.println("删除用户信息");break;
		case5: System,out.println("退出系统");break;
		default: System.out.println("输入错误，请重新输入！");
	}
	}
}
```

# 6.Java语言的数组声明与应用

#### 1.数组的基本概念

##### 1.1数组的基本概念

​	当需要在程序中记录单个数据内容时，则声明一个变量即可;当需要在程序中记录多个类型相同的数据内容时，则声明一维数组即可，一维数组的本质就是在内存中申请一段连续的存储单元。

![image-20250701143736672](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250701143736672.png)

- 数组是相数据类型的多个元素的容器，元素按线性顺序排列。
- 所谓线性顺序是指除第一个元素外，每一个元素都有唯一的前驱元素;除最后一个元素外，每一个元素都有唯一的后继元素(“一个跟一个”)
- 数组的操作其实就是对下标的控制，可以通过下标方式访问数组中每个元素

1.2声明方式

（1）语法格式

​	数据类型[]数组名称=new 数据类型[数组的长度]:
如:
int [] arr = new int[5];//表示声明一个长度为5元素类型为int类型的一维数组

int num=5;//表示声明一个初始值为5的变量
int arr[]=new int[5];//不推荐使用

```
public static void main(String[] args){
//1.声明一个长度为3元素类型为int类型的一维数组
int[] arr =new int[3];
//2.打印数组的长度以及每个元素的数值
System.out.println("数组的长度是:+ arr.length);
System.out.println("下标为0的元素是:+ arr0);
System.out.println("下标为1的元素是:+ arr[1]);
System.out.println("下标为2的元素是:+ arr[1]);
//编译ok 运行产生ArrayIndex0ut0fBoundsException数组下标越界异
//System.out.println("下标为3的元素是:+ arr[3]):
System.out.println("---------------------")
//3.使用循环实现数组中所有元素的打印
for(int i = 0;i<arr.length;i++){
	System.out.println("下标为"+i+"的元素是："+arr[i]);
		}
	}
}
```

**数组初始化**

- 基本类型的数组，(数据元素为基本类型)创建店，其元素的初始值:byte:short、char、it、long为0;float和double为0.0;boolean为false。

- 可以在数组声明的同时进行初始化，例如:

  int[] arr={10,23,30,-10,96.21};

- 但此种方式只能用于声明时的初始化，若用于赋值则有编译错误，例如:intl] arr;
  arr={10,23,30,-10,96,21}};

```
public static void main(String  args){
//1.声明一个长度为3元素类型为int类型的一维数组
int arr = new int[3];
//2.打印数组的长度以及每个元素的数值
System.out.println("数组的长度是:+ arr.length);//3
System.out.println("下标为0的元素是:"+ arr[0]);//0 默认值
System.out.println("下标为1的元素是://0+ arrl);//0
System.out.println("下标为2的元素是:帅+ arr[2]);
//编译ok 运行产生ArrayIndex0utOfBoundsException数组下标越界异常
System.out.println("下标为3的元素是:+ arr[3]);
System.out.println("------------------")
//3.使用循环实现数组中所有元素的打印
for(int i = 0;i<arr.length;i++){
System.out.println("下标为"+i+"的元素是："+arr[i]);//0
}
}

```

**数组的增删改查**

```
public class ArrayOperationTest{
	public static void main(String[] args){
	//1.声明一个长度为5元素类型为int类型的一维数组
	int[] arr = new int [5]
	//打印所有元素值
	for（int i=0;i<arr.length;i++){
		System.out.print(arr[i]+"");
	}
	System.out.println();
	//打印所有元素
	System.out.print("数组赋值后的元素为;
	for(int i=0;i<arr.length;i++){
		System.out.print(arr[i]+"");
	}
	System.out.println();
	System.out.println("-----------")
	//3.将数据50插入到数组中下标为0的位置，原有元素向后移动
	for(inti=4;i>0;i--){
	arrli]= arr[i-l];
	}
	arr[0]= 50;
	//再次打印
	System.out.print("数组插入后的元素为:")
	for(int i=0;i<arr.length; i++){
	System.out.print(arr[i]+"");//50 10 20 30
	}
	System.out.println()
	}
}
```

##### 1.2 二维数组的基本概念

​	**二维数组本质上就是由多个一维数组组成(摞在一起)的数组，也就是说二维数组中的每个元素都是一个一维数组，而一维数组中的每个元素才是数据内容**

- Java允许使用多维数组，其中最常见的就是二维数组。

- 二维数组就是由一维数组组成的数组，其元素是一维数组。

- 二维数组定义时需要两个中括号，方式如下:

  ​	int[][] arr= new int[2][3];

  ​	int[]] arr= newint[3]ll;

- 定义二维数组arr以后，arr是二维数组，arr[i]是一维数组，arr[i][j]是数据。

  其中，最左边的中括号里面必须有长度。

![image-20250701163710472](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250701163710472.png)

(1)语法格式数据类型[][]数组名称 = new 数据类型[行数] [列数]
	如:
	int[][]brr = new int[2] [3];-声明一个具有2行3列元素类型为int类型的二维数组

其中行下标的范围是:0~1:

其中列下标的范围是:0~2:

**维数组的分析:**
brr.length表示二维数组的长度,也就是二维数组中元素的个数，也就是一维数组的个数，也就是行数brr[0].length表示二维数组中的第一个元素的长度,也就是第一行的长度,也就是第一行的列数brr[0][0] 表示二维数组中第一行第一列的数据内容

# 7.运算符与表达式

#### 1 运算符的概念和使用

##### 1.1 算术运算符

 + +表示加法运算符	-表示减法运算符	*表示乘法运算符	/表示除法运算符	%表示取模/取余运算符

   ![image-20250630201103661](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630201103661.png)

注意事项:
（1）在Java语言中两个整数相除时，结果只保留整数部分丢弃小数部分;

（2）若希望保留小数部分，则处理方式如下:

​	a.将其中任意一个操作数强转为double类型进行运算即可:

​	b.让其中任意一个操作数乘以1.0后进行运算即可(推荐);

（3）0不能做除数，0.0可以做除数但结果是无穷

（4）+既可以作为算术运算符也可以作为字符串连接符，区分方式如下：

- 只要+两端的操作数中有一一个是字符串类型，则按照字符串连接符对待，结果字符串

![image-20250630201252388](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630201252388.png)

- 加（+）减(-)、乘(*)、除(/)、取余(%)

- 整数粗除，只能取整数部分，小数部分被舍弃。

- 整数运算时，0不能做除数; 浮点运算时，0.0可以，但结果是无穷。

- 算数运算看起来简单，其实有难度。

  int a = 121;	int b= 15;	intc=a/b;	inta=5;	System.out.println(a% 2);

  结果是8，整数除法会取整	计算a除以2取余数，结果是1。

**项目案例：**

- 提示用户输入整数类型的秒数，输出x小时x分x秒。

  如：输入7199，输出1小时59分59秒。

![image-20250630202212805](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630202212805.png)

 1.1.1**字符串连接运输符**

- +可以实现字符串的连接。同时可以实现字符串与其他数据类型“相连

![image-20250630202402080](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630202402080.png)

 1.1.2**关系运算符*****/*****比较运算符****

- .>表示是否大于运算符	>=表示是否大于等于运算符
- .<表示是否小于运算符	<=表示是否小于等于运算符
- ==表示是否等于运算符        ！=表示是否不等于运算符

所有以关系运算符作为最终运算的表达式结果一定是boolean类型，只有true和false

![image-20250630203806017](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630203806017.png)

 1.1.3**自增自减运算符**

- +表示加法运算符，++表示自增运算符，主要用于使得变量自身的数值加1
- -表示减法运算符，--表示自减运算符，主要用于使得变量自身的数值减1

注意:
(1)对于变量自身来说，++ia和ia++都实现变量自身数值的加1效果，是等价的:

(2)ia++表示先让ia的数值作为整个表达式的结果，表示先让ia自身的数值加1，++ia表示先让自身的数值加1，然后再作为整个表达式的结果；

注意:
a.对于变量自身的数值来说，无论++放在变量前还是变量后都是一样的结果;

b.ia++ 后++表示先使用ia变量白身的数值作为表达式的结果，然后ia自身的数值再加1;++ia 前++表示先让ia变量自身的数值加1，然后再作为表达式的结果:

 1.1.4 **逻辑运算符**

- 逻辑运算符的操作数均为boolean表达式。

- 逻辑运算符:&&与||或 ! 非

- && 表示逻辑与运算符，相当于"并且”，同真为真，一假为假

- ||表示逻辑或运算符，相当于"或者”，一真为真，同假为假

- ！表示逻辑非运算符，相当于"取反"，真为假，假为真。

- 逻辑运算符两端的操作数都是boolean类型的，结果应该是boolean类型的。

  短路特性:
  若第一个条件为假则整个表达式一定为假，对于逻辑与来说，铁掀二个条件不用判断对于逻辑或来说，若第一个条件为真则整表达式一定为真，二个条件不用判断;

![image-20250630204736792](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630204736792.png)

![image-20250630205026635](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630205026635.png)

&&、||具备“短路“的特性:如果通过第一个表达式的值即可得出最后的结果，则不计算第二个表达式。

1.1.5 **三元运算符**

- 条件运算符又称”三目运算符“，其结构为:

​	条件表达式?表达式1:表达式2

- 先计算boolean表达式的值，如果为true，则整个表达式的值为表达式1的值;如果为false，则整个表达式的值为表达式2的值。

```
int a =100,b=200
int flag=a>b?1:-1; flag的值为-1
int a = 100,b=200;
int max = a>=b?a:b; max的值为200
```

![image-20250630205623757](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630205623757.png)

1.1.6 **赋值运算符**

(1)简单赋值
=表示赋值运算符，主要用于将=右边的数据赋值给=左边的变量，覆盖原来的数值
如:
	ia=2;-表示使用数据2给变量ia赋值，覆盖该变量ia原来的数值笔试题:
	ia == 2;-判断ia的数值是否等于2判断2是否等于ia的数值，结果与上述方式等价，但推荐该方式2 	== ia:ia = 2;将数据2赋值给变量ia，覆盖原来的数值2= ia;编译报错
(2)复合赋值
+=、-=、*=、·······
如:
int ia = 2,
ia = ia + 3:从结果上等价于:ia+=3.

1.1.7 **运算符的优先级**

![image-20250630205959253](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250630205959253.png)

1.1.8 **位移运算符的概念和基本使用**

**移位运算符**

- 左移(<<)、算数右移(>>)逻辑右移

- 移位运算针对于整数做二进制位移动。
- <<表示左移运算符，用于将数据的二进制位向左移动，右边使用0补充
- .>>表示右移运算符，用于将数据的进制位向右移动，左边使用符号位补充
- .>>>表示逻辑右移运算符，用于将数据的二进制位向右移动，左边使用0补充

 **位运算符**

1.&表示按位与运算符，就是按照二进制位进行与运算，同1为1，一0为0(1-真 0-假).
2.|为表示按位或运算符，就是按照二进制位进行或运算，一1为1，同0为0.表示按位取反运算符，按照3.~二进制位进行取反，1为0，0为1.

4.^表示按位异或运算符，按照二进制位进行异或运算，相同为0，不同为1.

# 8.对象和面向对象

### 1.对象和面向对象的概念

#### 1.1 什么是对象?

​	万物皆可对象

#### 1.2 什么是面向对象？

​	面向对象就是指以特征(属性)和行为的观点去分析现实世界中事物的方式。

#### 1.3 什么是面向对象编程

​	面向对象编程就是指先使用面向对象的方式进行分析，再使用任意一门面向对象的编程语言进行翻译的过程。

​	其中C语言是一门面向过程的编程语言。

​	其中C++语言是一门既面向过程又面向对象的编程语言

​	其中Java语言是一门纯面向对象的编程语言。

#### 1.4 如何学好面向对象编程

​	深刻理解面向对象编程的三大特征:封装、继承、多态。

### 2.类、对象以及引用

#### 2.1对象和类的概念

​	对象是客观存在的实体，在Java语言体现为内存空间的一块区域。

​	类就是分类的概念，是对具有相同特征和行为的多个对象共性的抽象描述，在Java语言中包含描述特征的成员变量和描述行为的成员方法

- 类是一-个**概念(名词)**抽象的定义。简单说就是分类。
- 类定义了该类型对象的数据结构，称之为**成员变量**些可以被调用的功能，称之为 成员方法。
  同时，也定义了一些可以被调用的功能，称之为**成员方法**
- 类是用于构建对象的模板，对象的实质就是内存中一块存储区域，其数据结构由定义它的类来决定。

#### 2.2 类的定义

（1）类定义的语法格式

```
class 类名{
 类体;
}
如:
class Person{

}
注意:
当类名由多个单词组成时，要求每个单词的首字母都要大写;
(2)成员变量定义的语法格式
class 类名{
数据类型 成员变量名=初始值; -其中=初始值通常省略，但分号不能省略
}
加:
class Person{
String name ;
int age;
}
注意:
当成员变量名由多个单词组成时，要求从第二个单词起每个单词首字母大写
扩展:
局部变量-主要指在方法体中声明的变量，作用范围从声明开始到方法体结束
成员变量-主要指在方法体外类体内声明的变量，作用范围从声明到类体结束
```

#### 2.3 对象的创建

- 当一个类的定义存在后，可以使用**new运算**创建该类的对象。对象创建的过程一般称为**类的实例化。**
- new 类名();

```
（1）语法格式
new 类名();
如:
new Person();-创建Person类型的对象，由于该对象没有名字因此叫做"匿名对象
(2)注意事项
a.当一个类定义完毕后，使用new关键字创建/构造对象的过程叫做 类的实例化;
b.创建对象的本质就是在内存中的堆区申请存储空间，来存放该对象独有的特征信息
```

#### 2.4 引用

（1）基本概念

在Java语言中使用引用数据类型声明的变量叫做引用型变量，称为"引用”

引用变量主要用于记录对象在堆区中的内存地址信息，便于下次访问。

(2)语法格式

类名 引用变量名:
如:
Person p; - 表示声明Person类型的引用变量p，在栈区申请存储空间
Person p=newPerson(); - 表示声明引用变量p来记录Person类型对象的地址信息

引用变量名.成员变量名;

如：

p.name = "zhangfei"; - 表示使用引用变量p访问所指向堆区对象的姓名特征

#### 2.5 point类

```
public class Point{
	int x;
	int y;
	public static void main(String[] args){
	//声明Point引用指向Point对象，打印特征的默认数值
	Point p = new Point();
	System.out.println("-----------------");
	//修改特征的数值为3和5后再次打印
	p.x = 3;
	p.y = 5;
	System.out.println("横坐标是:"+p.x+",纵坐标是:"+p.y);//3.5
	}
}
```

![image-20250702163445692](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250702163445692.png)

#### 2.6 成员方法的语法格式

```
语法格式
class 类名{
	返回值类型成员方法名(形参列表){
		成员方法体;
	}
}
如:
class Person{
	void show(){
		System.out.println("没事出来秀一下!");
	}
}
注意:当成员变量名由多个单词组成时，通常要求从第二个单词起每个单词首字母大写。
```

**详解：**

（1）返回值类型
	返回值主要指从方法体内向方法体外返回的数据内容。

​	返回值类型主要指返回值的数据类型，可以是基本数据类型，也可以是引用数据类型
​	如:

​	当返回的数据内容是66时，则返回值类型写int即可;

​	当返回的数据内容是3.14时，则返回值类型写double即可;

​	当返回的数据内容是"hel1o"时，则返回值类型写String即可

​	在方法体中使用return关键字来返回数据内容并结束当前方法。

​	如:
​	当返回的数据内容是66时，则方法体中写:return66;

​	当返回的数据内容是num时，则方法体中写:return num;

​	若该方法不需要返回任何数据内容，则返回值类型写void即可。

（2）形参列表

​	形式参数主要用于将方法体外的数据传入到方法体的内部，格式:数据类型 形参名。

​	形参列表主要指多个形式参数组成的整体，**格式如下:**

​	数据类型 形参名1，数据类型 形参名2，·······
​	当传入的数据内容是66时，则形参列表写为:int i即可;

​	当传入的数据内容是3.14时，则形参列表写为:double d即可:

​	当传入的数据内容是"he11o"时，则形参列表写为:string s即可;

​	当传入的数据内容是66和"he1lo"时，则形参列表写为:int i，String s即可;

​	若该方法不需要传入任何数据内容时，则形参列表位置啥也不写即可;

(3) 成员方法体

​	成员方法体主要编写描述该方法功能的语句。

​	如:
​	当该方法的功能就是打印时，则方法体中写 System.out.println("...");即可

​	当该方法的功能就是返回66时，则方法体中写return 66;即可

（4） 方法的调用

（1）语法格式

​	引用变量名:成员方法名(实参列表)

如：

show()           - 表示使用引用变量p调用show方法
(2)注意事项

a.实际参数列表主要用于对形式参数列表进行初始化操作，因此参数的个数、类型顺序等都必须与形参列表保持一致;

b.实参可以传递直接量、变量、表达式以及方法的调用等;

**Jvm内存结构-方法区**

该空间用于存放类的信息。Java程序运行时，首先会通过类装载器载入类文件的字节码信息，经过解析后将其装入方法区。在方法区保存类的各种信息

**Jvm内存结构-栈区**

栈用于存放程序运行过程当中所有的部变量一个运行的Java程序从开始到结束会有多次方法的调用。JVM会为每一个方法的调用在中分配一个对应的空间，这个空间称为该方法的栈帧。一个栈帧对应一个正在调用中的方法，栈帧中存储了该方法的参数、局部变量等数据。当某一个方法调用完成后，其对应的栈帧将被清除。

**Jvm内存结构-堆区**

JVM会在其内存空间中开辟一个称为“堆”的存储空间，这部分空间用于存储使用new关键字创建的对象。

# 9.Java的各种数据类型对象库的处理应用

#### 1.Object类

##### 1.1常用的包

java.lang包 - 该包是Java语言中的核心包，该包中的内容由Java虚拟机几自动导,如:String类、System类等

javá.util包 - 该包是Java语言中的工具包，里面包含了大量的工具类和集合类等一如:Scanner类、Random类等

java.io包  - 该包是Java语言中的输入输出包，里面包含了大量读写文件的类等如:File0utputStream类、FileInputStream类等

java.net包  - 该包是Java语言中的网络包，里面包含了大量网络编程的类等如:ServerSocket类、Socket类等
···········
**Java包的结构**

java.lang包 是Java最核心的包，JVM一启动自动加载这个包的所有类和接口无需impórt。常见的类:System/String/Object/Class/..
java.utit包 是Java的工具包，包括很多工具类和集合。
javá.io 包 是输入输出的包，包括读写各种设备。
javal.net包 是网络编程的包，包括各种网络编程。
javá.sql包 是操作数据的所有类和接口。
Java程序员在编程时，可以使用大量的类库，因此，Jayá编程需要的很多，对编程能力的本身要求不是特别的高。

##### 1.2基本概念

java.lang.0bject类是所有类层次结构的根类，任何类都是该类的直接或间接子类。

##### 1.3 常用的方法

0bject()-使用无参方式构造对象。
boolean equals(Object obj) - 用于判断调用对象是否与参数对象相等。
						该方法默认比较两个对象的地址，与==运算符结果相同

​						若该方法重写后，则应该重写hashCode方法来维护hashCode方法的常规协定

int hashCode()-用于获取调用对象的哈希码值(内存地址的编号)。	

​			-若调用equals方法的结果相等，则各自调用hashCode方法的结果相同

​			-若调用equals方法的结果不相等，则各自调用hashCode方法的结果不相同。

​			-为了维护上述的常规协定与equals方法结果保持一致，就需要重写该方法

String toString()-用于获取对象的字符串形式。
	该方法默认返回的字符串为:包名.类名@哈希码值的十六进制形式

​	为了返回更有意义的数据内容则需要重写该方法当字符串内容与引用进行连接时，自动调用toString方法

​	当使用print或print1n方法打印引用时，会自动调用toString法

##### 1.4.equals类

**基本概念**

在Java中，*Object*类的*equals()*方法用于比较两个对象是否相等。默认情况下，*equals()*方法比较的是两个对象的内存地址，即判断两个对象引用是否指向同一个对象

**语法**

```
object.equals(Object obj)
参数: obj - 要比较的对象。
返回值: 如果两个对象相等返回true，否则返回false。
```

**示例代码**

```
class RunoobTest {
public static void main(String[] args) {
// 创建两个对象
Object obj1 = new Object();
Object obj2 = new Object();

// 判断 obj1 与 obj2 是否相等
System.out.println(obj1.equals(obj2)); // false

// obj1 赋值给 obj3
Object obj3 = obj1;
System.out.println(obj1.equals(obj3)); // true
}
}
```

**重写equals**

在实际开发中，通常需要重写*equals()*方法，以便比较对象的内容而不是内存地址。例如，*String*类就重写了*equals()*方法，用于比较两个字符串的内容是否相等

以下是一个自定义类*Order*的示例，展示了如何重写*equals()*方法：

```
public class Order {
private int orderId;
private String orderName;

public Order(int orderId, String orderName) {
this.orderId = orderId;
this.orderName = orderName;
}

@Override
public boolean equals(Object obj) {
if (this == obj) {
return true;
}
if (obj instanceof Order) {
Order order = (Order) obj;
return this.orderId == order.orderId && this.orderName.equals(order.orderName);
}
return false;
}
```

#### 2.包装类和数学处理类

如：

Person p=new Person();	-声明Person类型的引用指向Person类型的对象

int num =10	声明一个int类型的变量num初始值为

Java语言是一门纯面向对象的编程语言

##### 2.1包装类的概念

​	Java语言是一门纯面向对象的编程语言，而8种基本数据类型声明的变量并不是对象，为了满足Java语言的特性就需要对这些变量进行对象化处理，而实现该功能的相关类就叫包装类。

##### 2.2包装类的分类

![image-20250706093012820](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250706093012820.png)

​	int =>java.lang.Integer类

​	char=>java.lang.Character类

​	其它类型对应的包装类就是将首字母变成大写

##### 2.3 Interger类

Integer(int value)-根据参数指定的整数构造对象

Integer(String s)  - 根据参数指定的字符串构造对象

该类重写了equals()、hashCode()、toString()方法

int intValue()-用于获取调用对象中的整数数据并返回。

static Integer value0f(int i）根据参数指定的整数返回对应的Integer对象。

static int parseInt(String s)-用于将String类型转换为int类型并返回。

#### 3.装箱和拆箱

- JDK5发布之前使用包装类对象进行运算时，需要较为繁琐的“拆箱”和“装箱”操作;即运算前先将包装类对象拆分为基本类型数据，运算后再将结果封装成包装类对象。

  Integer i=Integer.valueOf(100);

​	Integer j=Integer.valueOf(200);

​	Integer k=Integer.valueOf(i.intValue()+ j.intValue());

- “拆箱JDK5增加了自动(和“装箱”的功能。

​	Integer i= 100;

​	Integer j=200;

​	Integer k = i+j;
事实上JDK5的自动“拆箱”和“装箱”是依靠JDK5的编译器在编译器的“预处理”工作。

#### 3.BigDecimal类

**(1)基本概念**
由于float类型和double类型的运算可能会有误差，为了实现精确运算则需要借助java.math.BigDecimal类型加以描述。

**(2)常用的方法**

BigDecima?(String val)

​			-根据参数指定的字符串构造对象

BigDecimal add(BigDecimal augend)

​			-用于计算调用对象和参数对象的和并返回

BigDecimal subtract(BigDecimal subtrahend)

​			-用于计算调用对象和参数对象的差并返回

BigDecimal multiply(BigDecimal multiplicand)

​			-用于计算调用对象和参数对象的积并返回。

BigDecimal divide(BigDecimal divisor)

​			-用于计算调用对象和参数对象的商并返回

#### 4.String类

##### 4.1基本概念

​	java.lang.String类用于描述字符串，Java应用程序中所有字符串字面值都可以作为String类型的对象加以描述，如:"abc"等。

​	该类描述的字符串内容是个常量，一旦创建完毕后则不能更改，因此可以被共享。

如：

String strl = "abc";

String strl ="123";

##### 4.2 String类的特性

- java.lang.String用于封装字符串序列。

- Java字符串在内存中采用Unicode编码方式，任何一个字符对应两个字节的定长编码。
- String属于不可变类，即String对象一经创建后，其封装的字符串序列是不能改变的。

##### 4.3 常量池

​	由于String类型描述的字符串内容是个常量不可改变，因此Java虚拟机提供了一个常当Java程序中出现字符串内容时就放入常量池中，若后续出现重复的字符串内容则量池，直接使用池中已有的对象而不需再次创建，从而提高了性能。

**String类的构造方法**

| String()                                  | 使用无参构造对象得到控制符序列                              |
| ----------------------------------------- | ----------------------------------------------------------- |
| String(byte[]bytes,int offset,int length) | 使用bytes数组中下标从offset位置开始的length个字节来构造对象 |
| String(byte[] bytes)                      | 使用bytes数组中的所有内容来构造对象                         |

##### 4.4 String类的常用方法

| char charAt(int index) | 方法charAt用于返回字符串指定位置的字符，参数Index表示指定的位置 |
| ---------------------- | ------------------------------------------------------------ |
| int length()           | 返回字符串字符序列的长度                                     |

**charAt() 方法**用于返回指定索引处的字符。索引范围为从 0 到 length() - 1。

##### 语法

```
public char charAt(int index)
```

##### 实例

```
public class Test {
    public static void main(String args[]) {
        String s = "usahjsanfa";
        char result = s.charAt(6);
        System.out.println(result);
    }
}
```

![image-20250706103220460](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250706103220460.png)

##### equals() 方法

equals() 方法用于将字符串与指定的对象比较。

String 类中重写了 equals() 方法用于比较两个字符串的内容是否相等。

**语法**

```
public boolean equals(Object anObject)

```

示例

```
public class Test {
    public static void main(String args[]) {
        String Str1 = new String("runoob");
        String Str2 = Str1;
        String Str3 = new String("runoob");
        boolean retVal;

        retVal = Str1.equals( Str2 );
        System.out.println("返回值 = " + retVal );

        retVal = Str1.equals( Str3 );
        System.out.println("返回值 = " + retVal );
    }
}
```

```
String s1 = "Hello";              // String 直接创建
String s2 = "Hello";              // String 直接创建
String s3 = s1;                   // 相同引用
String s4 = new String("Hello");  // String 对象创建
String s5 = new String("Hello");  // String 对象创建
 
s1 == s1;         // true, 相同引用
s1 == s2;         // true, s1 和 s2 都在公共池中，引用相同
s1 == s3;         // true, s3 与 s1 引用相同
s1 == s4;         // false, 不同引用地址
s4 == s5;         // false, 堆中不同引用地址
 
s1.equals(s3);    // true, 相同内容
s1.equals(s4);    // true, 相同内容
s4.equals(s5);    // true, 相同内容String s1 = "Hello";              // String 直接创建
String s2 = "Hello";              // String 直接创建
String s3 = s1;                   // 相同引用
String s4 = new String("Hello");  // String 对象创建
String s5 = new String("Hello");  // String 对象创建
 
s1 == s1;         // true, 相同引用
s1 == s2;         // true, s1 和 s2 都在公共池中，引用相同
s1 == s3;         // true, s3 与 s1 引用相同
s1 == s4;         // false, 不同引用地址
s4 == s5;         // false, 堆中不同引用地址
 
s1.equals(s3);    // true, 相同内容
s1.equals(s4);    // true, 相同内容
s4.equals(s5);    // true, 相同内容
```

##### indexOf() 方法

- **public int indexOf(int ch):** 返回指定字符在字符串中第一次出现处的索引，如果此字符串中没有这样的字符，则返回 -1。
- **public int indexOf(int ch, int fromIndex):** 返回从 fromIndex 位置开始查找指定字符在字符串中第一次出现处的索引，如果此字符串中没有这样的字符，则返回 -1。
- **int indexOf(String str):** 返回指定字符在字符串中第一次出现处的索引，如果此字符串中没有这样的字符，则返回 -1。
- **int indexOf(String str, int fromIndex):** 返回从 fromIndex 位置开始查找指定字符在字符串中第一次出现处的索引，如果此字符串中没有这样的字符，则返回 -1。

​	**语法**

```
public int indexOf(int ch )

或

public int indexOf(int ch, int fromIndex)

或

int indexOf(String str)

或

int indexOf(String str, int fromIndex)

```

**参数**

- **ch** -- 字符，Unicode 编码。
- **fromIndex** -- 开始搜索的索引位置，第一个字符是 0 ，第二个是 1 ，以此类推。
- **str** -- 要搜索的子字符串。

示例

```
public class Main {
    public static void main(String args[]) {
        String string = "aaa456ac";  
        //查找指定字符是在字符串中的下标。在则返回所在字符串下标；不在则返回-1.  
        System.out.println(string.indexOf("b")); // indexOf(String str); 返回结果：-1，"b"不存在  
 
        // 从第四个字符位置开始往后继续查找，包含当前位置  
        System.out.println(string.indexOf("a",3));//indexOf(String str, int fromIndex); 返回结果：6  
 
        //（与之前的差别：上面的参数是 String 类型，下面的参数是 int 类型）参考数据：a-97,b-98,c-99  
 
        // 从头开始查找是否存在指定的字符  
        System.out.println(string.indexOf(99));//indexOf(int ch)；返回结果：7  
        System.out.println(string.indexOf('c'));//indexOf(int ch)；返回结果：7  
 
        //从fromIndex查找ch，这个是字符型变量，不是字符串。字符a对应的数字就是97。  
        System.out.println(string.indexOf(97,3));//indexOf(int ch, int fromIndex); 返回结果：6  
        System.out.println(string.indexOf('a',3));//indexOf(int ch, int fromIndex); 返回结果：6  
    }
}
```

指定子字符串在字符串中第一次出现处的索引，从指定的索引开始。

```
public class Test {
    public static void main(String args[]) {
        String Str = new String("66666666");
        String SubStr1 = new String("6478856666");
        String SubStr2 = new String("com");
 
        System.out.print("查找字符 o 第一次出现的位置 :" );
        System.out.println(Str.indexOf( 'o' ));
        System.out.print("从第14个位置查找字符 o 第一次出现的位置 :" );
        System.out.println(Str.indexOf( 'o', 14 ));
        System.out.print("子字符串 SubStr1 第一次出现的位置:" );
        System.out.println( Str.indexOf( SubStr1 ));
        System.out.print("从第十五个位置开始搜索子字符串 SubStr1 第一次出现的位置 :" );
        System.out.println( Str.indexOf( SubStr1, 15 ));
        System.out.print("子字符串 SubStr2 第一次出现的位置 :" );
        System.out.println(Str.indexOf( SubStr2 ));
    }
}
```

##### substring() 方法

substring() 方法返回字符串的子字符串。

**语法**

```
public String substring(int beginIndex)

或

public String substring(int beginIndex, int endIndex)

```

**参数**	

- **beginIndex** -- 起始索引（包括）, 索引从 0 开始。
- **endIndex** -- 结束索引（不包括）。

示例

```
public class RunoobTest {
    public static void main(String args[]) {
        String Str = new String("This is text");
 
        System.out.print("返回值 :" );
        System.out.println(Str.substring(4) );
 
        System.out.print("返回值 :" );
        System.out.println(Str.substring(4, 10) );
    }
}
```

##### Java StringBuffer 和 StringBuilder 类

当对字符串进行修改的时候，需要使用 StringBuffer 和 StringBuilder 类。

和 String 类不同的是，StringBuffer 和 StringBuilder 类的对象能够被多次的修改，并且不产生新的未使用对象。

![image-20250706104135502](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250706104135502.png)

在使用 StringBuffer 类时，每次都会对 StringBuffer 对象本身进行操作，而不是生成新的对象，所以如果需要对字符串进行修改推荐使用 StringBuffer。

StringBuilder 类在 Java 5 中被提出，它和 StringBuffer 之间的最大不同在于 StringBuilder 的方法不是线程安全的（不能同步访问）。

由于 StringBuilder 相较于 StringBuffer 有速度优势，所以多数情况下建议使用 StringBuilder 类。

示例

```
public class RunoobTest{
    public static void main(String[] args){
        StringBuilder sb = new StringBuilder(10);
        sb.append("Runoob..");
        System.out.println(sb);  
        sb.append("!");
        System.out.println(sb); 
        sb.insert(8, "Java");
        System.out.println(sb); 
        sb.delete(5,8);
        System.out.println(sb);  
    }
}
```

以下是 StringBuffer 类支持的主要方法：

| 序号 | 方法描述                                                     |
| :--- | :----------------------------------------------------------- |
| 1    | public StringBuffer append(String s) 将指定的字符串追加到此字符序列。 |
| 2    | public StringBuffer reverse()  将此字符序列用其反转形式取代。 |
| 3    | public delete(int start, int end) 移除此序列的子字符串中的字符。 |
| 4    | public insert(int offset, int i) 将 `int` 参数的字符串表示形式插入此序列中。 |
| 5    | insert(int offset, String str) 将 `str` 参数的字符串插入此序列中。 |
| 6    | replace(int start, int end, String str) 使用给定 `String` 中的字符替换此序列的子字符串中的字符。 |

以下列表列出了 StringBuffer 类的其他常用方法：

| 序号 | 方法描述                                                     |
| :--- | :----------------------------------------------------------- |
| 1    | int capacity() 返回当前容量。                                |
| 2    | char charAt(int index) 返回此序列中指定索引处的 `char` 值。  |
| 3    | void ensureCapacity(int minimumCapacity) 确保容量至少等于指定的最小值。 |
| 4    | void getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin) 将字符从此序列复制到目标字符数组 `dst`。 |
| 5    | int indexOf(String str) 返回第一次出现的指定子字符串在该字符串中的索引。 |
| 6    | int indexOf(String str, int fromIndex) 从指定的索引处开始，返回第一次出现的指定子字符串在该字符串中的索引。 |
| 7    | int lastIndexOf(String str) 返回最右边出现的指定子字符串在此字符串中的索引。 |
| 8    | int lastIndexOf(String str, int fromIndex) 返回 String 对象中子字符串最后出现的位置。 |
| 9    | int length()  返回长度（字符数）。                           |
| 10   | void setCharAt(int index, char ch) 将给定索引处的字符设置为 `ch`。 |
| 11   | void setLength(int newLength) 设置字符序列的长度。           |
| 12   | CharSequence subSequence(int start, int end) 返回一个新的字符序列，该字符序列是此序列的子序列。 |
| 13   | String substring(int start) 返回一个新的 `String`，它包含此字符序列当前所包含的字符子序列。 |
| 14   | String substring(int start, int end) 返回一个新的 `String`，它包含此序列当前所包含的字符子序列。 |
| 15   | String toString() 返回此序列中数据的字符串表示形式。         |

**StringBuilder实现增删改查**

```
public class stringBuilderDemo {

public static void main(String[] args) {

String line ="今天学习Java感觉如何？";
StringBuilder builder =new StringBuilder(line);

/*
*今天学习Java感觉如何？真是神清气爽
*/
builder.append("真是神清气爽");//增加在原有基础上增加字符
line=builder.toString();
System.out.println(line);

/*
* 今天学习Java感觉如何？真是神清气爽
* 今天学习Java感觉如何？呼吸都顺畅了
*/
builder.replace(13, 19, "呼吸都顺畅了");//替换 真是神清气爽 为 呼吸都顺畅了
line=builder.toString();
System.out.println(line);
/*
* 今天学习Java感觉如何？呼吸都顺畅了
* 呼吸都顺畅了
*/
builder.delete(0, 13);//删除 今天学习Java感觉如何？
line = builder.toString();
System.out.println(line);

/*
* 呼吸都顺畅了
* 打开窗户,
*/
builder.insert(0, "打开窗户,");//在某个位子插入
line = builder.toString();
System.out.println(line);
}

}
```

**stringbuilder类实现反转和相互转换**

```
public class StringDemo {
public static void main(String[] args) {
// 创建一个StringBuilder对象，并传入一个字符串
StringBuilder str = new StringBuilder("HelloWorld");

// 打印原始字符串
System.out.println("原始字符串: " + str.toString());

// 使用reverse()方法反转字符串
StringBuilder reversedStr = str.reverse();

// 打印反转后的字符串
System.out.println("反转后的字符串: " + reversedStr.toString());
}
}
```

#### 5.date类的概念和常用方法

5.1**概述**

`java.util.Date`类表示特定的瞬间，精确到毫秒。Date类的构造函数可以把**毫秒值转成日期对象**。

**5.2 Date类构造方法**

- public Date()：分配Date对象并初始化此对象，以表示分配它的时间（精确到毫秒）。
- public Date(long date)：分配Date对象并初始化此对象，以表示自从标准基准时间（称为“历元（epoch）”，即1970年1月1日00:00:00 GMT）以来的指定毫秒数。

简单来说：使用无参构造，可以自动设置当前系统时间的毫秒时刻；指定long类型的构造参数，可以自定义毫秒时刻。例如：

```
import java.util.Date;

public class DemoDate {
    public static void main(String[] args) {
        // 创建日期对象，把当前的时间转成日期对象
        System.out.println(new Date()); // Sat Sep 19 23:11:21 CST 2020
        // 创建日期对象，把当前的毫秒值转成日期对象
        System.out.println(new Date(0L)); // Thu Jan 01 08:00:00 CST 1970
    }
}

```

##### 5.3 Date类的getTime方法：返回毫秒数

**DateFormat类**
java.text.DateFormat 是日期/时间格式化子类的抽象类，我们通过这个类可以帮我们完成日期和文本之间的转换,也就是可以在Date对象与String对象之间进行来回转换。

- 格式化：按照指定的格式，从Date对象转换为String对象。(format)
- 解析：按照指定的格式，从String对象转换为Date对象。(parse)

##### 子类SimpleDateFormat的构造方法

由于DateFormat为抽象类，不能直接使用，所以需要常用的子类java.text.SimpleDateFormat。这个类需要一个模式（格式）来指定格式化或解析的标准。构造方法为：

- public SimpleDateFormat(String pattern)：用给定的模式和默认语言环境的日期格式符号构造SimpleDateFormat。


参数pattern是一个字符串，代表日期时间的自定义格式。

常用的格式规则为：

| 标识字母（区分大小写） | 含义 |
| ---------------------- | ---- |
| y                      | 年   |
| M                      | 月   |
| d                      | 日   |
| H                      | 时   |
| m                      | 分   |
| s                      | 秒   |

创建SimpleDateFormat对象的代码如：

```
import java.text.DateFormat;
import java.text.SimpleDateFormat;

public class Demo02SimpleDateFormat {
    public static void main(String[] args) {
        // 对应的日期格式如：2018-01-16 15:06:38
        DateFormat format = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
    }    
}

```

##### DateFormat类常用方法

使用format方法的代码为：

```
import java.text.DateFormat;
import java.text.SimpleDateFormat;
import java.util.Date;
/*
 把Date对象转换成String
*/
public class Demo03DateFormatMethod {
    public static void main(String[] args) {
        Date date = new Date();
        // 创建日期格式化对象,在获取格式化对象时可以指定风格
        DateFormat df = new SimpleDateFormat("yyyy年MM月dd日");
        String str = df.format(date);
        System.out.println(str); // 2020年09月19日
    }
}

```

#####  parse方法

使用parse方法的代码为：

```
import java.text.DateFormat;
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;
/*
 把String转换成Date对象
*/
public class Demo04DateFormatMethod {
    public static void main(String[] args) throws ParseException {
        DateFormat df = new SimpleDateFormat("yyyy年MM月dd日");
        String str = "2018年12月11日";
        Date date = df.parse(str);
        System.out.println(date); // Tue Dec 11 00:00:00 CST 2018
    }
}

```

#### 综合练习

**题目**：请使用日期时间相关的API，计算出一个人已经出生了多少天。

**思路：**

1.获取当前时间对应的毫秒值

2.获取自己出生日期对应的毫秒值

3.两个时间相减（当前时间– 出生日期）

```
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.Scanner;

/*
 把String转换成Date对象
*/
public class Demo {
    public static void main(String[] args) throws ParseException {
        System.out.println("请输入出生日期 格式 YYYY-MM-dd");
        // 获取出生日期,键盘输入
        String birthdayString = new Scanner(System.in).next();
        // 将字符串日期,转成Date对象
        // 创建SimpleDateFormat对象,写日期模式
        SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
        // 调用方法parse,字符串转成日期对象
        Date birthdayDate = sdf.parse(birthdayString);
        // 获取今天的日期对象
        Date todayDate = new Date();
        // 将两个日期转成毫秒值,Date类的方法getTime
        long birthdaySecond = birthdayDate.getTime();
        long todaySecond = todayDate.getTime();
        long secone = todaySecond-birthdaySecond;
        if (secone < 0){
            System.out.println("还没出生呢");
        } else {
            System.out.println(secone/1000/60/60/24);
        }
    }
}

```

#### 6 Calendar类

**6.1 概念**
	java.util.Calendar是日历类，在Date后出现，替换掉了许多Date的方法。该类将所有可能用到的时间信息封装为静态成员变量，方便获取。日历类就是方便获取各个时间属性的。

**6.2 获取方式**
	Calendar为抽象类，由于语言敏感性，Calendar类在创建对象时并非直接创建，而是通过静态方法创建，返回子类对象，如下：

Calendar静态方法

public static Calendar getInstance()：使用默认时区和语言环境获得一个日历
例如：

```
import java.util.Calendar;

public class Demo06CalendarInit {
    public static void main(String[] args) {
        Calendar cal = Calendar.getInstance();
    }    
}

```

**6.3 常用方法**
根据Calendar类的API文档，常用方法有：

- public int get(int field)：返回给定日历字段的值。

- public void set(int field, int value)：将给定的日历字段设置为给定值。
- public abstract void add(int field, int amount)：根据日历的规则，为给定的日历字段添加或减去指定的时间量。
- public Date getTime()：返回一个表示此Calendar时间值（从历元到现在的毫秒偏移量）的Date对象。

Calendar类中提供很多成员常量，代表给定的日历字段：

| 字段值       | 含义                                  |
| ------------ | ------------------------------------- |
| YEAR         | 年                                    |
| MONTH        | 月（从0开始，可以+1使用）             |
| DAY_OF_MONTH | 月中的天（几号）                      |
| HOUR         | 时（12小时制）                        |
| HOUR_OF_DAY  | 时（24小时制）                        |
| MINUTE       | 分                                    |
| SECOND       | 秒                                    |
| DAY_OF_WEEK  | 周中的天（周几，周日为1，可以-1使用） |

##### get/set方法

get方法用来获取指定字段的值，set方法用来设置指定字段的值，代码使用演示：

```
import java.util.Calendar;
public class Demo {
    public static void main(String[] args) {
        // 创建Calendar对象
        Calendar cal = Calendar.getInstance();
        // 获取年 
        int year = cal.get(Calendar.YEAR);
        // 获取月
        int month = cal.get(Calendar.MONTH) + 1;
        // 获取日
        int dayOfMonth = cal.get(Calendar.DAY_OF_MONTH);
        System.out.print(year + "年" + month + "月" + dayOfMonth + "日");
    }
}

```

```
import java.util.Calendar;

public class Demo07CalendarMethod {
    public static void main(String[] args) {
        Calendar cal = Calendar.getInstance();
        // 设置年
        cal.set(Calendar.YEAR, 2018);
        // 获取年
        int year = cal.get(Calendar.YEAR);
        // 获取月
        int month = cal.get(Calendar.MONTH) + 1;
        // 获取日
        int dayOfMonth = cal.get(Calendar.DAY_OF_MONTH);
        System.out.print(year + "年" + month + "月" + dayOfMonth + "日");
    }
}

```

##### add方法

add方法可以对指定日历字段的值进行加减操作，如果第二个参数为正数则加上偏移量，如果为负数则减去偏移量。代码如：

```
import java.util.Calendar;

public class Demo08CalendarMethod {
    public static void main(String[] args) {
        Calendar cal = Calendar.getInstance();
        // 获取年
        int year = cal.get(Calendar.YEAR);
        // 获取月
        int month = cal.get(Calendar.MONTH) + 1;
        // 获取日
        int dayOfMonth = cal.get(Calendar.DAY_OF_MONTH);
        System.out.println(year + "年" + month + "月" + dayOfMonth + "日");
        // 使用add方法
        cal.add(Calendar.DAY_OF_MONTH, 2); // 加2天
        cal.add(Calendar.YEAR, -3); // 减3年
        // 获取年
        year = cal.get(Calendar.YEAR);
        // 获取月
        month = cal.get(Calendar.MONTH) + 1;
        // 获取日
        dayOfMonth = cal.get(Calendar.DAY_OF_MONTH);
        System.out.println(year + "年" + month + "月" + dayOfMonth + "日");
    }
}

```

##### getTime方法：返回对应的Date对象

Calendar中的getTime方法并不是获取毫秒时刻，而是拿到对应的Date对象。

```
import java.util.Calendar;
import java.util.Date;

public class Demo {
    public static void main(String[] args) {
        Calendar cal = Calendar.getInstance();
        Date date = cal.getTime();
        System.out.println(date); 
    }
}

```

# 10.包装类、集合、数据结构

#### 1.集合(容器)框架

​	在Java语言中集合框架的顶层是:java.uti1.Collection集合 和 java.util.Map集合其中Co1lection集合中操作元素的基本单位是:单个元素。其中Map集合中操作元素的基本单位是:单对元素。

#### 集合接口

集合框架定义了一些接口。本节提供了每个接口的概述：

| 序号 | 接口描述                                                     |
| :--- | :----------------------------------------------------------- |
| 1    | Collection 接口 Collection 是最基本的集合接口，一个 Collection 代表一组 Object，即 Collection 的元素, Java不提供直接继承自Collection的类，只提供继承于的子接口(如List和set)。Collection 接口存储一组不唯一，无序的对象。 |
| 2    | List 接口 List接口是一个有序的 Collection，使用此接口能够精确的控制每个元素插入的位置，能够通过索引(元素在List中位置，类似于数组的下标)来访问List中的元素，第一个元素的索引为 0，而且允许有相同的元素。List 接口存储一组不唯一，有序（插入顺序）的对象。 |
| 3    | Set Set 具有与 Collection 完全一样的接口，只是行为上不同，Set 不保存重复的元素。Set 接口存储一组唯一，无序的对象。 |
| 4    | SortedSet 继承于Set保存有序的集合。                          |
| 5    | Map Map 接口存储一组键值对象，提供key（键）到value（值）的映射。 |
| 6    | Map.Entry 描述在一个Map中的一个元素（键/值对）。是一个 Map 的内部接口。 |
| 7    | SortedMap 继承于 Map，使 Key 保持在升序排列。                |
| 8    | Enumeration 这是一个传统的接口和定义的方法，通过它可以枚举（一次获得一个）对象集合中的元素。这个传统接口已被迭代器取代。 |

##### 集合实现类（集合类）

​	Java提供了一套实现了Collection接口的标准集合类。其中一些是具体类，这些类可以直接拿来使用，而另外一些是抽象类，提供了接口的部分实现。

标准集合类汇总于下表：

| 序号 | 类描述                                                       |
| :--- | :----------------------------------------------------------- |
| 1    | **AbstractCollection**  实现了大部分的集合接口。             |
| 2    | **AbstractList**  继承于AbstractCollection 并且实现了大部分List接口。 |
| 3    | **AbstractSequentialList**  继承于 AbstractList ，提供了对数据元素的链式访问而不是随机访问。 |
| 4    | LinkedList 该类实现了List接口，允许有null（空）元素。主要用于创建链表数据结构，该类没有同步方法，如果多个线程同时访问一个List，则必须自己实现访问同步，解决方法就是在创建List时候构造一个同步的List。例如：`List list=Collections.synchronizedList(newLinkedList(...));`LinkedList 查找效率低。 |
| 5    | ArrayList 该类也是实现了List的接口，实现了可变大小的数组，随机访问和遍历元素时，提供更好的性能。该类也是非同步的,在多线程的情况下不要使用。ArrayList 增长当前长度的50%，插入删除效率低。 |
| 6    | **AbstractSet**  继承于AbstractCollection 并且实现了大部分Set接口。 |
| 7    | HashSet 该类实现了Set接口，不允许出现重复元素，不保证集合中元素的顺序，允许包含值为null的元素，但最多只能一个。 |
| 8    | LinkedHashSet 具有可预知迭代顺序的 `Set` 接口的哈希表和链接列表实现。 |
| 9    | TreeSet 该类实现了Set接口，可以实现排序等功能。              |
| 10   | **AbstractMap**  实现了大部分的Map接口。                     |
| 11   | HashMap HashMap 是一个散列表，它存储的内容是键值对(key-value)映射。 该类实现了Map接口，根据键的HashCode值存储数据，具有很快的访问速度，最多允许一条记录的键为null，不支持线程同步。 |
| 12   | TreeMap 继承了AbstractMap，并且使用一颗树。                  |
| 13   | WeakHashMap 继承AbstractMap类，使用弱密钥的哈希表。          |
| 14   | LinkedHashMap 继承于HashMap，使用元素的自然顺序对元素进行排序. |
| 15   | IdentityHashMap 继承AbstractMap类，比较文档时使用引用相等。  |

在前面的教程中已经讨论通过java.util包中定义的类，如下所示：

| 序号 | 类描述                                                       |
| :--- | :----------------------------------------------------------- |
| 1    | Vector 该类和ArrayList非常相似，但是该类是同步的，可以用在多线程的情况，该类允许设置默认的增长长度，默认扩容方式为原来的2倍。 |
| 2    | Stack 栈是Vector的一个子类，它实现了一个标准的后进先出的栈。 |
| 3    | Dictionary Dictionary 类是一个抽象类，用来存储键/值对，作用和Map类相似。 |
| 4    | Hashtable Hashtable 是 Dictionary(字典) 类的子类，位于 java.util 包中。 |
| 5    | Properties Properties 继承于 Hashtable，表示一个持久的属性集，属性列表中每个键及其对应值都是一个字符串。 |
| 6    | BitSet 一个Bitset类创建一种特殊类型的数组来保存位值。BitSet中数组大小会随需要增加。 |

##### 集合算法

集合框架定义了几种算法，可用于集合和映射。这些算法被定义为集合类的静态方法。

在尝试比较不兼容的类型时，一些方法能够抛出 ClassCastException异常。当试图修改一个不可修改的集合时，抛出UnsupportedOperationException异常。

集合定义三个静态的变量：EMPTY_SET，EMPTY_LIST，EMPTY_MAP的。这些变量都不可改变。

| 序号 | 算法描述                                               |
| :--- | :----------------------------------------------------- |
| 1    | Collection Algorithms 这里是一个列表中的所有算法实现。 |
|      |                                                        |

##### 如何使用迭代器

通常情况下，你会希望遍历一个集合中的元素。例如，显示集合中的每个元素。

一般遍历数组都是采用for循环或者增强for，这两个方法也可以用在集合框架，但是还有一种方法是采用迭代器遍历集合框架，它是一个对象，实现了Iterator接口或 ListIterator接口。

迭代器，使你能够通过循环来得到或删除集合的元素。ListIterator 继承了 Iterator，以允许双向遍历列表和修改元素。

##### 遍历 ArrayList

```
import java.util.*;
 
public class Test{
 public static void main(String[] args) {
     List<String> list=new ArrayList<String>();
     list.add("Hello");
     list.add("World");
     list.add("HAHAHAHA");
     //第一种遍历方法使用 For-Each 遍历 List
     for (String str : list) {            //也可以改写 for(int i=0;i<list.size();i++) 这种形式
        System.out.println(str);
     }
 
     //第二种遍历，把链表变为数组相关的内容进行遍历
     String[] strArray=new String[list.size()];
     list.toArray(strArray);
     for(int i=0;i<strArray.length;i++) //这里也可以改写为  for(String str:strArray) 这种形式
     {
        System.out.println(strArray[i]);
     }
     
    //第三种遍历 使用迭代器进行相关遍历
     
     Iterator<String> ite=list.iterator();
     while(ite.hasNext())//判断下一个元素之后有值
     {
         System.out.println(ite.next());
     }
 }
}
```

**解析：**

三种方法都是用来遍历ArrayList集合，第三种方法是采用迭代器的方法，该方法可以不用担心在遍历的过程中会超出集合的长度。

##### 遍历 Map

```
import java.util.*;
 
public class Test{
     public static void main(String[] args) {
      Map<String, String> map = new HashMap<String, String>();
      map.put("1", "value1");
      map.put("2", "value2");
      map.put("3", "value3");
      
      //第一种：普遍使用，二次取值
      System.out.println("通过Map.keySet遍历key和value：");
      for (String key : map.keySet()) {
       System.out.println("key= "+ key + " and value= " + map.get(key));
      }
      
      //第二种
      System.out.println("通过Map.entrySet使用iterator遍历key和value：");
      Iterator<Map.Entry<String, String>> it = map.entrySet().iterator();
      while (it.hasNext()) {
       Map.Entry<String, String> entry = it.next();
       System.out.println("key= " + entry.getKey() + " and value= " + entry.getValue());
      }
      
      //第三种：推荐，尤其是容量大时
      System.out.println("通过Map.entrySet遍历key和value");
      for (Map.Entry<String, String> entry : map.entrySet()) {
       System.out.println("key= " + entry.getKey() + " and value= " + entry.getValue());
      }
    
      //第四种
      System.out.println("通过Map.values()遍历所有的value，但不能遍历key");
      for (String v : map.values()) {
       System.out.println("value= " + v);
      }
     }
}
```

##### 如何使用比较器

TreeSet和TreeMap的按照排序顺序来存储元素. 然而，这是通过比较器来精确定义按照什么样的排序顺序。

这个接口可以让我们以不同的方式来排序一个集合。

| 序号 | 比较器方法描述                                               |
| :--- | :----------------------------------------------------------- |
| 1    | 使用 Java Comparator 这里通过实例列出Comparator接口提供的所有方法 |

**ArrayList和LinkedList区别详解以及使用场景。**
**ArrayList：**
底层数据结构：ArrayList基于动态数组实现，内部维护一个Object数组，默认初始容量为10，当元素数量超过当前容量时会自动扩容。
随机访问效率高：由于基于数组，ArrayList支持通过索引快速访问元素，时间复杂度为O(1)。
插入和删除效率低：在中间或开头插入/删除元素时，需要移动后续元素，时间复杂度为O(n)。
适合随机访问：对于频繁随机访问元素的场景，ArrayList性能更好。
**LinkedList：**
底层数据结构：LinkedList基于双向链表实现，每个节点包含数据元素和指向前后节点的引用。
插入和删除效率高：在任意位置插入/删除元素时，只需调整相邻节点的引用，时间复杂度为O(1)。
顺序访问效率低：由于基于链表，LinkedList不支持随机访问，需要从头或尾开始遍历，时间复杂度为O(n)。
适合频繁插入和删除：对于频繁插入和删除元素的场景，LinkedList性能更好。
**总结：**
如果需要频繁进行随机访问操作，应选择ArrayList。
如果需要频繁进行插入和删除操作而访问操作较少，应选择LinkedList。
在需要同时进行大量随机访问和插入删除操作时，可以根据具体场景进行权衡选择。
综上所述，ArrayList适合随机访问，LinkedList适合插入和删除操作。根据具体需求和操作特点选择合适的集合类可以提高程序性能。

**特殊情况：**
**头插法插入数据：**
**ArrayList：**使用头插法插入数据时，需要将已有元素依次向后移动，因为ArrayList在中间或开头插入元素的时间复杂度为O(n)，效率较低。
**LinkedList：**LinkedList在头部插入元素时效率较高，只需要调整指针即可，时间复杂度为O(1)。
由于LinkedList在头部插入元素时效率更高，因此使用头插法插入数据时，应该选择LinkedList。

尾插法插入数据：
**ArrayList：**使用尾插法插入数据时，由于ArrayList在末尾添加元素的时间复杂度为O(1)，效率较高。
**LinkedList：**LinkedList在末尾插入元素时也需要调整指针，但时间复杂度也为O(1)。
对于尾插法插入数据，无论是ArrayList还是LinkedList都能够以较高的效率进行插入操作。

综上所述，使用头插法插入数据时应选择LinkedList，而使用尾插法插入数据时，ArrayList和LinkedList都可以达到较高的效率。



#### Vector和Stack的区别

**Vector**和**Stack**是Java集合框架中的两个重要类，它们在数据存储和操作上有不同的特点和用途。

定义和基本功能

**Vector**是一个动态数组，实现了List接口，可以自动扩容。它允许在任意位置插入、删除和访问元素

```
import java.util.Vector;

public class Main {
public static void main(String[] args) {
Vector<Integer> vector = new Vector<>();
vector.add(1);
vector.add(2);
vector.add(3);
System.out.println("Vector: " + vector);
}
}
```

**Stack**是Vector的子类，实现了栈的数据结构。栈是一种后进先出（LIFO）的数据结构，只能在栈顶进行插入和删除操作。例如：

```
import java.util.Stack;

public class Main {
public static void main(String[] args) {
Stack<Integer> stack = new Stack<>();
stack.push(1);
stack.push(2);
stack.push(3);
System.out.println("Stack: " + stack);
System.out.println("Pop element from stack: " + stack.pop());
System.out.println("Stack after pop: " + stack);
}
}
```

**实现原理**

**Vector**内部使用一个Object类型的数组来存储元素，当数组空间不足时，会创建一个更大的数组并将所有元素复制到新数组中，这个过程称为扩容。

**Stack**继承自Vector，所以它也使用数组来存储元素。与Vector不同的是，Stack限制了只能在栈顶进行插入和删除操作。

**优缺点**

**Vector**的优点是具有动态扩容功能，可以自动调整大小以适应可变数量的元素，支持在任意位置插入、删除和访问元素。缺点是由于内部使用数组来存储元素，在插入或删除元素时，可能需要移动其他元素的位置，导致性能下降。此外，Vector是线程安全的，但在多线程环境下使用时会带来额外的开销。

**Stack**的优点是继承自Vector，提供了栈的特性，方便实现后进先出的数据结构。缺点是由于继承自Vector，Stack也具有与Vector相同的缺点。另外，栈的大小是固定的，当栈满时无法再插入新的元素。

**使用注意事项**

在Java中，推荐使用ArrayList代替Vector，因为ArrayList不是线程安全的，并且性能更好。在实现后进先出的数据结构时，可以考虑使用Deque接口的实现类LinkedList，它既支持栈操作，又支持队列操作。

**总结**

**Vector**和**Stack**都是Java集合框架中的一部分，用于存储和操作可变数量的元素。Vector是一个动态数组，而Stack是Vector的子类，实现了栈的数据结构。在某些场景下，Vector和Stack非常有用，但在大多数情况下，推荐使用ArrayList或LinkedList来代替它们。

#### List集合的增删改查

##### 1.List集合的增删改查以及遍历删除问题

```
package com.zhongshun.list;
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

/**
 * List集合的增删改查和遍历集合删除的问题
 * @author zjjt
 *
 */
public class Demo {
	public static void main(String[] args) {
		//实例化一个list集合
		List<String> list = new ArrayList<>();
//	     增加list数组     往list集合添加数据   
		list.add("张三");
		list.add("李四");
		list.add("王五");
		list.add("老六");
//	删除list里面的数据
		//第一种  通过下标删除
		list.remove(0);
		System.out.println(list);
		//第二种  通过数据内容删除
		list.remove("张三");
		System.out.println(list);
//		修改  list数组  通过下标修改属性值
		list.set(0,"潘子"); //第一个值是数组下标 第二是要修改的
		System.out.println(list);
//		遍历list数组
		//第一种 for循环
		for (int i = 0; i < list.size(); i++) {
			System.out.println(list.get(i));
		}
		//第二种 foreach  增强的for循环
		for (String sa : list) {
			System.out.println(sa);
		}
		//第三种  迭代器
		Iterator<String> sa = list.iterator();
//		System.out.println(sa.hasNext()); //下一行，是否还有数据
//		System.out.println(sa.next());//下一行的数据
		while(sa.hasNext()) {//判断下一行是否还有数据
			System.out.println(sa.next());//打印出下一行的数据
		}
		//面试题经常问到的 最后list集合剩下什么元素？为什么？
		//  会爆错  在遍历list集合的时候是不能进行增删的
		for (String s : list) {
			if("张三".equals(s)) {
				list.remove(s);
			}
		}
		
	}
}

```

**List集合去重**

```
package com.zhongshun.list;

import java.util.ArrayList;
import java.util.List;

/**
 * list去重
 * 底层是是重写eq方法来执行去重元素
 * @author zjjt
 *
 */
public class Demo03 {

	public static void main(String[] args) {
		
		List<String> list = new ArrayList<>();
		list.add("张三");
		list.add("李四");
		list.add("张三");
		
		System.out.println(list);
		
		
		List<String> listNew = new ArrayList<>();//定义一个新list集合
		for (String sa : listNew) {
			if(!listNew.contains(sa)) {//判断新集合是否存在该数据不存在则往新集合里面加
				listNew.add(sa);
			}
		}
		//进行去重后的List集合
		System.out.println(listNew);
	
	}
}
```

#### 泛型的基本概念

##### 1. 什么是泛型？

泛型是 Java SE 5 引入的一种特性，它允许我们在编译时指定类型参数，从而避免在运行时进行类型转换和类型检查。泛型的本质是在编译时进行类型检查，确保类型安全。

##### 2. 为什么使用泛型？

在没有泛型之前，我们通常使用 `Object` 类型来表示集合中的元素，然后在使用时进行类型转换。这种方式容易导致类型转换异常和代码不安全。泛型的引入解决了这些问题，它可以在编译时进行类型检查，避免类型转换异常，提高代码的安全性和可读性。

#### 二、泛型的基本用法

##### 1. 泛型类

泛型类是在类定义时使用类型参数的类。例如，`ArrayList` 是一个泛型类，它可以存储任意类型的对象。

###### 示例代码

```
import java.util.ArrayList;

public class GenericClassExample {
    public static void main(String[] args) {
        // 创建一个泛型类的实例
        ArrayList<String> list = new ArrayList<>();
        // 添加元素
        list.add("Hello");
        list.add("World");
        // 遍历元素
        for (String s : list) {
            System.out.println(s);
        }
    }
}

```

##### 2. 泛型接口

泛型接口是在接口定义时使用类型参数的接口。例如，`Comparable` 是一个泛型接口，它可以用于定义对象的排序规则。

##### 示例代码

```
import java.util.ArrayList;
import java.util.Collections;

public class GenericInterfaceExample {
    public static void main(String[] args) {
        // 创建一个泛型接口的实现类
        ArrayList<String> list = new ArrayList<>();
        list.add("Banana");
        list.add("Apple");
        list.add("Cherry");
        // 排序
        Collections.sort(list);
        // 遍历元素
        for (String s : list) {
            System.out.println(s);
        }
    }
}

```

##### 3. 泛型方法

泛型方法是在方法定义时使用类型参数的方法。例如，`Arrays.asList` 是一个泛型方法，它可以将数组转换为列表。

###### 示例代码

```
import java.util.Arrays;
import java.util.List;

public class GenericMethodExample {
    public static void main(String[] args) {
        // 创建一个数组
        String[] array = {"Hello", "World"};
        // 使用泛型方法将数组转换为列表
        List<String> list = Arrays.asList(array);
        // 遍历元素
        for (String s : list) {
            System.out.println(s);
        }
    }
}

```

#### 三、通配符

在使用泛型时，我们有时需要处理未知类型的集合。这时可以使用通配符 `?` 来表示未知类型。

##### 1. 无界通配符

无界通配符 `?` 表示未知类型，可以用于读取集合中的元素，但不能用于添加元素。

###### 示例代码

```
import java.util.ArrayList;

public class WildcardExample {
    public static void main(String[] args) {
        // 创建一个泛型类的实例
        ArrayList<String> list = new ArrayList<>();
        list.add("Hello");
        list.add("World");
        // 使用无界通配符读取元素
        printList(list);
    }

    public static void printList(List<?> list) {
        for (Object s : list) {
            System.out.println(s);
        }
    }
}

```

##### 2. 有界通配符

有界通配符 `? extends T` 表示未知类型是 `T` 或 `T` 的子类，`? super T` 表示未知类型是 `T` 或 `T` 的父类。

###### 示例代码

```
import java.util.ArrayList;

public class BoundedWildcardExample {
    public static void main(String[] args) {
        // 创建一个泛型类的实例
        ArrayList<Animal> list = new ArrayList<>();
        list.add(new Dog());
        list.add(new Cat());
        // 使用有界通配符读取元素
        printList(list);
    }

    public static void printList(List<? extends Animal> list) {
        for (Animal animal : list) {
            System.out.println(animal);
        }
    }
}

class Animal {
    public String toString() {
        return "Animal";
    }
}

class Dog extends Animal {
    public String toString() {
        return "Dog";
    }
}

class Cat extends Animal {
    public String toString() {
        return "Cat";
    }
}

```

##### 四、类型擦除

类型擦除是泛型实现的一个重要概念。在编译时，泛型类型信息会被擦除，只保留原始类型。这意味着在运行时，泛型类型信息是不可用的。

1. 类型擦除的影响
   类型擦除会导致一些问题，例如无法在运行时获取泛型类型信息，无法使用反射获取泛型类型参数等。

2. 解决方法
   为了解决类型擦除的问题，可以使用 Class 类来获取类型信息，或者使用 Type 接口来获取泛型类型参数。

```
import java.lang.reflect.ParameterizedType;
import java.lang.reflect.Type;

public class TypeErasureExample {
    public static void main(String[] args) {
        // 获取泛型类型参数
        Type type = new ArrayList<String>() {}.getClass().getGenericSuperclass();
        ParameterizedType parameterizedType = (ParameterizedType) type;
        Type[] typeArguments = parameterizedType.getActualTypeArguments();
        System.out.println("泛型类型参数: " + typeArguments[0]);
    }
}

```

##### 五、实际应用示例

##### 1. 泛型在集合框架中的应用

泛型在 Java 的集合框架中得到了广泛应用，例如 `ArrayList`、`HashMap` 等。

###### 示例代码

```
import java.util.ArrayList;
import java.util.HashMap;

public class GenericInCollectionExample {
    public static void main(String[] args) {
        // 使用泛型的 ArrayList
        ArrayList<String> list = new ArrayList<>();
        list.add("Hello");
        list.add("World");
        // 使用泛型的 HashMap
        HashMap<String, Integer> map = new HashMap<>();
        map.put("One", 1);
        map.put("Two", 2);
        // 遍历集合
        for (String s : list) {
            System.out.println(s);
        }
        for (String key : map.keySet()) {
            System.out.println(key + ": " + map.get(key));
        }
    }
}

```

# 11.构造方法及方法重载

#### 1.构造方法

```
（1）语法格式
	class 类名{
		类名（形参列表）{
			构造方法体;
		}
	}
如:
	class Person{
		Person(){
		
		}
	}
```

(2)注意事项
a.构造方法的名称与类名完全相同，没有返回值类型连void都不许有。
(3)默认构造方法

a.当一个类中没有自定义任何形式的构造方法时，编译器会自动添加一个无参的a.空构造方法，叫做默认/缺省构造方法，如:Person(){}

- 建议自定义来参构造方法，不要对编译器形成依赖，避免错误发生。
- 当类中有非常量成员变量时，建议提供两个版本的构造方法，一个是无参构造方法，一个是全属性做参数的构造方法。
- 当类中所有成员变量都是常量或者没有成员变量时，建议不提供任何版本构造

#### 1.2 方法的重载

**（1)基本概念**
	在Java语言中若方法的名称相同但参数列表不同，这样的方法之间构成重载关系
**(2)体现形式**

​	方法重载的主要形式有:参数的个数不同、参数的类型不同、参数的顺序不同，与形参变量名和返回值类型无关，但建议返回值类型最好相同。

​	判断方法是否重载的核心:调用能否区分。

**(3)实际意义**

​	对于调用者来说只需要记住一个方法名就可以调用各种不同的版本实现不同的效果
**如:**
char c=‘a’；

System.out.println(c)；

int i= 10；

System.out.prinltn(i);

double d=3.14；

System.out.println(d);

```
public class OverloadTest{
	void show(){
	System.out.println("show()");
	}
	void show(int i){ 
	//ok 体现在
	System.out.println("show(int)");
	}
	public static void main(Stringll args){
	//声明本类类型的引用 指向本类的对象
	OverloadTest ot=newverloadTest()
	// 调用成员方法
	ot.show();
	ot.show(66);
	ot.show(66，3.14);
	ot.show(66，118);
	ot.show(3.14,66);
	}
}

```

**方法重载的意义**

​	在方法的调用者看来，似乎只有一个print厉法，而它可以处理不同的数据。这样的设计方式，称为重载设计，即设计多个同名但不同参数的方法。适当的使用重载，可以使类的设计变得优雅。

#### 1.3 this关键字

**基本概念**

在构造方法中this关键字代表当前正在构造的对象。
在成员方法中this关键字代表当前正在调用的对象。

原理分析:
当成员方法中访问成员变量时默认会加上this:(相当于汉语中"我的")，当不同的引用调用同一个成员方法时会导致成员方法中的this不同，那么this.访问的结果随之不同。

**使用方式**

（1）当形参变量和成员变量同名时，在构造方法或成员方法中通常优先使用形参变量，若希望使用成员变量就需要在变量名的前面加上this.进行说明(重中之重）。

（2）在构造方法的第一行使用this(实参)的方式可以调用本类中的其它构造方法(了解)

```
public class Boy{
String name;
Boy(){
}
Boy(String s){
	name =s;
}
//this = b1; this.name = b1.name = "肖生杰"
//this = b2; this.name = b2.name = "刘昊";
void show(){
	System.out.println("name ="+ name);
}
public static void main(String[] args){
	Boy bl = new Boy("肖圣杰”);
	b1.show(); //肖圣杰
	System.out.println("------------");
	Boy b2 = new Boy("刘昊");
	b2.show(); //刘昊
}
}

```

**this关键字的作用**

所有的成员变量不能重名，在同一区域的局部变量能重名，但成员变量局部变量可以重名。在局部变量的作用区域之外，变量名代表成员变量，局部变量的作用区域之内，代表局部变量，如果想使用成员变量，需要th的方式访问。
在方法中可以通过this关键字表示“调用该方法的那个对象

```
public void down(int y){
this.y+= y;
}
```

**this关键字和控制**

引用类型变量用于存放对象的地址，可以给引用类型赋值为向任何对象。
当某个引用类型变量为null时无法对对象施访问(因为它没有指向任何对象)。此时，如果通过引用访问成员变量或调用方法，会产生NullPointerException 异常。
Point p = null;

p.print();		会产生NullPointerException

#### 1.4 方法调用的传参过程

​	(1)当形参变量和成员变量同名时，在构造方法或成员方法中通常优先使用形参变量，若希望使用成员变量就需要在变量名的前面加上this.进行说明(重中之重)。

(2)在构造方法的第一行使用this(实参)的方式可以调用本类中的其它构造方法(了解)
3.方法的传参和递归调用
3.1方法的传参过程(理解)
(1)main方法是程序的入口，为main方法中的局部变量开辟内存空间并初始化:

(2)调用max方法时为max方法的形参变量开辟内存空间;

(3)使用实参变量给形参变量进行赋值操作;

(4)当max方法结束后释放形参变量的

(5)main方法中的res得到max方法的返回值然后继续向下执行;

(6)当main方法结束后释放局部变量的内存空间;

```
public class ArgumentTest{
	void show(int i){
	i = 200;
	System.out.println("i="+i); //200
	}
	public static void main(String[] args){
	ArgumentTest at=new ArgumentTest();
	int num=10;
	at.show(num);
	System.out.println("num="+ num); //10
	}
}

```

**传参的基本概念**

- Java中的方法可以传递参数，参数的传递方法就是值传递。

- 参数有形参和实参，定义方法时写的参数叫形参，真正调用方法时，传递的参数叫实参。调用方法时，会把实参传递给形参，方法内部其实是在使用形参。

- 所谓值传递就是当参数是基水类型时，传递参数了值，比如传递i=10，真实传参时，把10赋值给了形参。当参数是对象时，传递的是对象的值，也就是对象的首地址。就是把对象的地址赋值给形参。

**参数传递的步骤**

1分配实参箜间，基本类型在栈中赋值，引用类型变量在栈中指向堆中的对象

2 传递参数其实就是在栈中分配形参的空间，然后把中实参的值复制过来

3 在方法中使用形参，方法结束形参出栈(消失)，只剩下实参。

- gc主要针对堆中的对象，栈中数据是随时进出的。判断堆中对象是不是内存垃圾的条件看栈中是否有指向，直接或者间接的指向都可以，没有的就是内存垃圾。

**使用递推实现阶乘的计算**

```
public class iechengTest{
//自定义成员方法实现参数n阶乘的计算并返回
int show(int n){
int res =l;
for(int i=n;i>l;i--){
res *=i;//res =res *i;
}
return res;
public static void main(String  args){
	JiechengTest jt = new JiechengTest()
	int num= jt.show(5);
	System.out.println("最终计算的结果是:"+num);//num=120
}
}

```

**递归的基本概念**

- 方法自包调用自己就叫递归。递归有可能会大幅简礼代码的编写。递归要考虑性能问题，有些时候可以使用循环而不是递归。

- 递归的使用原则:

  1 必须有退出条件。

  2 必须使问题变简单，而不是复杂化。

# 12.面向对象的多态和抽象类和接口

#### 1.多态的效果

(1)当父类的引用指向子类的对象时，父类的引用可以直接调用父类独有的方法;

(2)当父类的引用指向子类的对象时，父类的引用不可以直接调用子类独有的方法;

(3)对于父子类都有的非静态成员方法来说，编译阶段调用父类版本，运行阶段调用子类重写以后的版本;(4)对于父子类都有的静态方法来说，编译和运行阶段调用父类版本，隶属于类层级,因此与指向的对象无关;

#### 2.引用数据类型之间的转换

(1)引用数据类型之间的转换分为:自动类型转换 和强制类型转换。其中自动类型转换主要指从小范围到大范围之间的转换，也就是子类到父类的转换其中强制类型转换主要指从大范围到小范围之间的转换，:也就是父类到子类的转换

(2)引用数据类型之间的转换必须发生在父子类之间，否则编译报错。

(3)若转换到的目标类型是子类类型但不是该引用真正指向的子类类型，则编译通过,运行阶段发生类型转换异常。

(4)为了避免上述错误的发生，可以使用instanceof进行判断，具体格式如下：

​	if(引用变量名 instanceof 数据类型)-判断引用变量指向的对象是否为后面类型

#### 3.多态的意义

​	多态的实际意义在于可以屏蔽不同子类的差异性实现通用的编程，但可以调用不同的方法带来不同的结果。

#### 4.抽象类

##### 4.1 抽象方法的概念

抽象方法就是指不能具体实现的方法，也就是没有方法体并使用abstract关键字修饰；

```
语法格式:
访问控制符 abstract 返回值类型 方法名称(形参列表);
如:
public abstract void cry();
```

##### 4.2 抽象类的概念

​	抽象类就是指不能具体实例化的类，也就是不能创建对象并使用abstract关键字修饰

##### 4.3 注意事项

(1)抽象类中可以有成员变量、构造方法以及成员方法;

(2)抽象类中可以有抽象方法也可以没有抽象方法;

(3)拥有抽象方法的类必须是抽象类，因此严格来说，具有抽象方法并且使用abstract关键字修饰的类才算真正意义上的抽象类。

**实际意义**

​	抽象类的意义不在于自身创建对象而在于被继承，当一个类继承抽象类后必须重写抽象类中的抽象方法，否则该类也变成抽象类

​	也就是说抽象类对子类具有强制性和规范性因此叫做模板设计模式。

**抽象类的应用**

```
模板设计模式
银行有 定期账户和活期账户。继承账卢类。账户类中:
public class Account{
private double money;
public double getLixi(){ 获取利率的方法，问题来了,
定期和活期账户的利率不一样，方法没法写;
但这个方法必须存在，只能定义成抽象方法，交给子类实现
}
}
```

**经验分享**

​	在以后的开发中推荐使用多态的语法格式，当父类的引用指向子类的对象时，那么父类引用直接调用的所有方法一定是父类拥有的方法，若希望更换子类时，只需要将new关键字后面的类型修改而其它地方无需更改立即生效，从而提高了代码的可维护性。

​	该方式的缺点就是:父类引用不能直接访问子类独有的方法，若访问则需要强转。

#### 5.接口

##### 5.1基本概念

​	接口就是一种比抽象类还抽象的类，体现为所有成员方法都是抽象方法。

​	定义类的关键字是class，而定义接口的关键字是interface

​	继承类的关键字是extends，而实现接口的关键字是implemets。

##### 6.类和接口之间的关系

```
类和类之间的关系			使用extends关键字表达继承的关系				支持单继承
类和接口之间的关系			使用implemets关键字表达实现的关系			支持多实现
接口和接口之间的关系			使用extends关键字表达继承的关系				支持多继承
```

#### 7.抽象类和接口之间的区别

(1)定义抽象类的关键字是abstract class，而定义接口的关键字是interface。
(2)继承抽象类的关键字是extends，而实现接口的关键字是implements。
(3)继承抽象类支持单继承，而实现接口可以多实现。
(4)抽象类中可以有构造方法，而接口中不可以有构造方法，

(5)抽象类中可以有成员变量，而接口中只可以有常量。

(6)抽象类中可以有成员方法，而接口中只可以有抽象方法。

(7)抽象类中增加方法可以不影响子类，而接口中增加方法通常都影响子类。

(8)从jdk1.8开始允许接口中出现非抽象方法，但需要使用default关键字修饰。

#### 8.内部类

##### 2.1 基本概念

​	当一个类的定义出现在另外一个类的类体中时，那么这个类叫做内部类，而这个内部类所在的类叫做外部类。类中的内容:成员变量、成员方法、构造方法、静态成员、构造块和静态代码块、内部类
语法格式

##### 2.2 语法格式

```
class 外部类名{
class 内部类名{
内部类的类体;
}
}
如:
class A{
class B{}
}
```

##### 2.3实际作用

​	当一个类存在的价值仅仅是为某一个类单独服务时，那么就可以将这个类定义为所服务类中的内部类，这样可以隐藏该类的实现细节并且可以方便的访问外部类的私有成员而不再需要提供公有的get和set方法。

##### 2.4基本分类

普通内部类 - 直接将一个类的定义放在另外一个类的类体中。
静态内部类 - 使用static关键字修饰的内部类，隶属于类层级。

局部内部类 - 直接将一个类的定义放在方法体的内部时

​			作用范围是从声明开始一直到方法体结束

**内部类的定义**

- 一个类可以定义在另外一个类的内部，定义在类内部的类称之为Innsr，其所在的类称之为0uter。

![image-20250705153418212](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250705153418212.png)

# 13.面向对象的封装特性和static关键字

#### 1.作业讲解之car类的定义

- 自定义Car类，特征有:品牌(branc、颜色(color)、价格(price)，行为有:无参构造、三个参数的构造、打印所有特征的行为、获取品牌并返回的行为、获取颜色并返回的行为、获取价格并返回的行为、设置品牌为参数指定的数值、设置颜色为参数指定的数实现价格增长1000元的行为、实现价格增长参数指定数值、设置价格为参数指定的数值、值的行为。要求在main()方法中使用无参形式构造对象打印特征，再使用有参形式构造对象打印特征，并使用有参形式构造的对象调用其他方法测试。

```
public class Car{
String brand
String color:
int price;
//无参构造
Car(){
	// 三个参数的构造
	Car(String brand,String color, int price){
	this.brand = brand;
	this.color =color;
	this.price = price;
	}
	//打印所有特征的行为
	void show(){
	System.out.println("品牌:”+color +"，颜色:"+color+"",价格:"+price");
	}
	// 获取品牌并返回的行为
	String getBrand(){
	return brand;
	}
	//获取颜色并返回的行为
	String getColor(){
	return color;
	}
	//获取价格并返回的行为
	int getPrice(){
	return price;
	}
	//设置品牌为参数指定的数值
	void setBrand(String brand){
	this.brand=brand;
	}
	//设置颜色为参数指定的数值
	void setColor(String color){
	this.color =color;
	}
	//设置价格为参数指定的数值
	void setPrice(int price){
	this.price =price
	}
	//实现价格增长1000元的行为
	void grow(){
	price += 1000;
	}
	//实现价格增长参数指定数值的行为
	void grow(int price){
	this.price += price;
	}
}
}

```

#### 2.费氏数列的递归

```
public Class FeeTest{
//自定义成员方法计算费氏数列中第n项数值的计算并返回，n由参数指定
//1 12 3 5 8 13 21 ..
int show(int n){
//使用递归的方式计算并返回
//从第3项起每项都是前两项数值的和，当n=1或n=2时返回1
if(1==n||2==n){
return 1;
}
return show(n-l)+show(n-2);
}
public static void main(String args){
FeeTest ft = new FeeTest();
int res = ft.show(5);
System.out.println("计算的结果是:”+res);
}
}

```

#### 3.封装的基本概念

**3.1基本概念**

​	通常情况下测试类可以对封装类中的成员变量进行赋值，若赋值的数据合法但不合理日ナ无论时编译阶段还是运行阶段都不会报错或者给出提示，I此时与现实生活不符。

​	为了避免上述错误的发生，就需要对成员变量进行密封包装处理，该机制就叫做封装换句话说，封装就是一种保证成员变量值合理性的机制。

**实现流程**

(1)私有化成员变量，使用private关键字修饰;

(2)提供公有的get和set方法，在方法体中进行合理值的判断:

(3)在构造方法中调用set方法进行合理值的判断;

**3.2 封装的概念和流程**

若代码不做限制，则很多属性值是无效的。封装就是保证性值有效的技术。

封装的步骤:
1 属性(非 常量属性) 必须private，确保外部的调用者无法直接赋值。

2 提供操作属性的方法，一般都是读/写属性方法，get属性和set属性方法

3 构造方法中，也要调用set属性方法进行赋值。

#### 4 static关键字

通常情况下，属性/方法都是隶属玉对象层级，就是每个对象都有自己独有的属性空间，有些属性需要属于整个类，就是所有对象要共享。

static就是把对象级提升到类级。static的属性/代码块/方法都是隶属于类在类加载时就准备完成了，而不需要创建对象(new)。

- 类加载只做一次，包括:

  1 类名.的时候会类加载。

  2 new 对象时会类加载。

  3程序员可以用程序加载，比如:Class.forName()。

- 静态的成员(属性和方法)可以用对象.调用，但一般推荐用类名.调用。

**使用方式**

(1)在非静态的成员方法中既能访问非静态的成员也能访问静态的成员;(成员:成员变量+成员方法，静态成员被所有对象共享)

(2)在静态的成员方法中只能访问静态的成员不能访问非静态的成员;(成员:成员变量+成员方法，调用静态方法时可能还没有创建对象)

- static的属性/方法在类加载时就已经做好准备，因此类名.就可以调用，与对象存在不社在无关。
- 非static的属性方法隶属于对象，必须先创建对象，才能使用。

- static的方法中，不能使用非静态的属性或者方法，必须先创建对象，然后用对象.调用;
- static方法的作用在于提供一些“工具方法”和“工厂方法”而非static的方法中，可以直接使用静态的属性或方法
- 只有隶属于类(所有对象共享)的属性才能加static，static不能随便加。

#### 5 单例设计模式

**5.1基本概念**

在某些特殊场合中一一个类对外提供且只提供一个对象，这样的类叫做单例类。
而设计单例类的思想和模式叫做单例设计模式，主要用于固定的场合。

- 设计模式是形成标准化流程的经验总结，是特定问题的固定解决方案。

- 有时候，一个类只需要创建一个对象，不需要第一个，使用单例模式.

- 单例模式的思路:

  1 先private构造，阻止外部去创建对象。

  2 本类提“一个对象，定义一个privatestatic的本类类型属性。

  3 对外提供一个get方法，把唯一的对象传出去。

- 单例有饿汉式和懒汉式两种写法。

**实现流程**

a.私有化构造方法，使用private关键字修饰;

b.声明本类类型的引用指向本类类型的对象，使用private static共同修饰;

c.提供公有的get方法负责将成员变量的数值返回出去，使用static关键字修饰:

**实现方式**

单例设计模式的实现方式有两种:饿汉式和懒汉式，在以后的开发中推荐饿汉式。

#### 6.继承的基本概念

当多个类之间有相同的特征和行为时，可以将相同的内容提取出来组成一个公共类，让多个类吸收公共类中已有特征和行为而在多个类的内部编写自己独有特征和行为方式，叫继承。

使用继承可以提高代码的复用性和扩展性以及可维护性。

在Java语言中使用extends(扩展)关键字来表达继承关系
如:
public class Student extends Person{)-表示Student类继承自Person类

其中Person类叫做基类、父类、超类

其中Student类叫做派生类、子类、孩子类

#### 7.代码块和静态代码块的概念

代码块 -- java允许直接用(}代码，叫代码块。(了解)

写在类体中的代码护叫构造块，每创建对象，构造块都会被执行一次。

前面加staic的构造块叫静态代码块,类加载时执行一次

# 14.面向对象的继承特性和final关键字抽象类和接口

#### 1.继承的注意事项

(1)子类可以继承父类的成员变量和成员方法，其中私有成员变量可以继承但不可以直接使用，子类不可以继承父类的构造方法和私有方法。

(2)无论使用何种方式构造子类对象时，都会自动调用父类中的无参构造方法来初始化从父类中继承下来的成员变量，相当于在子类构造方法的第一行增加代码:super()的效果

(3)使用继承必须满足子类isa父类的逻辑关系，也就是不能滥用继承但一个

(4)Java语言中只支持单继承不支持多继承，也就是一个子类只能有一个父类父类可以有多个子类。

#### 2.方法重写的概念

（1)基本概念
若从父类中继承下来的方法不满足子类的需求时，就需要在子类中重新写一个与父类中方法一样的方法来覆盖从父类中继承的版本，这种方式就叫做重写。

(2)重写的原则(笔试题)

a.要求方法名相同、参数列表相同、返回值类型相同，从jdk1.5开始允许返回子类类型

b.要求方法的访问权限不能变小，可以相同或者变大。

c.要求不能抛出更大的异常(异常机制)。

#### 3.访问控制（笔试题）

**3.1 常见的访问控制符**

![image-20250704093613668](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250704093613668.png)

- 而public修饰的成员变量和方法可以在任何地方调用。public修饰的内容是对外提供可以被调用的功能，需要相对稳定;

- 用protected修饰的成员变量和方法可以被子类及同一个包中的类使用。

- 默认访问控制即不书写任何访问控制符。默认访问控制的成员变量和方法可以被同一个包中的类调用。
- private修饰的成员变量和方法仅仅只能在本类中调用;private修饰的内容是对内实现的封装，如果“公开”会增加维护的成本。

**访问控制符的对比**

- 对于类的修饰可以使用public和默认方式。public修饰的类可以被任何一个类使用;默认访问控制的类只可以被同一个包中的类使用。protected和private可以用于修饰内部类。

![image-20250704093857676](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250704093857676.png)

**package语句的由来**

- 定义类时需要指定类的名称。但如果仅仅将类备作为类的唯一标识，则不可避免的出现命名冲突的问题。这这会给组件复用以及团队间的合作造成很大的麻烦!在Java语言中，用包(package)的概念来解决命名冲突的问题。

**pageage的定义**

- 包名也可以有层欢结构，在一个包中可以包含另外一个包。格式如下:package 包名1.包名2…包名n;
- 如果各个公司或开发组织的程序员都随心所欲的命名包名的话，仍然不能从根本上解决命名冲突的问题。因此，在指定包名的时候应该按照一定的规范。

org.apache.commons.lang.StringUtilStringUtils是类名。而org.apache.commons.lang是多层包名，其含义如下:org.apache表示公司或组织的信息(是这个公司(或组织)域名的反写);common表示项目的名称信息;lang表示模块的名称信息。

#### 4.final修饰类的作用

**4.1 基本概念**

final本意为"最终的,不可更改的"，该关键字可以修饰类、成员方法、成员变量等。

**4.2 使用方式**

final关键字修饰类表示该类不能被继承。

​	为了防止滥用继承带来的危害

​	如:java.lang.String类等

final关键字修饰成员方法表示该方法不能被重写但可以被继承。
	为了防止不经意间造成的方法重写

​	如:java.text.DateFormat类中的format方法等

final关键字修饰成员变量表示该成员变量必须初始化而且不能更改。

​	为了防止不经意间造成数值的更改。

​	如:rjava.lang.Thread类中的MAX PRIORITY

**扩展**：

在以后的开发中很少单独使用static关键字或fina1关键字修饰成员变量，通常都是使用public static final共同修饰成员变量来表达常量的含义，常量的命名规则是:要求所有字母大写，不同单词之间采用下划线连接，如:public static final double PI = 3.14.

#### 5.多态的基本概念和语法

**5.1基本概念**

多态主要指同一种事物表现出来的多种形态。

饮料:可乐、雪碧、脉动、乐虎、红牛、宠物:狗、猫、鸟、乌龟、鱼、.人:学生、教师、工人、
**语法格式**
父类类型 引用变量名=new 子类类型()；

如:
Person pw= new Worker();

**5.2多态的特点**

new Studept();     p 究竟是当父类用，还是子类用呢?

其实是当成父类的对象使用。
1只能使用父类中定义的属性和方法
2不能直接使用子类中扩展的属性和方法。
3 如果子类重写了方法，静态方法调父类的，非静态方法调子类的。
原因:
编译时，p被认为是Person类型;但在运行时是Student类型。在内存中其实是子类对象。

# 15.queue集合的概念和常用方法

**基本概念**

**Queue** 是 Java 中的接口，常用于实现先进先出（FIFO）的数据结构。它提供了插入、删除和检查操作，常见实现类包括 *LinkedList* 和 *PriorityQueue*。

```
import java.util.LinkedList;
import java.util.Queue;

public class QueueExample {
public static void main(String[] args) {
Queue<String> queue = new LinkedList<>();

// 添加元素
queue.offer("元素A");
queue.offer("元素B");
queue.offer("元素C");

// 遍历并移除元素
while (!queue.isEmpty()) {
System.out.println(queue.poll()); // 输出队头元素并移除
}
}
}
```

常用方法

1. **添加元素**： add(E e)：添加失败抛异常。 offer(E e)：添加失败返回 false。
2. **移除元素**： remove()：移除队头，队列为空时抛异常。 poll()：移除队头，队列为空时返回 null。
3. **获取队头元素**： element()：获取队头，不移除，队列为空时抛异常。 peek()：获取队头，不移除，队列为空时返回 null。

注意事项

- **线程安全**：普通的 *Queue* 实现类如 *LinkedList* 不是线程安全的。如果需要线程安全，可以使用 *BlockingQueue*。
- **优先级队列**：*PriorityQueue* 会根据自然顺序或自定义比较器排序，而非 FIFO。

应用场景

- **消息队列**：用于异步任务处理。
- **任务调度**：按顺序执行任务。
- **广度优先搜索（BFS）**：用于图或树的层级遍历。

# 16.Set集合

#### **1.1  Set集合的概述和特点**

​     ——Set集合是一个存储元素不能重复的集合方式，因为存储数据的时候通过判断其元素的hashCode值，不一样再存储。

       Set集合特点：是Collection集合的子类
    
                              不包含重复的元素的集合
    
                              没有带索引的方法，所以不能用普通的for循环遍历。

 **1.2  哈希值**
         哈希值：是JDK根据u第项的地址或者数字运算出来的int类的数值；

        Object类中有一个方式可以获取哈希值， public int hashCode();返回哈希值。

   对象哈希值的特点 ：

        1、同一个对象多次调用和hashCode()方法返回的哈希值是相同的。
    
        2、默认情况下，不同对象的哈希值是不同，但可以通过重写hashCode方法使得哈希值相同。     

注意：有不一样的字符串 的哈希值也有一样，因为String 重写了hashCode方法，比如“重地“和”通话“，哈希值都是1179395

#### **2、HashSet集合**

**2.1 HashSet集合的特点**      
————也就说 HashSet是 元素不重复，输入输出无序

1、底层数据结构是哈希表

2、对集合的迭代顺序不作任何保证，也就是说不保证存储和取出的先后顺序一致；

3、没有带索引的方法，所以不能用普通的for循环遍历， 但可以用加强for和 iterator 迭代器遍历

4、由于是Set集合，所以不包含重复元素

**2.2 HashSet 集合使用格式**

格式： Set<T>  对象名=new  HashSet<T>();  //T是数据类型

           HashSet   对象名=new   HashSet<T>();

 **2.3 HashSet集合保证元素唯一性源码分析**
        ——HashSet是通过哈希值存储元素，使得元素的不重复性。

​        —— 要保证唯一性，需要在引用类型中重写hashCode()和equals()方法；

 **2.4  HashSet的基本方法**
       因为HashSet是Set类的子类，而Set类是Collection的子类，即hashCode的基本方法继承了Collection方法，如下

方法	含义
boolean  add(E e);	添加元素
boolean   remove(object  o);        	移除指定的元素
void   clear();	清楚集合种所有的元素
boolean contains (Object o);	判断集合种是否存在指定的元素
boolean  iEmpty();	判断集合是否为空
int  size();	计算集合长度（元素个数）

####    **3、LinkHashSet 集合**

 **3.1 LinkHashSet集合概述和特点**
     1、哈希表和链表实现Set接口，具有可预测的迭代次序；

     2、由链表保证元素有序，也就是说元素的存储和取出顺序hi是一致的。
    
     3、由哈希值保证元素唯一，也就是说没有重复的元素

 **3.2 LinkHashSet集合创建对象格式**

格式：Set<T>  集合名=new LinkHashSet<T>();  //T是数据类型

           LinkHashSet <T>   集合名=new  LinkHashSet<T>()；

**3.3 LinkHshSet集合的基本用法**
   LinkHashSet与HashSet的用法基本一致.

#### **4、TreeSet集合**

**4.1    TreeSet 集合特点**
       ——元素按一定顺序排序，元素不重叠

```
  1、元素有序：这里的顺序不是指存储和取出的顺序，而是按照一定的规则进行排序，具体排序方法取决于构造方法。   

                 TreeSet(): 根据其元素的自然排序进行排序；

                  TreeSet (Comparator comparator):根据指定的比较器进行排序

   2、没有索引的方法：所以不能用普通的for循环遍历，可以用加强for或迭代器iterator

   3、由于是Set集合，所以不包含重复元素
```

**4.2 TreeSet 创建对象格式**
      格式： Set<T>  集合名=new  TreeSet<T>();  //  T表示数据类型

```
            TreeSet<T>  集合名=new TreeSet<T>();
```

**4.3 自然排序Comparable的使用**
              1、存储学生的对象并遍历，创建TreeSet集合使用无参构造方法

结论：1、用TreeSet 集合存储定义对象，无参构造方法使用的是自然排序对元素进行排序的；

```
       2、自然排序，就是让元素元素所属的类实现Comparable接口，重写compareTo(To)方法

       3、重写方法时，一定要注意排序规则必须按照要求的主要条件和次要条件来写。
```
 4.3 比较器排序Comparator 的使用

```
——存储学生对象并遍历，创建TreeSet集合使用的带参构造方法
```

结论：

```
  1、用TreeSet集合存储自定义对象，带参构造方法使用的是比较器排序对元素进行排序的；

  2、比较器排序，就是让集合构造方法接收Comparator的实现对象。重写compara(T  o1,T  o2)方法；
  3、重写方法时，一定要注意排序规则必须按照要求的主要条件和次要条件来写 
```

##### 首先是添加元素的put()方法：

```
//hashMap的添加元素方法
    public V put(K key, V value) {
        return putVal(hash(key), key, value, false, true);
    }
 
 
   //hash()方法，用于计算当前元素的hash值
    static final int hash(Object key) {
        int h;
        return (key == null) ? 0 : (h = key.hashCode()) ^ (h >>> 16);
    }
 
 
```

**下面是putVal()方法：**	
putVal()的执行流程：

1.put方法传入键值对

2.计算hash值

3.根据hash值找到在数组中的存放位置

如果无哈希冲突，则直接存入数组中

如果出现了哈希冲突时：

如果当前的数据结构是红黑树 则存入到红黑树

如果当前的数据结构是链表时：

如果链表插入之后长度小于8，则直接插入到链表中

如果链表插入之后长度大于等于8，则将链表转化为红黑树，存入红黑树中

```
final V putVal(int hash, K key, V value, boolean onlyIfAbsent,
                   boolean evict) {
        Node<K,V>[] tab; Node<K,V> p; int n, i;
        //如果数组为空，调用resize()方法进行初始化
        if ((tab = table) == null || (n = tab.length) == 0)
            n = (tab = resize()).length;
 
        //i = (n - 1) & hash获取数组的索引位置，如果计算的索引对应的位置上没有元素，则直接插入该节点
        if ((p = tab[i = (n - 1) & hash]) == null)
            tab[i] = newNode(hash, key, value, null);
        //出现了哈希冲突，通过链表或红黑树解决冲突
        else {
            Node<K,V> e; K k;
            //如果该索引对应的已经存在的元素与待插入的元素key相等，则覆盖
            if (p.hash == hash &&
                ((k = p.key) == key || (key != null && key.equals(k))))
                e = p;
            //如果p已经存在，而且是红黑树
            else if (p instanceof TreeNode)
                //那么将该元素添加到红黑树中
                e = ((TreeNode<K,V>)p).putTreeVal(this, tab, hash, key, value);
                //如果p已经存在，不是红黑树而是链表
            else {
                   //遍历链表
                for (int binCount = 0; ; ++binCount) {
                     //如果节点链表的next为空
                    if ((e = p.next) == null) {
                         //将待添加的节点直接添加到链表中
                        p.next = newNode(hash, key, value, null);
                        //如果节点链表的数量超过8个，则将其转化为红黑树，以便于查找
                        if (binCount >= TREEIFY_THRESHOLD - 1) // -1 for 1st
                            treeifyBin(tab, hash);
                        break;
                    }
                    //如果待传入的key和链表中已经存在的key相同，则直接退出，因为HashMap中无重复元素
                    if (e.hash == hash &&
                        ((k = e.key) == key || (key != null && key.equals(k))))
                        break;
                    p = e;
                }
            }
            if (e != null) { // existing mapping for key
                V oldValue = e.value;
                if (!onlyIfAbsent || oldValue == null)
                    e.value = value;
                afterNodeAccess(e);
                return oldValue;
            }
        }
        ++modCount;
        //当前的大小大于阈值，则扩容
        if (++size > threshold)
            resize();
        afterNodeInsertion(evict);
        return null;
    }
```

 下面是resize()扩容方法：

当向容器添加元素的时候，会判断当前容器的元素个数，如果大于等于阈值—即当前数组的长度乘以加载因子的值的时候，就要自动扩容。

```
final Node<K,V>[] resize() {
        Node<K,V>[] oldTab = table;
        //现有数组的容量等于数组长度，数组为空时，容量为0
        int oldCap = (oldTab == null) ? 0 : oldTab.length;
        int oldThr = threshold;
        int newCap, newThr = 0;
        //先有容量大于0，则已经扩容过了 
        if (oldCap > 0) {
            //现有容量大于最大容量，直接返回
            if (oldCap >= MAXIMUM_CAPACITY) {
                threshold = Integer.MAX_VALUE;
                return oldTab;
            }
            //如果扩大两倍之后的容量小于最大容量，且现有容量大于等于初始容量16
            else if ((newCap = oldCap << 1) < MAXIMUM_CAPACITY &&
                     oldCap >= DEFAULT_INITIAL_CAPACITY)
                //// 新的扩容阀值扩大为两倍
                newThr = oldThr << 1; // double threshold
        }
        // 否则如果当前容量等于0 ，但是当前扩容阈值 > 0,调用有参构造函数会到这里
        else if (oldThr > 0) 
            newCap = oldThr;
        else {   
            // 新的容量等于默认容量            
            newCap = DEFAULT_INITIAL_CAPACITY;
            // 新的扩容阈值等于默认负载因子0.75*默认容量16=12
            newThr = (int)(DEFAULT_LOAD_FACTOR * DEFAULT_INITIAL_CAPACITY);
        }
        if (newThr == 0) {
              // 设置新的扩容阈值等于新的容量*负载因子
            float ft = (float)newCap * loadFactor;
            newThr = (newCap < MAXIMUM_CAPACITY && ft < (float)MAXIMUM_CAPACITY ?
                      (int)ft : Integer.MAX_VALUE);
        }
        threshold = newThr;
        @SuppressWarnings({"rawtypes","unchecked"})
        Node<K,V>[] newTab = (Node<K,V>[])new Node[newCap];
        table = newTab;
        if (oldTab != null) {
            for (int j = 0; j < oldCap; ++j) {
                Node<K,V> e;
                if ((e = oldTab[j]) != null) {
                    oldTab[j] = null;
                    if (e.next == null)
                        newTab[e.hash & (newCap - 1)] = e;
                    else if (e instanceof TreeNode)
                        ((TreeNode<K,V>)e).split(this, newTab, j, oldCap);
                    else { // preserve order
                        Node<K,V> loHead = null, loTail = null;
                        Node<K,V> hiHead = null, hiTail = null;
                        Node<K,V> next;
                        do {
                            next = e.next;
                            if ((e.hash & oldCap) == 0) {
                                if (loTail == null)
                                    loHead = e;
                                else
                                    loTail.next = e;
                                loTail = e;
                            }
                            else {
                                if (hiTail == null)
                                    hiHead = e;
                                else
                                    hiTail.next = e;
                                hiTail = e;
                            }
                        } while ((e = next) != null);
                        if (loTail != null) {
                            loTail.next = null;
                            newTab[j] = loHead;
                        }
                        if (hiTail != null) {
                            hiTail.next = null;
                            newTab[j + oldCap] = hiHead;
                        }
                    }
                }
            }
        }
        return newTab;
    }
```

#### 5.Java迭代器的详解

##### 迭代器的定义

​	迭代器是属于设计模式之一，迭代器模式提供了一种方法来顺序访问一个聚合对象中各个元素，而不保留该对象的内部表示。

1）Iterator对象称为迭代器，主要用于遍历Collection集合中的元素。
2）所有实现了Collection接口的集合类都有一个iterator()方法，用以返回一个实现了Iterator接口的对象，即可以返回一个迭代器。
3）Iterator仅用于遍历集合，Iterator本身并不存放对象。
**认识Iterator**

![image-20250706205052367](C:\Users\li\AppData\Roaming\Typora\typora-user-images\image-20250706205052367.png)

通过观察类结构图的继承关系我们发现，集合的顶层接口`Collection`继承`Iterable`接口。

##### Iterable接口

```
public interface Iterable<T> {
    /**
     * Returns an iterator over elements of type {@code T}.
     *
     * @return an Iterator.
     */
    Iterator<T> iterator();
}

```

在`Iterable接口`中有一个`Iterator方法`，它返回一个`Itertator对象`。

##### Iterator接口

```
public interface Iterator<E> {
    boolean hasNext();
    
    E next();
    
    default void remove() {
        throw new UnsupportedOperationException("remove");
    }
}

```

##### Iterator接口的方法

| **返回值类型** | **方法名** | **功能**                                                     |
| -------------- | ---------- | ------------------------------------------------------------ |
| boolean        | hasNext()  | 判断集合是否还有元素，如果返回 **true** 表示集合还有元素，返回 **false** 表示集合中没有元素；一般对集合的访问通过 **while(hasNext())** 判断是否还需要遍历。 |
| E              | next()     | 获取集合中遍历的当前元素 ；一般先调用 **hasNext()** 方法判断是否存在元素，再调用 **next()** 获取元素，需要进行循环交替遍历集合中的元素。 |
| void           | remove     | 删除集合中的元素。                                           |

##### 使用迭代器遍历集合

我们用`ArrayList集合`存放一些整型数据做示例，然后将其集合中的元素一一遍历打印输出。

```
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class TestDemo {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<>();
        list.add(111);
        list.add(222);
        list.add(333);

        Iterator<Integer> iterator = list.iterator();
        while(iterator.hasNext()) {
            int value = iterator.next();
            System.out.print(value + " ");
        }
    }
}

```

##### 执行过程详解

①首先得到一个集合的迭代器Iterator iterator = list.iterator();
②进入while循环，调用hasNext()判断是否有下一个元素，返回true，Iterator.next()移动一个位置，将该位置的元素111返回。
③再次进入while循环，调用hasNext()判断是否有下一个元素，返回true，Iterator.next()移动一个位置，将该位置222的元素返回。
④再次进入while循环，调用hasNext()判断是否有下一个元素，返回true，Iterator.next()移动一个位置，将该位置333的元素返回。
⑤再次进入while循环，调用hasNext()判断是否有下一个元素，返回false，循环结束。
	在 迭代器的遍历过程中先通过hastNext()方法判断是否有下一个元素，如果存在下一个元素再调用next()方法获取元素，在这里next()方法先往后移动一个元素位置，再返回该位置的元素。因此，在调用next()方法之前必须要调用hastNext()方法进行检测；如果没有调用并且没有下一个元素，直接调用next()方法会抛出 NoSuchElementException异常。

##### 生成迭代器的快捷键

​	一开始使用迭代器可能会觉得麻烦，但是如果用的`Idea编译器`是有快捷键的，输入`itit`再回车就会直接生成。

##### 迭代器中的remove()

##### 迭代器的remove()方法使用

在Iterator接口中除了`hasNext()`和`next()`方法外，还有一个`remove()`方法，即**删除集合中的元素**。

*如删除上述示例集合中的元素111*

```
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;
@SuppressWarnings({"all"})
public class TestDemo {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<>();
        list.add(111);
        list.add(222);
        list.add(333);

        System.out.println("删除前:" + list);
        Iterator<Integer> iterator = list.iterator();
        while (iterator.hasNext()) {
            Integer value =  iterator.next();
            if(value == 111) iterator.remove();
        }
        System.out.println("删除后" + list);
    }
}

```

##### 迭代器遍历中调用集合revome()方法触发异常

​	在Java集合中，以集合ArrayList为例，在使用中可能会遇到删除的需求场景，此时如果代码书写不当，极有可能会抛出java.util.ConcurrentModificationException异常信息。
在上述示例中用Iterator调用了迭代器remove()方法，如果在使用中不小心调用了集合中的remove()方法会发生什么？

```
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;
@SuppressWarnings({"all"})
public class TestDemo {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<>();
        list.add(111);
        list.add(222);
        list.add(333);

        System.out.println("删除前:" + list);
        Iterator<Integer> iterator = list.iterator();
        while (iterator.hasNext()) {
            Integer value =  iterator.next();
            if(value == 111) list.remove(Integer.valueOf(111));
        }
        System.out.println("删除后" + list);
    }
}


```

运行结果中抛出`java.util.ConcurrentModificationException`异常信息。这是因为触发了集合中并发修改的异常 接下来我们通过源码对抛出异常的原因进行剖析。

```
    public Iterator<E> iterator() {
        return new Itr();
    }

```

在`ArrayList`集合的`Iterator`方法中，是通过返回`Itr`对象来获得迭代器的。`Itr`是`ArrayList`的一个内部类，它实现了`Iterator`接口，*代码如下：*

```
   private class Itr implements Iterator<E> {
        int cursor;       // index of next element to return
        int lastRet = -1; // index of last element returned; -1 if no such
        int expectedModCount = modCount;

        Itr() {}

        public boolean hasNext() {
            return cursor != size;
        }

        @SuppressWarnings("unchecked")
        public E next() {
            checkForComodification();
            int i = cursor;
            if (i >= size)
                throw new NoSuchElementException();
            Object[] elementData = ArrayList.this.elementData;
            if (i >= elementData.length)
                throw new ConcurrentModificationException();
            cursor = i + 1;
            return (E) elementData[lastRet = i];
        }

        public void remove() {
            if (lastRet < 0)
                throw new IllegalStateException();
            checkForComodification();

            try {
                ArrayList.this.remove(lastRet);
                cursor = lastRet;
                lastRet = -1;
                expectedModCount = modCount;
            } catch (IndexOutOfBoundsException ex) {
                throw new ConcurrentModificationException();
            }
        }

```

##### Itr类属性

| 属性             | 含义                                                     |
| ---------------- | -------------------------------------------------------- |
| cursor           | 索引下标，表示下一个可以访问的元素的索引，默认值为 **0** |
| lastRet          | 索引下标，表示上一个元素的索引，默认值为 **-1**          |
| expectedModCount | 对集合修改的版本号，初始值为**ModCount**                 |

ModCount定义在AbstractList接口中，初始值为**0**，定义如下：

```
 protected transient int modCount = 0;

```

ModCount是版本号，在对集合进行变更操作（增加、删除、修改等）的时候会对版本号进行 **+1** 操作。

结合上述代码进行抛出java.util.ConcurrentModificationException异常的解释。
①初始化ArrayList，添加三次元素，即三次调用add()方法，进行三次modCount++; 此时，

mod Count = 3 ， size = 3 ； 	color{red}{modCount = 3，size = 3；}modCount=3，size=3；

②初始化Iterator迭代器进行循环，此时，e x p e c t e d M o d C o u n t = m o d C o u n t = 3 ， \color{red}{expectedModCount = modCount=3，}expectedModCount=modCount=3， c u r s o r = 0 ， l a s t R e t = − 1 \color{red}{cursor=0，lastRet = -1}cursor=0，lastRet=−1

③进行hasNext判断，cursor != size;成立，进入循环

④调用next()方法，首先进行checkForComodification()校验，m o d C o u n t = = e x p e c t e d M o d C o u n t \color{red}{modCount == expectedModCount}modCount==expectedModCount，校验通过，返回值，此时l a s t R e t = 0 ; c u r s o r = 1 \color{red}{lastRet = 0;cursor = 1}lastRet=0;cursor=1


```
 final void checkForComodification() {
            if (modCount != expectedModCount)
                throw new ConcurrentModificationException();
        }

```

⑤调用集合remove()方法，modCount++；，此时m o d C o u n t = 4 ; s i z e = 2 \color{red}{modCount = 4;size = 2}modCount=4;size=2
⑥再次调用hasNext()方法判断，cursor != size;成立，进入循环
⑦调用next()方法进行校验，m o d C o u n t ! = e x p e c t e d M o d C o u n t \color{red}{modCount != expectedModCount}modCount!=expectedModCount，校验未通过，抛出java.util.ConcurrentModificationException异常

#### 增强for循环