### 计算机基础概念

计算机（Computer）是一种被广泛应用于各个领域的设备。它由**硬件和软件**两大部分组成，广泛应用于科学计算、数据处理、自动化控制、通信、娱乐等领域。

#### 1. 计算机的核心

##### 1.1 硬件（Hardware）

- **中央处理器（CPU）**：负责执行指令和处理数据，是计算机的“大脑”。
- **存储器**：包括内存（RAM，临时存储）和硬盘（永久存储）。
- **输入/输出设备**：如键盘、鼠标、显示器、打印机等。

[^]: 科普:1TB = 1024GB , 1GB = 1024MB.(MB也就是常见的'兆'),1MB = 1024KB, 1KB = 1024byte(字节).通常一个英文字母占1个字节，一个汉字占2个字节.1byte =  8bit(二进制位)在计算机的底层识别0和1组成的二进制序列.

##### 1.2 软件（Software）

- **系统软件**：如操作系统（Windows、macOS、Linux），管理硬件和运行其他程序。
- **应用软件**：如办公软件、游戏、浏览器等，完成特定任务。

#### 2. 计算机体系结构

使用者 => 应用软件 => 系统软件 => 硬件设备 

​			=> 其中系统软件分为:内核(Kernel) 和 外壳(She11)

***

### java语言

Java 是一种广泛使用的 **高级编程语言**.它由 **Sun Microsystems**（现为 **Oracle** 公司所有）于 1995 年推出，以其 **“一次编写，到处运行”**（Write Once, Run Anywhere, WORA）的特性而闻名。

#### 1. Java语言的主要版本

- Java SE - 称之为“Java平台标准版”，主要学习Java语言的语法规范和常见类。
- Java EE - 称之为“Java平台企业版”，主要学习Java后台开发技术，编写B/S架构项目。
#### 2. java相关概念

**jdk** - Java开发工具包，只要做Java开发就需要下载和安装该软件。

**jre** - Java运行时环境信息，只要运行Java程序就需要下载和安装该软件。

**jvm** - Java虚拟机，是Java程序与计算机操作系统之间的桥梁

**javac.exe** - Java语言的编译器，主要用于将Java程序进行编译生成字节码文件。

**java.exe** - Java语言的解释器，主要用于启动Java虚拟机对字节码文件进行解释执行。

#### 3. 创建你的第一个java代码

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```

### Java语言的基本语法格式

####  1.变量和注释(重点)

##### 1.1 基本概念

​	当需要在Java程序中记录单个数据内容时，则声明一个变量即可，而声明变量的本质就是在内存空间中申请一块存储单元，由于该存储单元的数值可以发生改变，因此得名为变量”

​	由于存放数据内容的大小不同导致所需存储单元的容量不同，在Java语言中使用数据类型加以描述，为了便于下次访问还需要指定变量的名称。

##### 1.2 声明方式

​	数据类型 变量名 = 初始值

 ```java
public class demoTest {
    public static void main(String[] args) {
        // 1. 声明一个初始化为10元素类型为int类型的变量
        int a = 10;
        // 2. 打印变量的数值 + 字符串连接符,用于实现连接的功能\
        System.out.println("a =" + a);
        System.out.println("---------------------");
        //3. 变量在使用之前必须声明
        // System.out.println("sa = " + sa); //错误: 找不到符号
        // String sa;
       	// System.out.println("sa = " + sa); //错误: 变量未初始化sa
        String sa = "xiaoming";
        System.out.println("sa = " + sa); //sa = xiaoming     
        
        int a = 10; //4. 变量不能重复定义 (错误: 已定义了变量 a)               
    }
}
 ```

##### 1.3 标识符(变量名)的命名规则

- 要求由字母丶数字丶下划线和美元$组成,其中数字不能开头.

  如: name丶age丶name1等

- 要求不能使用Java中的关键字，所谓关键字就是Java中用于表示特殊含义的单词。
  如:public、class、void、static等

- 区分大小写，长度没有限制但不宜过长。

  如:name 和Name代表不同的标识符，**不推荐使用**

- 尽量做到见名知意，支持中文但不推荐使用。

  如:year、month、size、length、time等

```java
import java.util.Scanner

public class Input {
    public static void main(String[] args) {
        //输入姓名和年龄并赋值给变量
        System.out.println("请输入姓名和年龄：");
        //创建Scanner对象来获取用户输入
        Scanner sc = new Scanner(System.in);
        //通过扫描器获取用户输入字符串
        String name = sc.next();
        //通过扫描器获取用户输入整数
        int age = sc.nextInt();
        //打印输出姓名和年龄
        System.out.println("姓名：" + name + "，年龄：" + age);
    }
}
```

##### 1.4 注释

- //表示单行注释，从//开始一直到本行末尾的所有内容都是注释。

- /* */表示多行注释，从/*开始一直到*/之间的所有内容都是注释。

[^]: 多行注释不允许嵌套

#### 2.数据类型

##### 2.1 基本数据类型

在java中将数据分为两大类: 

1. 基本数据类型

   byte、short、int、long、float、double、boolean、char

2. 引用数类型

   数组.类.接口.注解.枚举

[^]: 生活中常见的数字都是十进制,而在编程中,我们需要学到二进制.也就是只包括 0 和 1 的数字.在进制转换中,我们需要学到数学中的概念"权重".如:345这个十进制数字,在百位上的权重是10的2次方,在十位数上,权重是10的1次方,在个位数上,是10的0次方,等于300 *10  * 10  + 40 * 10 * 1 + 5 * 10 * 0 = 345.

### 算数运算符的概念和使用

#### 1.算数符

'+'表示加法运算符	'/'表示除法运算符	'-'表示减法运算符 

'*'表示乘法运算符	'%'表示取模/取余运算符

**注意:**

(1)在Java语言中两个整数相除时，结果只保留整数部分丢弃小数部分;

(2)若希望保留小数部分，则处理方式如下:

​	a.将其中任意一个操作数强转为double类型进行运算即可;

​	bi让其中任意一个操作数乘以1.0后

(3)0不能做除数，0.0可以做除数但结果是无穷

(4)+既可以作为算术运算符也可以作为字符串连接符，区分方式如下，只要+两端的操作数中有一个是字符串类型，则按照字符串连接符对待.

**案例:**

```java
import java.util.Scanner;

public class demo1 {
    public static void main(String[] args) {
        //1. 提示用户输入
        System.out.println("请输入数字：");
        Scanner sc = new Scanner(System.in);
        int number = sc.nextInt();
        //2. 将输入数字进行转换
        int a = number / 100; // 百位
        int b = number % 100 / 10;// 十位
        int c = number % 10; // 个位
        //3. 打印输出
        System.out.println("百位：" + a + " 十位：" + b + " 个位：" + c);
    }
}
```

#### 2 关系/比较运算符

'>'表示是否大于运算符	'<'表示是否小于运算符

'=='表示是否等于运算符	'>='表示是否大于等于运算符

'<='表示是否小于等于运算符	'!='表示是否不等于运算符
**注意:**所有以关系运算符作为最终运算的表达式结果一定是boolean类型，只有true和false

#### 3 自增减运算符

'+'表示加法运算符	'-'表示减法运算符
'++'表示自增运算符，主要用于使得变量自身的数值加1

'--'表示自减运算符，主要用于使得变量自身的数值减1

注意:
(1)对于变量自身来说,++a和a++都实现变量自身数值的加1效果,是等价的;

(2)a++ 表示先让a的数值作为整个表达式的结果，然后再让a自身的数值加1;

​	++a 表示先让a自身的数值加1，然后再作为整个表达式的结果;

#### 4.逻辑运算符

&& 表示逻辑与运算符,相当于"并且”，同真为真，一假为假

|| 表示逻辑或运算符，相当于"或者”，一真为真，同假为假。

!	表示逻辑或运算符，相当于"或者”，一真为真，同假为假。

逻辑运算符两端的操作数都是boolean类型的，结果也应该是boolean类型的

**"&&”丶"||"具备“短路”的特性:如果通过第一个表达式的值即可得出最后的结果，则不计算第二个表达式。**

```java
import java.util.Scanner;

public class demo2 {
    public static void main(String[] args) {
        //1. 提示用户输入
        System.out.println("请输入数字：");
        Scanner sc = new Scanner(System.in);
        int number = sc.nextInt();
        //2. 使用逻辑运算符进行判断并打印
        if (number % 2 == 0) {
            System.out.println("偶数");
        }
        else {
            System.out.println("奇数");
        }
    }
}
```

#### 5. 条件运算符

**三目运算符**

 条件表达式 ? 表达式1: 表达式2

​	=>判断条件是否成立

​		=>若成立，则执行表达式1;

​		=>若不成立，则执行表达式2;

```java
import java.util.Scanner;

public class demo3 {
    public static void main(String[] args) {
        //1. 提示用户输入两个数字
        System.out.println("请输入两个数字：");
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        //2. 使用三目运算符进行判断并打印
        String result = a > b ? "a比b大" : "a比b小";
    }
}
```

#### 6. 赋值运算法

(1)简单赋值
=表示赋值运算符，主要用于将=右边的数据赋值给=左边的变量，覆盖原来的数值

(2)复合赋值

+=丶 -= 丶*= ...

#### 7运算符的优先级

a. ()的优先级极高.

b. =的优先级极低.

c. 若实在不确定运算符的优先级，则可以借助()加以确定:

#### 8.位运算符

&表示按位与运算符，就是按照二进制位进行与运算，同1为1，一0为0(1-真 0-假).
|表示按位或运算符，就是按照二进制位进行或运算，一1为1，同0为0.
~表示按位取反运算符，按照二进制位进行取反，1为0，0为1.
^表示按位异或运算符，按照二进制位进行异或运算，相同为0，不同为1.

### 分支结构

#### 1. 基本概念

在某些特殊场合中需要进行判断并作出选择时，就需要使用分支结构

#### 2. if分支结构

语法结构

​	if(条件表达式){

​		语句块;

​	}

=>判断条件,若成功,执行语句,结束;

#### 3. if-else分支结构

if(条件表达式){

​		语句块;

​	}else{

​		语句块;

​	}

 =>判断条件,若成功,执行语句1,结束;

=>判断条件,不成功,执行语句2,结束;

#### 4. if-elseif-else分支结构

语法结构

​	if(条件表达式1){

​		语句块1;

​	}elseif(条件表达式2){

​		语句块2;

​	}else{

​		语句块3;

​	}

 =>判断条件1,若成功,执行语句1,结束;

=>判断条件1,不成功,判断条件2,若成功,执行语句2,结束;

=>判断条件1,不成功,判断条件2,不成功,直接执行语句3,结束;

```java
import java.util.Scanner;

public class demo4 {
    public static void main(String[] args) {
        //1. 提示用户输入两个数字
        System.out.println("请输入数字：");
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        //2. 使用if语句进行判断并打印
        if (a > b) {
            System.out.println("a比b大");
        }else if (a < b) {
            System.out.println("a比b小");
        }else {
            System.out.println("a和b相等");
        }
    }
}
```

#### 5.switch-case分支结构

语法结构

switch(变量/表达式){

​	case 字面值1: 语句块1;break;

​	case 字面值1: 语句块1;break;

​	...

​	default: 语句块n;

}

**注意事项:**

switch()中支持的数据类型有:byte、short、char以及int类型，从idk1.5开始支持枚举类型,从jdk1.7开始支持String类型.

```java
package day1;

import java.util.Scanner;

//使用switch-case分支结构
public class demo10 {
    public static void main(String[] args) {
        //1.提示用户输入1~7中的整数
        System.out.println("请输入1~7中的整数：");
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        //2.使用switch-case分支结构进行判断并打印
        switch (a) {
            case 1:
                System.out.println("星期一");
                break;
            case 2:
                System.out.println("星期二");
                break;
            case 3:
                System.out.println("星期三");
                break;
            case 4:
                System.out.println("星期四");
                break;
            case 5:
                System.out.println("星期五");
                break;
            case 6:
                System.out.println("星期六");
                break;
            case 7:
                System.out.println("星期日");
                break;
            default:
                System.out.println("输入的数字有误！");
                break;
        }
    }
}
```

***

### 循环结构

#### 1. 基本概念

在某些特殊场合中需要重复执行一段代码时，借助循环结构加以处理.

#### 2. for循环

语法格式

​	for(初始化表达式; 条件表达式;修改初始值表达式){

​		循环体;

​	} 

```java
import java.util.Scanner;
/*
*   编程实现for循环的使用
*/
public class demo5 {
    public static void main(String[] args) {
        //1. 提示用户输入
        System.out.println("请输入数字：");
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        //2. 使用for循环进行打印
        for (int i = 0; i < a; i++) {
            System.out.println("i = " + i);
        }
    }
}
```

```java
//编程使用for循环实现1~100的数字累加和并打印
public class demo6 {
    public static void main(String[] args) {
        //1. 定义变量保存结果
        int sum = 0;
        //2. 循环累加
        for (int i = 1; i <= 100; i++) {
            sum += i;
        }
        System.out.println(sum);
    }
}
```

***

##### 2.1 break和continue关键字

break关键字用于循环中表示跳出当前循环;
continue关键字用于循环中表示结束本次循环继续下一次循环(会用);

```java
//编程使用break和continue
public class demo7 {
    public static void main(String[] args) {
        //使用break
        for (int i = 0; i < 100; i++) {
            if (i == 20) {
                break;//跳出循环
            }
            System.out.println(i);
        }
        //使用continue
        for (int i = 0; i < 100; i++) {
            if (i == 20) {
                continue;//跳过当前循环
            }
            System.out.println(i);
        }
    }
}
```

##### 2.2 特殊的循环

for(;;) - 这种没有循环条件的循环叫做无限循环，俗称"死循环,通常与break关键字搭配使用.

2.3 双重for的使用

​	for(初始化表达式1; 条件表达式2;修改初始值表达式3){

​			for(初始化表达式4; 条件表达式5;修改初始值表达式6){

​						循环体;

​			} 

​	} 

```java
package day1;
//双重for的使用
public class demo8 {
    public static void main(String[] args) {
        //外层循环
        for (int i = 0; i < 10; i++) {
            //内层循环
            for (int j = 0; j < 10; j++) {
                System.out.println("i = " + i + " j = " + j);
            }
        }
    }
}
```

***

#### 3. while循环

语法格式

while(条件表达式){

​	循环体;

}

```java
package day1;
//使用while循环
public class demo9 {
    public static void main(String[] args) {
        int i = 0;
        //循环条件
        while (i < 10) {
            System.out.println("i = " + i);
            i++;
        }
    }
}
```

**注意事项:**

a. while循环和for循环可以完全互换;

b. while(true)和for(;;)表示无限循环;

c. while循环主要用于明确循环条件但不明确循环次数的场合中;
	for循环主要用于明确循环次数或范围的场合中;

### 一维数组

#### 1. 基本概念

​	当需要在程序中记录单个数据内容时，则声明一个变量即可;

​	当需要在程序中记录多个类型相同的数据内容时，则声明一维数组即可，一维数组的本质就是在内存中申请一段连续的存储单元，

如:

``` java
int[ ] arr = new int[5]; //表示声明一个长度为5元素类型为int类型的一维数组.
```

其中:

arr -表示数组的名称，便于下次访问该存储空间的数据

数组元素-主要指存放到数组中的数据内容。

数组长度-主要指数组的容量或最多可以存放的元素个数。

​	-数组名.length

数组下标-主要指数组元素的编号，从0开始可以取到长度-1。

```java
package day2;
//编程实现数组的声明和打印
public class demo2 {
    public static void main(String[] args) {
        //1. 数组声明
        int[] arr = new int[3];//动态方式
        //2. 打印数组长度和数组元素
        System.out.println(arr.length);// 未初始化默认值为0
        System.out.println(arr[0]);
        System.out.println(arr[1]);
        System.out.println(arr[2]);
//        System.out.println(arr[3]);//数组访问越界
        System.out.println("-----------------");
        //3. 循环实现数组打印
        for (int i = 0; i < arr.length; i++) {
            System.out.println(arr[i]);
        }
        //4. 声明一个长度为5的double类型数组
        double[] arr1 = new double[5];//默认值0.0
        //5. 循环实现数组打印
        for (int i = 0; i < arr1.length; i++) {
            System.out.println(arr1[i]);
        }
        System.out.println("-----------------");
        //6. 实现对数组的赋值
//        arr[0] = 10;
//        arr[1] = 20;
//        arr[2] = 30;
        //7. 循环实现数组赋值
        for (int i = 0; i < arr.length; i++) {
            arr[i] = i * 10;
        }
        for (int i = 0; i < arr.length; i++) {
            System.out.println(arr[i]);
        }
    }
}
```

***

```java
package day2;
//编程实现一维数组的增删改查
public class demo3 {
    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 0};//静态数组
        //1. 添加元素
        arr[4] = 5;
        System.out.println(arr[4]);
        System.out.println("----------------");
        //2. 删除元素
        arr[4] = 0;
        System.out.println(arr[4]);
        System.out.println("----------------");
        //3. 修改元素
        arr[4] = 5;
        System.out.println(arr[4]);
        System.out.println("----------------");
        //4. 查询元素
        System.out.println(arr[4]);
        System.out.println("----------------");
        for (int i = 0; i < arr.length; i++) {
            System.out.println(arr[i]);
        }
    }
}
```

***

### 二维数组

#### 1. 基本概念

一维数组本质上就是一段连续的存储单元，用于存放多个类型相同的数据内容;

**二维数组本质上就是由多个一维数组组成(摞在)的数组**,每个元素都是一个一维数组，而一维数组中的每个元素才是数据内容;

简单的理解就是,'数组'的'数组'.

#### 2. 声明方式

数据类型[] [] 数组名称 = {{初始值1,初始值2,...},...}

```java
package day2;
//编程实现二维数组
public class demo4 {
    public static void main(String[] args) {
        //1. 定义二维数组
        int[][] arr = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};//静态二维数组
        //2. 循环遍历二维数组
        //2.1 循环遍历二维数组的行
        for (int i = 0; i < arr.length; i++) {
            //2.2 循环遍历二维数组的列
            for (int j = 0; j < arr[i].length; j++) {
                System.out.println(arr[i][j]);
            }
        }
    }
}
```

### 面向对象编程的概念

#### 1. 什么是对象?

万物皆对象

#### 2. 什么事面向对象?

面向对象就是指以特征(属性)和行为的观点去分析现实世界中事物的方式。

#### 3. 什么是面向对象编程?

面向对象编程就是指先使用面向对象的方式进行分析，再使用意一门面向对象的编程语言进行翻译的过程。	

​	其中C语言是一门面向过程的编程语言.

​	其中C++语言是一门既面向过程又面向对象的编程语言.

​	其中Java语言是一门纯面向对象的编程语言.

[^]: **面向过程**：**把问题拆成步骤，一步步用函数实现**。

#### 4. 如何学好面向对象编程?

深刻理解面向对象编程的三大特征:封装、继承、多态.

### 类、对象以及引用

#### 1. 对象和类的概念 

对象是客观存在的实体，在Java语言体现为内存空间的一块区域.

类就是分类的概念，是对具有相同特征和行为的多个对象共性的抽象描述.在java语言中包含描述特征的成员变量和描述行为的成员方法，是创建对象的板。

#### 2. 类的定义

##### 2.1 类定义的语法格式

class 类名 {

​	类体;

}

**注意:**当类名由多个单词组成时，要求每个单词的首字母都要大写;

##### 2.2 成员变量定义的语法格式

calss 类名 {

​	数据类型 成员变量名 = 初始值;	//其中=初始值通常省略,但分号不能省略.

}

**注意:**当成员变量名由多个单词组成时，要求从第二个单词起每个单词首字母大写;

**扩展:**

​	局部变量 - 主要指在方法体中声明的变量，作用范围从声明开始到方法体结束

​	成员变量 - 主要指在方法体外类体内声明的变量，作用范围从声明到类体结束 

##### 2.3 对象的创建

语法格式

​	new 类名();

如:	new Person(); - 创建Person类型的对象,由于该对象没有名字因此叫做"匿名对象".

**注意事项:**

a. 当一个类定义完毕后，使用new关键字创建/构造对象的过程叫做类的实例化.

b. 创建对象的本质就是在内存中的堆区申请存储空间，来存放该对象独有的特征信息.

##### 2.4 引用

基本概念

​	在Java语言中使用引用数据类型声明的变量叫做引用型变量，简称为”引用”;

​	引用变量主要用于记录对象在堆区中的内存地址信息，便于下次访问。

语法格式:

​	类名 引用变量名; 

如:

​	Person p;  // 表示声明Person类型的引用变量p，本质上在栈区申请存储空间.

​	Person p =new Person();// 表示声明引用变量p来记录Person类型对象的地址信息.

引用变量名.成员变量名;

​	P.name = "xiaoming"; //表示使用引用变量p访问所指向堆区对象的姓名特征.

```java
package day2;
//面向对象类的定义和使用
public class demo5 {
    public static void main(String[] args) {
        //1. 创建对象
        Person p1 = new Person();
        //2. 使用对象
        p1.name = "张三";
        System.out.println(p1.name);
    }
}
```

#### 3.  成员变量

##### 3.1 语法格式

​	class 类名{

​		返回值类型 成员方法名(形参列表){

​				成员变量体;

​			}

​	}

**注意:** 

​	当成员变量名由多个单词组成时，通常要求从第二个单词起每个单词首字母大写.

##### 3.2 格式的详解

​	返回值类型

​		返回值主要指从方法体内向方法体外返回的数据内容。

​		返回值类型主要指返回值的数据类型，可以是基本数据类型，也可以是引用数据类型

#### 4. 方法

引用变量名.成员方法名(实参列表);

注意事项:

a. 实际参数列表主要用于对形式参数列表进行初始化操作，因此参数的个数、类型、顺序等都必须与形参列表保持一致;

b.  实参可以传递直接量、变量、表达式以及方法的调用等;

```java
package day2;
//成员方法的调用和成员变量的使用
public class demo6 {
    public static void main(String[] args) {

        //1. 创建对象
        Person p1 = new Person();
        //2. 使用对象的成员方法
        p1.showName();
        //3. 使用对象的成员变量
        System.out.println(p1.name);
    }
}
```

### 构造方法和方法重载

#### 1. 构造方法

##### 1.语法格式

​	class 类名{

​		类名(形参列表){

​			构造方法体;

​		}

​	}

**注意事项:**

a. 构造方法的名称与类名完全相同，没有返回值类型连void都不许有。

b. 当一个类中没有自定义任何形式的构造方法时，编译器会自动添加一个空构造方法，叫做默认/缺省构造方法，如:Person(){}

c. 若类中出现自定义构造方法，则编译器不再提供任何形式的构造方法

```java
package day2;
//编程实现point 类的
public class Point {
    //属性
    private int x;
    private int y;
    // 无参构造方法
    public Point(){
    }
    // 带参构造方法
    public Point(int x,int y){
        this.x = x;
        this.y = y;
    }
    public void show(){
        System.out.println("("+x+","+y+")");
    }

    public static void main(String[] args) {
        Point p = new Point(10,20);
        p.show();
    }
}
```

#### 2. 方法重载

##### 1. 基本概念

​	在Java语言中若方法的名称相同但参数列表不同，这样的方法之间构成重载关系。

##### 2. 体现方式

​	方法重载的主要形式有:参数的个数不同、参数的类型不同、参数的顺序不同，与形参变量名和返回值类型无关，但建议返回值类型最好相同.

​	判断方法是否重载的核心:调用能否区分.

#####  3. 实际意义

对于调用者来说只需要记住一个方法名就可以调用各种不同的版本实现不同的效果

***

### this关键字

#### 基本概念

在构造方法中this关键字代表当前正在构造的对象。

在成员方法中this关键字代表当前正在调用的对象。

##### **原理分析:**

​	当成员方法中访问成员变量时默认会加上this.(相当于汉语中"我的”)，当不同的引用调用同一个成员方法时会导致成员方法中的this不同，那么this.访问的结果随之不同.

##### **使用方法:**

a. 当形参变量和成员变量同名时，在构造方法或成员方法中通常优先使用形参变量.若希望使用成员变量就需要在变量名的前面加上this.进行说明.

b. 在构造方法的第一行使用this(实参)的方式可以调用本类中的其它构造方法.

```java
package day2;

public class Boy {
    String name;
    public Boy(){
    }
    public Boy(String name) {
        this.name = name;
    }
    void show() {
        System.out.println("boy name is " + name);
    }

    public static void main(String[] args) {
        //this关键字的原理:当成员方法中访问成员变量时默认会加上this.(相当于汉语中"我的")
        Boy b = new Boy("Tom");
        b.show();
        Boy b1 = new Boy("jack");
        b1.show();
    }
}
```

***

### 方法的传参和递归调用

#### 方法的传参过程

(1) main方法是程序的入口,为main方法中的局部变量开辟内存空间并初始化:

(2)调用max方法时为max方法的形参变量开辟内存空间;

(3)使用实参变量给形参变量进行赋值操作，执行max方法的方法体;

(4)当max方法结束后释放形参变量的内存空间:

(5)main方法中的res得到max方法的返回值然后继续向下执行;

(6)当main方法结束后释放局部变量的内存空间;

```java
package day2;
//编程实现参数传递过程的测试
public class demo7 {
    void show(int a)
    {
        a = 10;
        System.out.println("a = " + a);
    }
    public static void main(String[] args) {
        demo7 d = new demo7();
        int a = 5;
        d.show(a);
    }
}
```

a. 当基本数据类型的变量作为方法的参数传递时，形参变量的改变不会影响到实参;

b. 当引用数据类型的变量作为方法的参数传递时，形参变量指向的内容发生改变后会影响到实参变量指向的内容;

c. 当引用数据类型的变量作为方法的参数传递时，形参变量改变指向后再改变指定的内容时不会影响到实参变量指向的内容;

#### 递归调用

**在一个方法体的内部调用当前方法自身的形式，叫做递归。**

**使用事项:**

a. 必须找到递归的规律和退出条件.

b. 使用递归使得问题简单化而不是复杂化;

c. 若递归影响到程序的执行性能

***

### 1. 封装

#### 1.1 基本概念

​	通常情况下测试类可以对封装类中的成员变量进行赋值，若赋值的数据合法但不合理时，无论时编译阶段还是运行阶段都不会报错或者给出提示，此时与现实生活不符.

​	为了避免上述错误的发生，就需要对成员变量进行密封包装处理，该机制就叫做封装.换句话说，封装就是一种保证成员变量值合理性的机制。

#### 2.2 实现流程

a. 私有化成员变量，使用private关键字修饰;

b. 提供公有的get和set方法，在方法体中进行合理值的判断;

c. 在构造方法中调用set方法进行合理值的判断;

```java
package day3;

public class demo1 {
    //1. 私有化成员变量，使用private关键字修饰
    // private修饰成员变量表示私有的含义，该成员变量只能在本类的内部使用
    private String name ;
    private int age ;
    //2. 提供公有的get和set方法，并在方法体中进行合理值的判断
    // public修饰成员方法表示公有的，该方法可以在任意位置调用
    // 若方法的前面啥也不加表示默认权限，访问级别低于public
    public demo1(String name, int age) {
        this.name = name;
        this.age = age;
    }
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    public int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
    }
    public static void main(String[] args) {

    }
}
```

***

### 2. static关键字

#### 2.1 基本概念

​	通常情况下成员变量隶属于对象层级，每创建一个对象就需要申请独立的内存空间来存放该对象独立的成员变量信息，若所有对象的某个成员变量数值完全一样却又单独存放会造成内存空间的浪费。

​	为了解决上述问题，则使用static关键字修饰成员变量表达静态的含义，此时该成员变量由对象层级提升为类层级被所有对象共享，该成员变量随着类的加载准备就绪，与是否创建对象无关.

static关键字也可以修饰成员方法，推荐使用 类名. 的方式访问.

#### 2.2 使用方式

(1) 非静态的成员方法中既能访问非静态的成员也能访问静态的成员;

​	(成员:成员变量+成员方法，静态成员被所有对象共享)

(2) 在静态的成员方法中只能访问静态的成员不能访问非静态的成员;

​	(成员:成员变量+成员方法，调用静态方法时可能还没有创建对象)

(3) 只有隶属于类层级被所有对象共享的内容才可以使用static修饰;

​	(不能滥用static关键字)

```java
package day3;
//编程实现static
public class demo2{
    //静态成员变量
    static int a = 10;
    //静态成员方法
    static void show() {
        System.out.println("a=" + a);
    }
    public static void main(String[] args) {
        //静态成员方法调用
        demo2.show();
    }
}
```

***

### 继承

#### 基本概念

​	当多个类之间有相同的特征和行为时，可以将相同的内容提取出来组成一个公共类，让多个类吸收公共类中已有特征和行为而在多个类的内部编写自己独有特征和行为的方式叫做继承。

​	使用继承可以提高代码的复用性和扩展性以及可维护性。

​	在Java语言中使用extends(扩展)关键字来表达继承关系。

如:

public class Student extends Person - 表示Student类继承自Person类

其中Person类叫做基类、父类、超类

其中Student类叫做派生类、子类、孩子类

**注意事项:**

(1) 类可以继承父类的成员变量和成员方法，其中私有成员变量可以继承但不可以直接使用.子类不可以继承父类的构造方法和私有方法。

(2) 无论使用何种方式构造子类对象时，都会自动调用父类中的无参构造方法来初始化从父类中继承下来的成员变量，相当于在子类构造方法第一行增加代码:super()的效果

(3) 使用继承必须满足子类isa父类的逻辑关系，也就是不能滥用继承。

(4) Java语言中只支持单继承不支持多继承，也就是一个子类只能有一个父类，但一个父类可以有多个子类。

### 方法重写

若从父类中继承下来的方法不满足子类的需求时，就需要在中一样的方法来覆盖从父类中继承的版本，这种方式就叫做重写。
重写的原则:

​	a. 要求方法名相同、参数列表相同、返回值类型相同，从idk1.5开始允许返回子类类型.

​	b. 要求方法的访问权隔不能变小，可以相同或者变大。

​	c. 要求不能抛出更大的异常(异常机制)

### final关键字

**基本概念**

​	final本意为"最终的，不可更改的"，该关键字可以修饰类、成员方法、成员变量等

**使用方法**

(1) final关键字修饰类表示该类不能被继承。

​		**为了防止滥用继承带来的危害 .如:java.lang.String类等.**

(2) fina1关键字修饰成员方法表示该方法不能被重写但可以被继承。

​		**为了防止不经意间造成的方法重写 如:java.text.DateFormat类中的format方法等**

(3) final关键字修饰成员变量表示该成员变量必须初始化而且不能更改。

​	**为了防止不经意间造成数值的更改.如:java.lang.Thread类中的MAX PRIORITY等**



#### 扩展:

​	在以后的开发中很少单独使用static关键字或final关键字修饰成员变量，通常都是使用public static final共同修饰成员变量来表达常量的含义，常量的命名规则是:要求所有字母大写，不同单词之间采用下划线连接，如:public static final double PI = 3.14;

### 多态

**基本概念:**

​	多态主要指同一种事物表现出来的多种形态.

**语法格式:**	

​	父类类型 引用变量名 = new 子类类型();

如:	

​	Person pw = new Worker();

​	pw.show();

解析: 

​	编译阶段调用Person类中show方法，在运行阶段调用Worker类中重写以后的show方法

**多态的效果:**

(1) 当父类的引用指向子类的对象时，父类的引用可以直接调用父类独有的方法;

(2) 当父类的引用指向子类的对象时，父类的引用不可以直接调用子类独有的方法;

(3) 对于父子类都有的非静态成员方法来说，编译阶段调用父类版本，运行阶段调用子类重写以后的版本;

(4) 对于父子类都有的静态方法来说，编译和运行阶段调用父类版本，隶属于类层级，因此与指向的对象无关:

**引用数据类型之间的转换**

​	引用数据类型之间的转换分为:	自动类型转换	和	强制类型转换。

​	其中自动类型转换主要指从小范围到大范围之间的转换，也就是子类到父类的转换

​	其中强制类型转换主要指从大范围到小范围之间的转换，也就是父类到子类的转换

**注意:引用数据类型之间的转换必须发生在父子类之间，否则编译报错。**

​	若转换到的目标类型是子类类型但不是该引用真正指向的子类类型，则编译通过，运行阶段发生类型转换异常。

为了避免上述错误的发生，可以使用instanceof进行判断，具体格式如下:

​	if(引用变量名 instanceof数据类型)	------判断引用变量指向的对象是否为后面类型 	

**多态的意义:**

​	多态的实际意义在于可以屏蔽不同子类的差异性实现通用的编程，但可以调用不同的方法带来不同的结果。

### 抽象类

**基本概念:**

​	抽象方法就是指不能具体实现的方法，也就是没有方法体并使用abstract关键字修饰. 

​	抽象类就是指不能具体实例化的类，也就是不能创建对象并使用abstract关键字修饰.

**语法格式:** 

​	访问控制符 abstract 返回值类型 方法名称(形参列表);

**注意事项:**

(1) 抽象类中可以有成员变量、构造方法以及成员方法，

(2) 抽象类中可以有抽象方法也可以没有抽象方法;

(3) 拥有抽象方法的类必须是抽象类，因此严格来说，具有抽象方法并且使用bstract关键字修饰的类才算真正意义上的抽象类。

**实际意义:**

​	抽象类的意义不在于自身创建对象而在于被继承，个类继承抽象类后必须重写抽象类中的抽象方法，否则该类也变成抽象类。

​	也就是说抽象类对子类具有强制性和规范性，因此叫做模板设计模式。

### 接口

**基本概念:**

​	接口就是一种比抽象类还抽象的类，体现为所有成员方法都是抽象方法。
​	定义类的关键字是class，而定义接口的关键字是interface。
​	继承类的关键字是extends;而实现接口的关键字是implemets。

**类和接口之间的关系**

​	类和类之间的关系	使用extends关键字表达继承的关系	支持单继承

​	类和接口之间的关系	使用implemets关键字表达实现的关系	支持多实现

​	接口和接口之间的关系	使用extends关键字表达继承的关系	支持多继承

**抽象类和接口之间的区别**

(1) 定义抽象类的关键字是abstract class，而定义接口的关键字是interface。

(2) 继承抽象类的关键字是extends，而实现接口的关键字是implements。

(3) 继承抽象类支持单继承，而实现接口可以多实现。

(4) 抽象类中可以有构造方法，而接口中不可以有构造方法。

(5) 抽象类中可以有成员变量，而接口中只可以有常量。

(6) 抽象类中可以有成员方法，而接口中只可以有抽象方法。

(7) 不影响子类，而接口中增加方法通常都影响子类。抽象类中增加方法可以

(8) 从jdk1.8开始允许接口中出现非抽象方法，但需要使用default关键字修饰。

### 匿名内部类

**语法格式:**

​	接口/父类类型 引用变量名= new 接口/父类类型(){方法的重写};

**经验分享:**

​	当接口类型的引用作为方法的形参时，实参的传递方式有两种:

​	a. 自定义类实现接口，然后创建该类的对象作为实参传递;

​	b. 使用匿名内部类的语法格式来得到接口类型的引用作为实参传递;

### 内部类

**基本概念:**

​	当一个类的定义出现在另外一个类的类体中时，那么这个类叫做内部类，而这个内部类所在的类叫做外部类。

​	类中的内容:成员变量、成员方法、构造方法、静态成员、构造块和静态代码块、内部类

**实际作用:**

​	一个类存在的价值仅仅是为某一个类单独服务时，那么就可以将这个类定义为所服务类中的内部类，这样可以隐藏该类的实现细节并且可以方便的访问外部类的私有成员而不再需要提供公有的get和set方法。

**基本分类:**

​	普通内部类------直接将一个类的定义放在另外一个类的类体中。

​	静态内部类------使用static关键字修饰的内部类，隶属于类层级。

​	局部内部类------直接将一个类的定义放在方法体的内部时.

​					   ------作用范围是从声明开始一直到方法体结束.

### Object类

#### 常用的包

java.lang包 	- 该包是java语言的核心包,该包中的内容由java虚拟机自动导入

​						- 如:String类丶System类

java.util包	  - 该包是Java语言中的工具包，里面包含了大量的工具类和集合类等

​						- 如:Scanner类、Random类等

java.io包	    - 该包是Java语言中的输入输出包，里面包含了大量读写文件的类等

​					   - 如:File0utputStream类、FileInputStream类等

java.net包     - 该包是Java语言中的网络包，里面包含了大量网络编程的类等

​					   - 如:ServerSocket类、Socket类等

#### 基本概念

java.lang.0bject类是所有类层次结构的根类，任何类都是该类的直接或间接子类.

#### 常用方法

Object()	- 使用无参方式构造对象

boolean equals(Object obj)	- 用于判断调用对象是否与参数对象相等

​													- 该方法默认比较两个对象的地址，与==运算符结果相同。

   - 为了使得该方法比较两个对象的内容，则需要重写该方法。

​													- 若该方法重写后，则应该重写hashCode方法来维护hashCode方法的常规协定

int hashCode()	- 用于获取调用对象的哈希码值(内存地址的编号)。

​							  - 若调用equals方法的结果相等，则各自调用hashCode方法的结果相同。

​							  - 若调用equals方法的结果不相等，则各自调用hashCode方法的结果不相同。

​							  - 为了维护上述的常规协定与equals方法结果保持一致，就需要重写该方法。

String toString() 	- 用于获取对象的字符串形式。

​	- 该方法返回的字符串为:包名.类名@哈希码值的十六进制形式	

​	- 为了返回更有意义的数据内容则需要重写该方法

​	- 当字符串内容与引用进行连接时，自动调用toString()方法

​	- 当使用print或println()方法打印引用时，会自动调用toString()方法

### 包装类和数学处理类

#### 基本概念

由于Java语言是一门纯面向对象编程语言，而8种基本数据类型声明的变量并不是对象,为了满足Java语言的特性就需要对这些变量进行对象化处理，而实现该功能的相关类就叫做包装类。

#### 包装类分类

int 	=>	java.lang.Integer类

char  =>	java.lang.Character类

其它类型对应的包装类就是将首字母变成大写

##### Integer类

**基本概念**

java.lang.Integer类是int类型的包装类，该类由fina1关键字修饰表示不能被继承。
里面包含了一个int类型的成员变量。

**常用的方法**

Integer(int value)	-	根据参数指定的整数构造对象

Integer(String s)	-	根据参数指定的字符串构造对象

该类重写了equals()、hashCode()、toString()方法

static Integer value0f(int i)- 根据参数指定的整数返回对应的Integer对象。

static int parseInt(String s)-用于将String类型转换为int类型并返回。

#### 数学处理类

**BigDecimal类**

由于float类型和double类型的运算可能会有误差，为了实现精确运算则需要借助java.math.BigDecimal类型加以描述。

### String类

#### 基本概念

java.lang.String类用于描述字符串，Java应用程序中所有字符串字面值都可以作为String类型的对象加以描述，如:"abc"等。

该类描述的字符串内容是个常量，一旦创建完毕后则不能更改，因此可以被共享。

#### 常量池

由于String类型描述的字符串内容是个常量不可改变，因此Java虚拟机提供了一个常量池，当Java程序中出现字符串内容时就放入常量池中，若后续出现重复的字符串内容则直接使用池中已有的对象而不需再次创建，从而提高了性能。

### Srting类的常用方法

char charAt(int index)	- 方法charAt用于返回字符串指定位置的字符。参数index表示指定的位置

int length()	- 返回字符串字符序列的长度

```java
package day3;
//编程使用charAt和length方法
public class demo4 {

    public static void main(String[] args) {
        //1. 创建一个String类型的对象
        String str = "Hello";

        //2. 获取字符串的长度
        int length = str.length();//    5
        //3. 获取字符串中每个字符
        for(int i = 0; i < length; i++){
            char c = str.charAt(i);// H  e  l  l  o
            System.out.println(c);
        }
    }
}
```

**String向int 类型的转换方式:**

第一种:调用Integer类中的parseInt方法进行转换即可

第二种:取出字符串中的每个字符并转换为整数数据再合并起来

```java
package day3;

public class demo5 {
    public static void main(String[] args) {
        //String向int类型的转换方法
        //第一种:调用Integer类中的parseInt方法进行转换即可
        String s = "123";
//        int i = Integer.parseInt(s);
        //第二种:取出字符串中的每个字符并转换为整数数据再合并起来
        int sum = 0;
        for(int i= 0; i < s.length(); i++){
            char c = s.charAt(i);
            int a = c - '0';
            sum = sum * 10 + a;
        }
    }
}
```

 基本方法:

boolean contains(CharSequence s)	- 用于判断当前字符串是否包含参数指定的内容

String toLowerCase()	- 返回字符串的小写形式

String toUpperCase()	- 返回字符串的大写形式

String trim()	- 返回去掉前导和后继空白的字符串

boolean startsWith(String prefix)	- 判断字符串是否以参数字符串开头

boolean endsWith(String suffix)	- 判断字符串是否以参数字符串结尾

```java
package day3;

public class demo6 {
    public static void main(String[] args) {
        //1. 创建一个String类型的对象
        String str = "Hello";
        //boolean contains(CharSequence s)用于判断当前字符串是否包含参数指定的内容
        boolean b = str.contains("l");
        System.out.println(b);// true
        //String toLowerCase()	- 返回字符串的小写形式
        String s1 = str.toLowerCase();
        System.out.println(s1);// hello
        //String toUpperCase()	- 返回字符串的大写形式
        String s2 = str.toUpperCase();
        System.out.println(s2);// HELLO
        //String trim()	- 返回去掉前导和后继空白的字符串
        String s3 = "   Hello   ";
        String s4 = s3.trim();
        System.out.println(s4);// Hello
        //boolean startsWith(String prefix)	- 判断字符串是否以参数字符串开头
        boolean b1 = str.startsWith("H");
        System.out.println(b1);// true
        //boolean endsWith(String suffix)	- 判断字符串是否以参数字符串结尾
        boolean b2 = str.endsWith("o");
        System.out.println(b2);// true
    }
}
```

**String类中的equals方法**

String类重写了继承自Object的equals方法，其逻辑为:字符序列相同的String对象equals返回true。

通常使用equals方法判断两个字符串的字符序列是否相同。

String还提供equalslgnoreCase方法，该方法在判断时将忽略大小写。

**方法indexOf**

indexOf方法用于实现在字符串中检索另外一个字符串。

String提供几个重载的indexOf方法:

int indexOf(String str)	- 在字符串中检索str，返回其第一出现的位置，如果找不到则返回-1

int indexOf(String str,int fromIndex)	- 类似indexOf(String)，但是是从字符串的fromIndex位置开始检索

```java
package day3;
//编程使用indexOf方法，判断字符串中"java"出现的位置
public class demo7 {
    public static void main(String[] args) {
        //1. 创建一个String类型的对象
        String str = "hello java hello java hello java";
        // int indexOf(String str)	- 在字符串中检索str，返回其第一出现的位置，如果找不到则返回-1
        int index = str.indexOf("java");
        System.out.println(index);// 6
        // int indexOf(String str,int fromIndex)	- 类似indexOf(String)，但是是从字符串的fromIndex位置开始检索
        int index2 = str.indexOf("java", 7);
        System.out.println(index2);// 17
    }
}
```

**方法substring**

substring方法用于返回一个字符串的子字符串。

substring常用重载方法定义如下:

String substring(int beginIndex,int endindex)	- 返回字符串中从下标beginIndex(包括)开始到endIndex(不包括)结束的子字符串

String substring(int beginindex)	- 返回字符串中从下标beginIndex(包括)开始到字符串结尾的子字符串

```java
package day3;
//编程使用subString方法截取字符串
public class demo8 {
    public static void main(String[] args) {
        //1. 创建一个String类型的对象
        String str = "hello java hello java hello java";
        // String substring(int beginIndex,int endindex)	- 返回字符串中从下标beginIndex(包括)开始到endIndex(不包括)结束的子字符串
        String sub = str.substring(6, 11);
        System.out.println(sub);// java
        //String substring(int beginindex)	- 返回字符串中从下标beginIndex(包括)开始到字符串结尾的子字符串
        String sub1 = str.substring(6);
        System.out.println(sub1);// java hello java hello java
    }
}
```

***

### StringBuilder类和StringBuffer类

​	由于String类型描述的字符串内容是个常量不可更改，当程序中出现大量类似的字符串时需要单独存放从而浪费内存空间，若希望使用一块内存空间进行存储并且可以修改字符串内容，则应该使用StringBuilder类和StringBuffer类。

​	其中StringBuffer类从idk1.0开始存在，该类支持线程安全，因此访问的效率比较低

​	其中StringBuilder类从jdk1.5开始存在，该类不支持线程安全，访问的效率比较高

**StringBuilder类的常用方法**

StringBuilder append(String str)	- 追加字符串

StringBuilder insert(int offset, String str)	- 插入字符串

StringBuilder delete(int start, int end)	- 删除字符串

StringBuilder replace(int start, int end, String str)	- 替换字符串

StringBuilder reverse()	- 字符串反转

***

### 日期相关的类

**Date类**

java.uti1.Date类用于描述特定的瞬间，可以精确到毫秒。

**SimpleDateFormat类**

java.text.SimpleDateFormat类主要用于实现日期和文本之间的相关转换。

**Calendar类**

iava.util.Calendar类用于取代Date类来描述年月日时分秒的特定瞬间。

### 集合(容器)框架

当需要在程序中记录单个数据内容时，则声明一个变量即可;

当需要在程序中记录多个类型相同的数据内容时，则声明一个一维数组即可:

当需要在程序中记录多个类型不同的数据内容时，则构造一个对象即可;

当需要在程序中记录多个类型相同的对象时，则声明当一个对象数组即可;

**当需要在程序中记录多个类型不同的对象时，则声明一个集合即可;**

在Java语言中集合框架的顶层是:java.uti1.Gollection集合 和 java.util.Map集合
其中Collection集合中操作元素的基本单位是:单个元素。
其中Map集合中操作元素的基本单位是:单对元素。

在以后的开发中很少直接使用Collection集合，而是使用该集合的子集合:List集合、Queue集合、Set集合等。

#### Collection集合

java.uti1.Collection集合是集合框架的根接口，其它接口是该接口的子接口。

**方法:**

```java
package day3;

import java.util.ArrayList;

public class demo9 {
    public static void main(String[] args) {
        //创建一个集合对象
        ArrayList<String> list = new ArrayList<String>();
        //1. boolean add(E e)  - 向集合中添加对象
        list.add("hello");
        //2. boolean contains(Objecto) - 判断是否包含指定对象
        boolean b = list.contains("hello");// true
        //3. boolean remove(Object o)  - 从集合中删除对象
        boolean b1 = list.remove("world");
        //4. void clear()  - 清空集合
        list.clear();
        //5. int size()    - 返回包含对象的个数
        int size = list.size();
        //6. boolean isEmpty() - 判断是否为空
        boolean b2 = list.isEmpty();
    }
}
```

#### List集合

iava.uti1.List集合是Collection集合的子集合，该集合中**元素有先后次序且允许重复**

该集合的主要实现类有:ArrayList类、LinkedList类、Stack类、Vector类等

其中ArrayList类的底层是采用动态数组进行数据管理，访问方便，增删不方便。

其中LinkedList类的底层是采用链表进行数据管理，增删方便，访问不方便。

其中Stack类主要用于描述具有后进先出特征的数据结构，叫做栈，last in first out(后进先出).该类的底层是采用数组进行数据的管理

其中Vector类的底层采用数组进行数据的管理，与ArrayList类相比属于线程安全的类.因此效率比较低，在以后的开发中推荐使用ArrayList类取代之。

**List集分的常用方法**

void add(int index,E element)	- 向集合中指定位置添加元素

boolean addAll(int index, Collection<?extends E> c)	- 向集合中添加所有元素

E get(int index)	- 从集合中获取指定位置元素

E set(int index, E element)	- 修改指定位置的元素

E remove(int index)	- 删除指定位置的元素

```java
package day4;

import java.util.ArrayList;
import java.util.List;

public class demo1 {
    public static void main(String[] args) {
        //**List集分的常用方法**
        List<String> list = new ArrayList<>();
        //void add(int index,E element)	- 向集合中指定位置添加元素
        list.add(0,"hello");//[hello]
        //boolean addAll(int index, Collection<?extends E> c)	- 向集合中添加所有元素
        list.addAll(1,list);//[hello, hello]
        //E get(int index)	- 从集合中获取指定位置元素
        String s = list.get(0);// hello
        //E set(int index, E element)	- 修改指定位置的元素
        String s1 = list.set(0,"world");// hello
        //E remove(int index)	- 删除指定位置的元素
        String s2 = list.remove(0);// world
    }
}
```

### 泛型机制

**基本概念**

​	通常情况下集合中可以存放不同类型的对象，本质上是将这些对象全部看做0bject类型放入的，因此从集合中取出元素时也是0bject类型，为了表达元素最真实的数据类型就需要强制类型转换，而强制类型转换可能发生类型转换异常.

​	为了避免上述错误的发生，从jdk1.5开始提出泛型机制，也就是在集合名称的右侧使用<数据类型>的方式明确要求该集合可以存放的元素类型，若放入其它类型则编译报错如:

List lt1=new LinkedList();	 - 可以放入任意类型对象，取出麻烦

List<String>= new LinkedList<String>():	- 只能放入String类型，取出方便

**原理分析**

泛型的本质就是参数化类型，也就是让数据类型作为参数传递，集合定义中的E相当于形式参数负责占位，而使用集合时<>中的数据类型相当于实际参数负责给形式参数初始化当初始化完毕后所有E被替换为实际参数表示的类型进行使用。

### Queue集合(队列)

**基本概念**

​	java.uti1.Queue集合是Collection集合的子集合，与List集合是平级关系。

​	该集合的主要实现类是:LinkedList类，因为该类在增删方面有一定的优势。

​	该集合用于描述具有先进先出特征的数据结构，叫做队列(first in first out)

**Queue集舍的方法**

boolean offer(E e)	- 将一个对象添加至队尾，若添加成功则返回true

E poll()	- 从队首删除并返回一个元素

E peek()	- 返回队首的元素(但并不删除)

```java
package day4;

import java.util.LinkedList;
import java.util.Queue;

public class demo2 {
    public static void main(String[] args) {
        //**Queue集舍的方法**
        Queue<String> queue = new LinkedList<>();
        //boolean offer(E e)	- 将一个对象添加至队尾，若添加成功则返回true
        System.out.println(queue.offer("hello"));// true
        //E poll()	- 从队首删除并返回一个元素
        System.out.println(queue.poll());// hello
        //E peek()	- 返回队首的元素(但并不删除)
        System.out.println(queue.peek());// null
    }
}
```

### Set集合

**基本概念**

​	java.util.Set集合是Collection集合的子集合，与List集合以及Queue集合平级关系

​	该集合与List集合的主要区别在于:元素没有先后次序并且不允许重复的元素。

​	该集合的主要实现类有:HashSet类和Treeset类

​	其中HashSet类的底层采用哈希表进行数据管理的。

​	其中TreeSet类的底层采用二叉树进行数据管理的。

**常用的方法**

参考Collection集售的方法即可

**Set集合的遍历**

​	所有Collection的实现类都实现了其iterator方法，该方法返回一个lterator接口类型的对象，用于实现对集合元素的迭代遍历。

Iterator接口的主要方法有:

boolean hasNext()	- 判断集合中是否有可以迭代/访问的元素

E next()	- 用于取出一个元素并指向下一个元素

void remove()	- 用于删除访问到的最后一个元素

**注意:**

当使用迭代器迭代集合中的所有元素时，若使用集合中的remove方法来删除元素，则会出现ConcurrentModificationException并发修改异常，以后的开发中应该使用迭代器的remove方法来删除元素。

#### 增强的for循环(for each结构)

**语法格式**

for(元素类型 变量名 : 数组名.集合名){

​		循环体;

}

**执行流程**

不断地从数组或集合中取出一个元素并赋值给变量并执行循环体，直到处理完毕所有元素为止.

```java
package day4;
//编程使用for each循环遍历数组
public class demo3 {
    public static void main(String[] args) {
        int[] arr = {1,2,3,4,5};
        //for each循环
        for(int i : arr){
            System.out.println(i);
        }
    }
}
```

遍历Set集合的方式有三种:toString()、for each结构、迭代器方式

遍历List集合的方式有四种:除了上述3种方式外，还有get方法。

***

### Map集合

**基本概念**

java.util.Map<K,V>集合中操作元素的基本单位是:单对元素，其中类型参数如下:

​	K-此映射所维护的键(key)的类型

​	V-映射值(value)的类型

该集合中不允许出现重复的键，每个键最多只能映射到一个值。

该集合的主要实现类有:HashMap类和TreeMap类:

其中HashMap类的底层是采用哈希表进行数据管理的.

其中TreeMap类的底层是采用二叉树进行数据管理的.

**Map的常用方法**

V put(k key, V value);	- 将Key-Value对存入Map，若集合中已经包含该Key，则替换该Key所对应的Value，返回值为该Key原来所对应											的Value，若没有则返回null

V get(Object key);	- 返回与参数Key所对应的Value对象，如果不存在则返回null

boolean containsKey(Object key);	-判断集合中是否包含指定的Key。

boolean containsValue(Object value);	- 判断集合中是否包含指定的Value。

```java
package day4;

import java.util.HashMap;
import java.util.Map;

public class demo4 {
    public static void main(String[] args) {
        //**Map的常用方法**
        Map<String,String> map = new HashMap<>();
        //V put(k key, V value)
        map.put("1","hello");//{1=hello}
        //V get(Object key)
        System.out.println(map.get("1"));//hello
        //boolean containsKey(Object key)-判断集合中是否包含指定的Key。
        System.out.println(map.containsKey("1"));//true
        //boolean containsValue(Object value)- 判断集合中是否包含指定的Value。
        System.out.println(map.containsValue("hello"));//true
    }
}
```

**Map集合的性能调优**

Capacity:容量,hash表里bucket(桶)的数量,也就是散列数组大小.

Initial capacity: 初始容量,创建hash表的时 初始bucket的数量,默认构建容量为16.也可以使用特定容量.

Size: 大小,当前散列表中存储数据的数量.

Load factor : 加载因子,默认值C75(就是75%),当向散列表增加数据时如果size/capacity的值大于Load factor则发生扩容并且重新散列						(rehash).

性能优化: 加载因子较小时候散列查找性能会提高,同时也浪费了散列桶空间容量.0.75是性能和空间相对平衡结果,在创建散列表时候指定合理容量,减少rehash提高性能,

### 异常机制

**基本概念:**

​	异常就是"不正常"的含义，在Java语言中用于表示运行阶段发生的错误。

​	java. lang. Throwable类是Java语言中所有错误(Error)和异常(Exception)的超类。

​	其中Error类主要用于描述比较严重无法编码解决的问题，如:JVM挂了。

​	其中Exception类主要用于描述比较轻微可以编码解决的问题，如:0作为除数。

**基本分类:**

java.lang.Exception类是所有异常类的超类，主要分为以下两大类:

​	RuntimeException-运行时异常，也叫作非检测性异常

​	IOException和其它异常-其它异常，也叫作检测性异常

​		- 所谓检测性异常就是在编译阶段能够被编译器检测出来的异常

​	其中RuntimeException类的主要子类:

​		ArithmeticException-算术异常

​		ArrayIndex0ut0fBoundsException-数组下标越界异常

​		NullPointerException-指针异常

​		ClassCastException-类型转换异常

​		NumberFormatException-数字格式异常

**注意:**

​	当程序执行过程中发生异常但没有手动处理时:由Java虚拟机采用默认方式处理，而默认处理方式就是:打印异常名称、异常原因、异常发生的位置等并终止程序。

#### 异常的避免

​	在以后的开发中尽量使用if条件判断来避免异常的发生

#### 异常的捕获

**语法格式:**

try {

​		编写可能发生异常的语句.

}

catch(异常类型 变量名){

​	编写针对该异常的处理语句;

}

...

finally{

​	编写无论是否发生异常都应该执行的语句;

}

```java
package day4;
//异常的捕获
public class dmeo5 {
    public static void main(String[] args) {
        // try {}catch(){}finally{}
        try {
            //编写可能发生异常的语句.
            int a = 10;
            int b = 0;
            int c = a / b;
        }
        catch (Exception e) {
            //编写针对该异常的处理语句;
            System.out.println("异常信息：" + e.getMessage());
        }
        //编写无论是否发生异常都应该执行的语句;
        finally {
            System.out.println("程序结束");
        }
    }
}
```

注意: 

a. 当需要编写多个catch分支时，切记小类型的异常应该放在大类型异常的上面。

b. finally主要用于编写善后处理的语句，如:关闭已经打开的文件等。

#### 异常的抛出:

**基本概念**

在某些特殊情况下产生的异常无法处理或者不便于处理时，就可以将该异常转移给该方法的调用者，这种方式就叫做异常的抛出。

**语法格式:**

访问权限 返回值类型 方法名称(形参列表)throws 异常类型1，异常类型2,...{}

**方法重写的原则**

a. 要求方法名相同、参数列表相同、返回值类型相同，从jdk1.5开始允许返回子类类型

b. 要求方法的访问权限不能变小，可以相同或者变大

c. 要求不能抛出更大的异常

#### 自定义异常

**基本概念:**

虽然Java官方提供了大量的异常类，但一定不会包含所有开发中可能出现的异常，在Java程序中若需要表达特定问题的特定异常时，就需要程序员自定义异常来描述。

**实现流程:**

a. 自定义xxxxException继承自Exception类或者其子类;

b. 提供两个版本的构造方法:无参构造方法 和 字符串作为参数的构造方法

### File类

**基本概念**

java.io.File类主要用于描述文件和且录的路径信息，可以获取名称、大小等属性信息

```java
package day4;

import java.io.File;

public class demo6 {
    public static void main(String[] args) {
        //1. 构造File类型的对象描述c:/a.txt文件
        File f1 = new File("C:\\Users\\Administrator\\Desktop\\code\\day4\\demo1.java");
        //2. 判断文件是否存在，若存在则获取相关信息并打印出来
        if(f1.exists()){
            System.out.println("文件名：" + f1.getName());
            System.out.println("文件大小: "+ f1.length());
            //获取文件的绝对路径
            System.out.println("文件的绝对路径：" + f1.getAbsolutePath());
        }else {
            System.out.println("文件不存在");
        }
    }
}
```

**常用的方法**

绝对路径 - 主要指以根目录开始的路径信息，如:c:/...	d:/.	/...

相对路径 - 主要指以当前工作目录开始的路径信息，如:./...

​				- . 表示当前目录	.. 表示当前目录的上一级目录

​				-  在以后得开发中尽量使用相对路径

```java
package day4;

import java.io.File;

public class demo7 {
    public static void main(String[] args) {
        //file类实现目录的创建和删除
        String path = "d:\\a\\b\\c";
        File file = new File(path);
        if(file.exists()){
            file.delete();
        }else{
            file.mkdirs();
        }
        System.out.println("目录创建成功");
    }
}
```

***

### IO流

**基本概念:**

I/0就是Input/0utput的简写，也就是输入输出的含义。

I/0流就是像流水一样不间断地读写状态，

**基本分类:** 

按照数据读写的基本单位不同分为 字节流 和 字符流。

其中字节流主要指以字节为单位进行读写的流，可以处理任意类型的文件;

其中字符流主要指以字符(2个字节)为单位进行读写的流，只能处理文本文件;

按照数据流动的方向不同分为:	输入流	和	输出流	(站在程序的角度)。

其中输入流主要指从文件中读取数据内容输入到程序中，也就是读文件;

其中输出流主要指将程序中的数据内容输出到文件中，也就是写文件;

File0utputStream类

**基本概念**

iava.io.File0utputStream类主要用于将图像数据之类的原始字节流写入输出流中.

```java
package day4;

public class demo8 {
    public static void main(String[] args) throws Exception {
        // 2.使用输出流写入数据到文件中
        java.io.FileOutputStream fos = new java.io.FileOutputStream("test.txt");
        fos.write(97);           // 写入整数97 - 'a' 按照文本显示就变成了'a'
        fos.write('9');          // 写入字符'9' 跟在a的后面
        fos.write('7');          // 写入字符'7' 跟在9的后面
        // 向输出流中写入整个字节数组 "hello"
        fos.write("hello".getBytes());

        System.out.println("写入数据成功！");
        // 3.关闭流对象并释放有关的资源
        fos.close();
    }
}
```

**FilelnputStream类**

**基本概念**

java.io. FileInputStream类主要用于从输入流中读取图像数据之类的原始字节流。

```java
package day4;

public class demo9 {
    public static void main(String[] args) {
        try {
            // 1.构造FileInputStream类型的对象与test.txt文件关联
            java.io.FileInputStream fis = new java.io.FileInputStream("test.txt");

            // 2.通过输入流从文件中读取数据内容
            int res = fis.read();
            System.out.println("读取到的单个字节是: " + res);

            // 使用字节数组来读取文件中的所有内容
            byte[] bArr = new byte[20];
            // 期望通过输入流读取bArr.length个字节的数据内容
            // 放入数组bArr中下标从3开始的索引位置
            res = fis.read(bArr, 3, bArr.length - 3);
            System.out.println("读取到的数据内容是: " + new String(bArr)
                + ", 实际读取到的数据大小是: " + res);

            // 3.关闭流对象并释放有关的资源
            fis.close();
        } catch(Exception e) {
            e.printStackTrace();
        }
    }
}
```

```java
package day4;

public class demo10 {
    public static void main(String[] args) {
        try {
            // 1.构造FileInputStream类型的对象与test.txt文件关联
            java.io.FileInputStream fis = new java.io.FileInputStream("test.txt");
            // 2.构造FileOutputStream类型的对象与copy.txt文件关联
            java.io.FileOutputStream fos = new java.io.FileOutputStream("copy.txt");
            // 3.不断地从输入流中读取一个字节写入到输出流中
            System.out.println("正在玩命地拷贝...");
            int res = 0;
            while((res = fis.read()) != -1) {
                fos.write(res);
            }
            System.out.println("拷贝文件成功！");
            // 4.关闭流对象并释放有关的资源
            fos.close();
            fis.close();
        } catch(Exception e) {
            e.printStackTrace();
        }
    }
}
```

***

**BufferedWriter类**

**基本概念:**

java.io.Bufferedwriter类主要用于向输出流中写入单个字符、字符数组以及字符串

**常用方法:**

```java
package day4;

public class demo11 {
    public static void main(String[] args) throws Exception {
        // 创建BufferedWriter对象，关联文件output.txt
        java.io.BufferedWriter bw = new java.io.BufferedWriter(
            new java.io.FileWriter("output.txt")
        );

        // 1. 写入单个字符到输出流中
        bw.write('A'); // 写入字符A

        // 2. 写入字符数组的一部分到输出流中
        char[] cbuf = {'你', '好', '，', 'J', 'a', 'v', 'a', '!'};
        bw.write(cbuf, 2, 3); // 写入'，Ja'

        // 3. 写入整个字符数组到输出流中
        bw.write(cbuf); // 写入"你好，Java!"

        // 4. 写入字符串到输出流中
        bw.write("Hello, BufferedWriter!");

        // 5. 写入一个行分隔符
        bw.newLine();
        bw.write("新的一行");

        // 6. 关闭流对象并释放资源
        bw.close();
    }
}
```

**BufferedReader类**

java.io.BufferedReader类主要用于从输入流中读取单个字符、字符数组以及一行字符串内容。

**常用方法:**

```java
package day4;

public class demo12 {
    public static void main(String[] args) throws Exception {
        // 创建BufferedReader对象，关联文件output.txt
        java.io.BufferedReader br = new java.io.BufferedReader(
            new java.io.FileReader("output.txt")
        );

        // 1. 读取单个字符
        int ch = br.read();
        System.out.println("读取到的单个字符: " + (char)ch);

        // 2. 读取字符数组的一部分
        char[] cbuf = new char[10];
        int num = br.read(cbuf, 2, 5); // 从下标2开始，最多读取5个字符
        System.out.println("读取到的字符数组部分: " + new String(cbuf) + ", 实际读取个数: " + num);

        // 3. 读取满整个字符数组
        char[] cbuf2 = new char[8];
        int num2 = br.read(cbuf2);
        System.out.println("读取满数组: " + new String(cbuf2) + ", 实际读取个数: " + num2);

        // 4. 读取一行字符串
        String line = br.readLine();
        System.out.println("读取到的一行: " + line);

        // 5. 关闭流对象并释放资源
        br.close();
    }
}
```

***

**PrintStream类**

**基本概念**

iava.io.PrintStream类主要用于方便地打印各种数据内容并且自动刷新。

```java
package day4;

public class demo13 {
    public static void main(String[] args) throws Exception {
        // 创建PrintStream对象，关联文件print.txt，自动刷新
        java.io.PrintStream ps = new java.io.PrintStream(
            new java.io.FileOutputStream("print.txt"), true
        );

        // 打印各种数据类型内容
        ps.println(123); // 打印整数
        ps.println('A'); // 打印字符
        ps.println("Hello, PrintStream!"); // 打印字符串
        ps.println(); // 换行
        ps.println(3.14); // 打印浮点数并换行
        ps.println(true); // 打印布尔值并换行

        // 自动刷新：每次println/print后都会自动刷新到文件

        // 关闭流对象
        ps.close();
    }
}
```

**ObjectOutputStream类**

**基本概念:**

java. io.0bject0utputStream类主要用于将Java语言中的对象整体写入输出流中

只能将支持 java.io.Serializable 接口的对象写入流中

类通过实现 java.io.Serializable 接口以启用其序列化功能

所谓序列化就是指将一个对象相关的所有信息有效组织成字节序列的转化过程

**ObjectInputStream类**

**基本概念:**

java.io.0bjectInputStream类主要用于从输入流中一次性将一个对象的内容读取出来

```java
package day4;

public class demo14 {
    // 静态内部类
    static class Person implements java.io.Serializable {
        String name;
        int age;
        public Person(String name, int age) {
            this.name = name;
            this.age = age;
        }
        public String toString() {
            return "Person{name='" + name + "', age=" + age + "}";
        }
    }

    public static void main(String[] args) throws Exception {
        // 1. 使用ObjectOutputStream将对象写入文件
        java.io.ObjectOutputStream oos = new java.io.ObjectOutputStream(
            new java.io.FileOutputStream("person.obj")
        );
        Person p1 = new Person("张三", 20);
        oos.writeObject(p1); // 序列化对象
        oos.close();

        // 2. 使用ObjectInputStream从文件读取对象
        java.io.ObjectInputStream ois = new java.io.ObjectInputStream(
            new java.io.FileInputStream("person.obj")
        );
        Person p2 = (Person) ois.readObject(); // 反序列化对象
        System.out.println("读取到的对象: " + p2);
        ois.close();
    }
}
```

**经验分享:**
	当需要写入多个对象到文件中时，建议先将多个对象放入一个集合对象中，然后将集合对象看做一个整体只需要调用一次write0bject方法就可以写入所有内容，此时只需要调用一次readObject方法就可以将所有内容读取出来，这样就避免了通过返回值来判断是否读取到文件的末尾。

**transient关键字**

transient是Java语言的关键字，用来表示一个域不是该对象串行化的一部分。当一个对象被串行化的时候，transient型变量的值不包括在串行化的表示中，然而非transient型的变量是被包括进去的。

```java
package day4;

public class demo15 {
    // 静态内部类，含有transient字段
    static class User implements java.io.Serializable {
        String username;
        transient String password; // 使用transient修饰，序列化时不会被保存
        public User(String username, String password) {
            this.username = username;
            this.password = password;
        }
        public String toString() {
            return "User{username='" + username + "', password='" + password + "'}";
        }
    }

    public static void main(String[] args) throws Exception {
        // 1. 序列化对象到文件
        java.io.ObjectOutputStream oos = new java.io.ObjectOutputStream(
            new java.io.FileOutputStream("user.obj")
        );
        User user1 = new User("admin", "123456");
        oos.writeObject(user1);
        oos.close();

        // 2. 反序列化对象
        java.io.ObjectInputStream ois = new java.io.ObjectInputStream(
            new java.io.FileInputStream("user.obj")
        );
        User user2 = (User) ois.readObject();
        System.out.println("反序列化后的对象: " + user2);
        ois.close();
    }
}
```

***

### 线程

**基本概念**

程序 -数据结构 +算法，主要指存放在硬盘上的可执行文件。

进程 -主要指运行在内存中的程序。

目前主流的操作系统都支持多进程，为了使得操作系统能够同时执行多个任务.但进程是重量级的，新建进程对系统的资源消耗比较大，因此进程的数量比较局限。

