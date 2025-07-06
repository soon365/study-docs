# 一、JAVA编程基础与程序设计

## 1.1 JAVA程序开发入门

### 1.1.1 计算机的基本概念

#### 1.1.1.1 计算机的体系结构（常识）

**基本概念：**
计算机(Computer)是一种能够按照预先存储的程序自动、高速地进行信息处理的电子设备，广泛应用于科学计算、数据处理等领域。计算机系统由硬件系统和软件系统组成。

计算机硬件是客观存在的各种计算机相关设备，而计算机的软件是用于控制各种硬件设备完成 各种功能。

**硬件与软件：**
- 硬件：物理设备（如**CPU**、**内存**、**硬盘**等）
- 软件：控制硬件执行功能的程序集合

**常见硬件：**

- CPU：**中央处理器**，处理指令和数据
- 内存：临时存储运行中的程序
- 硬盘：长期数据存储，CPU不能直接访问硬盘中的数据，因此效率比较低
- 外设：显示器、鼠标等

**laptop-fsfnhr7j\heshaobin.zz**  是当前登录系统的 **设备名和用户名**：![](C:\Users\heshaobin.zz\AppData\Roaming\Typora\typora-user-images\image-20250628170723612.png)

**存储单位换算：**
- 1TB = 1024GB
- 1GB = 1024MB
- 1MB = 1024KB
- 1KB = 1024字节
- 1字节 = 8bit

**编码存储：**
- 英文字母：1字节
- 汉字：2字节

**思考题：**
为什么硬盘实际可用容量小于标称容量？

**解析：**
硬件厂商使用十进制(1000为基数)计算，操作系统使用二进制(1024为基数)计算。

| 标称容量 | 厂商计算(字节) | 系统显示容量 |
|---------|--------------|------------|
| 512GB   | 512×1000³    | ≈476GB     |

**常见软件分类：**

| 类型     | 示例 |
|---------|------|
| 系统软件 | Windows, Unix/Linux, iOS/Android |
| 应用软件 | QQ, 迅雷, 火狐浏览器等 |

##### 计算机体系结构：

用户 -> 应用软件 -> 系统软件 -> 硬件设备 -> 其中系统软件分为：内核(Kernel) 和 外壳(Shell)

![image-20250630144421301](C:\Users\heshaobin.zz\AppData\Roaming\Typora\typora-user-images\image-20250630144421301.png)



### 1.1.2 Java语言概述

#### 1.1.2.1 Java语言背景

Java由James Gosling及其团队于1991年在Sun Microsystems（现属Oracle）开发，最初命名为"Oak"，后改名为Java。其主要设计目标是解决跨平台兼容性问题，提出了"Write Once, Run Anywhere"(一次编写，到处运行)的理念。

**关键发展里程碑：**
- 1995年：Java 1.0正式发布
- 2004年：Java 5引入泛型、注解等重要特性
- 2014年：Java 8带来Lambda表达式和Stream API

**参考资源：**

1. Oracle官方Java文档：[https://docs.oracle.com/javase/](https://docs.oracle.com/javase/)
3. [Java语言发展简史](https://blog.csdn.net/dangerjxz/article/details/145632023)

#### 1.1.2.2 Java语言的主要版本

Java平台主要分为三个版本，针对不同的开发需求：

**1. Java SE (Java Platform, Standard Edition) - 标准版**

- 核心Java平台，包含语言基础、面向对象特性和核心类库
- 学习重点：语法规范、集合框架、I/O、多线程等
- 最新版本：Java 21（2023年9月发布）

**2. Java EE (Java Platform, Enterprise Edition) - 企业版**
- 现更名为Jakarta EE（2018年后）
- 企业级开发技术：Servlet/JSP、EJB、JPA等
- 主要用于开发B/S架构的企业级应用
- 代表框架：Spring、Spring Boot等

**3. Java ME (Java Platform, Micro Edition) - 微型版**
- 原用于嵌入式设备和移动设备开发
- 现状：随着Android和iOS的普及已逐渐淘汰
- 替代技术：Android开发(Kotlin/Java)、IoT开发等

> **注**：当前学习路径建议从Java SE开始，掌握基础后再选择Java EE(企业开发)或Android开发方向。

#### 1.1.2.3 开发环境搭建与使用（重点）

#### 1. JDK下载与安装

**官方下载渠道**：
- Oracle官网：[https://www.oracle.com/java/](https://www.oracle.com/java/)
- OpenJDK：[https://openjdk.org/](https://openjdk.org/)

**安装注意事项**：

1. 选择与操作系统匹配的版本（Windows/Linux/macOS，32位/64位）
2. 安装路径不要包含中文或特殊字符
3. 建议使用默认安装路径（C:\Program Files\Java\）
4. 记下安装路径，后续环境配置需要

**参考资料：**

- [JDK下载安装与环境配置](https://blog.csdn.net/m0_70545163/article/details/141332829)

> **重要提示**：64位JDK不能安装在32位系统上，安装前请确认系统类型。

#### 2. 核心概念解析

| 术语 | 全称 | 说明 |
|------|------|------|
| JDK | Java Development Kit | Java开发工具包，包含开发所需全部工具 |
| JRE | Java Runtime Environment | Java运行时环境，仅运行Java程序需要 |
| JVM | Java Virtual Machine | Java虚拟机，执行字节码的虚拟计算机 |
| javac.exe | Java Compiler | Java编译器，将.java文件编译为.class文件 |
| java.exe | Java Launcher | Java程序启动器，用于执行.class文件 |

**相关概念（记住）**：

- jdk - Java开发工具包，只要做Java开发就需要下载和安装该软件。
- jre - Java运行时环境信息，只要运行Java程序就需要下载和安装该软件
- jym - Java虚拟机，是Java程序与计算机操作系统之间的桥梁。
- javac.exe - Java语言的编译器，主要用于将Java源代码进行编译生成字节码文件。
- java. exe - Java语言的解释器，主要用于启动Java虚拟机对字节码文件进行解释执行

#### 3. Java程序的编写流程

- 新建文本文档，将文件名由xxx.txt修改为xxx.java;
- 使用记事本的方式打开文件，编写Java代码后进行保存;
- 启动dos窗口，切换到xxx.java文件所在的路径中;
- 使用javac  xxx.java进行编译，生成xxx.class的字节码文件;
- 使用java  xxx进行解释执行，打印最终结果;

**1. 编写Java代码(文件名：HellowWorld.java)**

```java
/**
  * 程序名称：HelloWorld
  * 功能描述：第一个Java程序，演示基本输出
  * 作者：张三
  * 版本：1.0
  */
   public class HelloWorld {
       public static void main(String[] args) {
           System.out.println("我就不打印Hello World!");
       }
   }
```

**2. 编译与执行**

- 把文件放在JDK的bin目录下面

- 打开命令行终端（cmd）

- 切换到源文件所在目录：

  shell

  ```
  cd /JDK/bin
  ```

- **编译Java源文件：**

  shell

  ```cmd
  javac HelloWorld.java
  ```

​	（成功编译会生成`HelloWorld.class`字节码文件）

- **运行程序：**

  shell

  ```cmd
  java HelloWorld
  ```

- **执行结果示例：**

  text

  ```
  我就不打印Hello World!
  ```

**注意事项：**

1. 类名必须与文件名严格一致（区分大小写）
2. 编译命令使用`javac`，运行命令使用`java`
3. 运行时不带`.class`扩展名
4. 建议使用专业IDE（如Eclipse/IntelliJ IDEA）替代记事本开发

**3. 环境变量配置**

**3.1 基本概念**

- **环境变量作用**：使系统能够在任何目录下识别Java命令
- **配置必要性**：未配置时只能在JDK安装目录的bin文件夹下执行javac/java命令
- **核心变量**：
  - `JAVA_HOME`：指向JDK安装目录（如`C:\Program Files\Java\jdk1.8.0_281`）
  - `Path`：添加`%JAVA_HOME%\bin`路径

**3.2 配置步骤（Windows）**

1. 右键"此电脑" → 属性 → 高级系统设置 → 环境变量
2. 新建系统变量：
   - 变量名：`JAVA_HOME`
   - 变量值：JDK安装路径（如`C:\Program Files\Java\jdk1.8.0_281`）
3. 编辑`Path`变量，新增：`%JAVA_HOME%\bin`
4. 验证配置：
   ```cmd
   java -version
   javac -version
   ```

**4. Java开发工具**

**4.1 代码编辑器**

| 工具         | 特点                     |
| :----------- | :----------------------- |
| Notepad++    | 轻量级，支持语法高亮     |
| VS Code      | 现代编辑器，强大插件系统 |
| Sublime Text | 快速响应，多语言支持     |

**4.2 集成开发环境（IDE）**

| IDE           | 特点                     | 适用场景      |
| :------------ | :----------------------- | :------------ |
| IntelliJ IDEA | 智能提示强大，企业级开发 | 专业Java开发  |
| Eclipse       | 开源免费，插件丰富       | 教学/传统项目 |
| NetBeans      | 官方支持，简单易用       | 初学者学习    |

**推荐选择**：

- 初学者：Eclipse/VSCode
- 企业开发：IntelliJ IDEA（社区版免费



# 二.  Java语言的基本语法格式

## 1.1 变量的基本概念

### 1.1.1 变量和注释（重点）

**变量基本概念：**

- 当需要在Java程序中记录单个数据内容时，则声明一个变量即可，而声明变量的本质就是在内存空间中申请一块存储单元，由于存储单元的数值可以改变，因此得名为"变量"。

- 由于存放数据的内容的大小不同导致所需存储单元的容量不同，在Java语言中使用数据类型加以描述，为了便于下次访问还需要指定变量的名称。

**声明语法：**

```java
// 数据类型 变量名 = 初始值;
int age = 18;          // 整数变量
String name = "张三";   // 字符串
```

**代码演示：**

```java
/*
 *	编程实现变量的声明和使用
*/
public class VarTest {
	public static void main(String[] args) {
	
	// 1.声明一个初始值为10的元素为int类型的变量
	int ia = 10;
	// 2.打印变量的数值
	System.out.println("ia = " + ia);
	}
}
```

## 1.2 标识符(变量名)的命名规则

- 要求字母、数字、下划线以及美元$组成，其中数字不能开头。

​	如：name、age、name2、age2

- 要求不能使用Java中的关键字，所谓关键字就是Java中用于表示特殊含义的单词。

​	如：public、class、void、static等

- 区分大小写，长度没有限制但不宜过长。

​	如：name 和 Name代表不同的标识符，不推荐使用。

- 见名知意（推荐小驼峰命名法）

## 1.3 变量的输入输出

**代码演示：**

```java
import java.util.Scanner;  // 添加Scanner类的导入

public class VarIO {
    public static void main(String[] args) {
          // 1. 声明两个变量分别用于记录姓名和年龄
          String name;
          int age;
          // 2. 提示用户输入并读取数据
          System.out.println("请输入您的姓名和年龄: ");

          // 创建Scanner对象
          Scanner sc = new Scanner(System.in);

          // 读取输入
          name = sc.next();      // 读取字符串
          age = sc.nextInt();    // 读取整数

          // 3. 打印变量的数值
          System.out.println("姓名: " + name);
          System.out.println("年龄: " + age);
    }
}
```

**优化代码演示**

```Java
import java.util.Scanner;

public class VarIO {
    public static void main(String[] args) {
        // 输入提示
        System.out.println("请输入您的姓名和年龄: ");
        
        // 创建Scanner并直接初始化变量
        Scanner sc = new Scanner(System.in);
        String name = sc.next();
        int age = sc.nextInt();
        
        // 合并输出
        System.out.println("姓名: " + name + "，年龄: " + age);
    }
}
```

## 1.4 数据类型

### 1.4.1 基本分类

Java语言中的数据类型分为两大类别：

**基本数据类型（8种）**

| 类型      | 大小 | 取值范围        | 默认值   | 示例                   |
| --------- | ---- | --------------- | -------- | ---------------------- |
| `byte`    | 8位  | -128 ~ 127      | 0        | `byte b = 100;`        |
| `short`   | 16位 | -32768 ~ 32767  | 0        | `short s = 500;`       |
| `int`     | 32位 | -2³¹ ~ 2³¹-1    | 0        | `int i = 1000;`        |
| `long`    | 64位 | -2⁶³ ~ 2⁶³-1    | 0L       | `long l = 10000L;`     |
| `float`   | 32位 | 约±3.4e38       | 0.0f     | `float f = 3.14f;`     |
| `double`  | 64位 | 约±1.7e308      | 0.0d     | `double d = 3.1415;`   |
| `boolean` | 1位  | true/false      | false    | `boolean flag = true;` |
| `char`    | 16位 | \u0000 ~ \uffff | '\u0000' | `char c = 'A';`        |

**引用数据类型**

| 类型      | 说明                   | 示例                      |
| --------- | ---------------------- | ------------------------- |
| 类(Class) | 用户自定义或Java内置类 | `String str = "Hello";`   |
| 接口      | 抽象行为规范           | `List<String> list;`      |
| 数组      | 相同类型元素的集合     | `int[] arr = {1,2,3};`    |
| 枚举      | 固定值集合             | `enum Color {RED, GREEN}` |
| 注解      | 元数据标记             | `@Override`               |

> **内存差异**：
>
> - 基本类型：直接存储值（栈内存）
> - 引用类型：存储对象引用（堆内存）

## 1.5 进制之间的转换

### 1.5.1 正数的转换

**基本进制：**

- **十进制**：0-9，日常使用
  `123 = 1×10² + 2×10¹ + 3×10⁰`
- **二进制**：0-1，计算机底层
  `1011 = 1×2³ + 0×2² + 1×2¹ + 1×2⁰ = 11`
- **十六进制**：0-9,A-F，简化二进制
  `A3 = 10×16¹ + 3×16⁰ = 163`

**快速转换表：**

| 十进制 | 二进制 | 十六进制 |
| :----- | :----- | :------- |
| 0      | 0000   | 0        |
| 5      | 0101   | 5        |
| 10     | 1010   | A        |
| 15     | 1111   | F        |

**转换方法：**

1. **二进制→十进制**：按权展开相加
   `1101 = 8+4+0+1 = 13`

2. **十进制→二进制**：除2取余倒序

   text

   ```
   13 ÷ 2 = 6...1
   6 ÷ 2 = 3...0  
   3 ÷ 2 = 1...1
   1 ÷ 2 = 0...1 → 1101
   ```

3. **二进制↔十六进制**：4位分组转换
   `1101 0110 → D6`

### 1.5.2 负数的转换

**负数表示法：**

1. **原码**：最高位为符号位
   `+5 = 0 0101`
   `-5 = 1 0101`
2. **反码**：负数符号位不变，其余取反
   `-5 = 1 1010`
3. **补码**（计算机实际使用）：
   - 正数：与原码相同
   - 负数：反码+1
     `-5 = 1 1011`

**4位二进制示例：**

| 十进制 | 原码 | 反码 | 补码 |
| :----- | :--- | :--- | :--- |
| +5     | 0101 | 0101 | 0101 |
| -5     | 1101 | 1010 | 1011 |
| -1     | 1001 | 1110 | 1111 |

**补码特性：**

1. 解决了`+0`和`-0`问题
2. 减法可转换为加法运算
   `5 - 3 = 5 + (-3的补码)`

**转换练习：**

- 求-7的8位补码：
  1. 原码：`1000 0111`
  2. 反码：`1111 1000`
  3. 补码：`1111 1001`

> 现代计算机统一使用补码存储整数



# 三.  运算符与表达式

## 1.1 算术运算符的概念和使用

**代码示例**

```java
public class ArithmeticOperations {
    public static void main(String[] args) {
        // 声明并初始化两个int类型变量
        int ia = 10;
        int ib = 2;
        
        // 算术运算演示
        int ic = ia + ib;  // 加法运算
        System.out.println("ic = " + ic);     // 输出: ic = 12
        System.out.println(ia + ib);          // 输出: 12 (加法)
        System.out.println(ia - ib);          // 输出: 8 (减法)
        System.out.println(ia * ib);          // 输出: 20 (乘法)
        System.out.println(ia / ib);          // 输出: 5 (除法)
        System.out.println(ia % ib);          // 输出: 0 (取模)
    }
}
```

**核心注意事项**

1. **变量声明**
   - 每行声明一个变量（`int a=1,b=2;`不推荐）
2. **整数运算**
   - 除法截断小数：`5/2=2`
   - 取模符号随被除数：`-5%3=-2`
   - 除数为零抛异常
3. **类型处理**
   - 自动类型提升：`int+double→double`
   - 注意整数溢出风险
4. **代码规范**
   - 运算符前后加空格
   - 复杂表达式加括号或拆分
   - 避免在表达式中嵌入副作用操作

> 提示：精确计算用`double`，大数运算用`BigDecimal`

## 1.2 字符串连接符的使用规则

**基本区分原则**

`+` 运算符在 Java 中有双重作用：

1. **算术加法**：当两端都是数值类型时
2. **字符串连接**：当至少一端是字符串时

**使用示例**

```java
System.out.println(3 + 4);       // 输出 7（算术加法）
System.out.println(3 + "4");     // 输出 "34"（字符串连接）
System.out.println("3" + 4);     // 输出 "34"（字符串连接）
System.out.println("3" + "4");   // 输出 "34"（字符串连接）
```

**混合运算优先级**

```java
System.out.println("结果是：" + 3 + 4);   // 输出 "结果是：34"
System.out.println(3 + 4 + "是结果");   // 输出 "7是结果"
System.out.println("和是：" + (3 + 4)); // 输出 "和是：7"
```

**最佳实践建议**

1. 使用括号明确运算优先级
2. 字符串连接推荐使用 StringBuilder 处理大量连接
3. 注意类型自动转换规则

> **关键点**：从左到右计算，遇到字符串后后续`+`都视为连接符

## 1.3 逻辑运算符的短路特性

**短路特性详解**

Java中的逻辑运算符`&&`(与)和`||`(或)具有短路特性：

1. **`&&` 运算符**：
   - 当第一个操作数为`false`时，不再计算第二个操作数
   - 因为无论第二个操作数是什么，结果都为`false`
2. **`||` 运算符**：
   - 当第一个操作数为`true`时，不再计算第二个操作数
   - 因为无论第二个操作数是什么，结果都为`true`

**代码示例分析**

```Java
int ia = 3;
int ib = 2;

// 示例1：&& 运算符
boolean b3 = (++ia == 3) && (++ib == 2);
/*
 * 执行过程：
 * 1. 先计算 ++ia → ia=4
 * 2. 4 == 3 为 false
 * 3. 由于&&的短路特性，不再执行 ++ib == 2
 * 结果：b3=false, ia=4, ib=2
 */

// 示例2：|| 运算符
boolean b4 = (++ia == 5) || (++ib == 3);
/*
 * 执行过程：
 * 1. 先计算 ++ia → ia=5
 * 2. 5 == 5 为 true
 * 3. 由于||的短路特性，不再执行 ++ib == 3
 * 结果：b4=true, ia=5, ib=2
 */
```

## 1.4 三目运算符的概念和使用

### 1.4.1 条件/三目运算符

**基本语法**

text

```
条件表达式 ? 表达式1 : 表达式2
```

- 先判断条件表达式是否成立
- 若成立，则执行表达式1
- 若不成立，则执行表达式2

**代码示例**

```java
// 判断数字正负
int number = 10;
String result = number < 0 ? "负数" : "非负数";
System.out.println(result);  // 输出"非负数"

// 求两个数的最大值
int a = 5, b = 8;
int max = a > b ? a : b;  // max = 8

// 嵌套三目运算符
int score = 85;
String grade = score >= 90 ? "A" : 
               score >= 80 ? "B" : 
               score >= 70 ? "C" : "D";
System.out.println(grade);  // 输出"B"
```

**关系运算符判断示例**

```java
import java.util.Scanner;

public class RelationJudgeTest {
    public static void main(String[] args) {
        // 1. 提示用户输入整数
        System.out.println("请输入一个整数: ");
        Scanner sc = new Scanner(System.in);
        int number = sc.nextInt();

        // 2. 使用关系运算符和三目运算符判断
        System.out.println(number < 0);  // 直接输出boolean结果
        System.out.println(number < 0 ? "负数" : "非负数");  // 三目运算符
        
        // 3. 判断是否为三位数
        boolean isThreeDigit = number >= 100 && number <= 999;
        System.out.println("是否为三位数: " + isThreeDigit);
    }
}
```

**三目运算符特点**

1. **简洁性**：替代简单的if-else结构
2. **返回值**：必须要有返回值
3. **类型一致**：表达式1和表达式2的类型应该一致
4. **可读性**：适合简单条件判断，复杂逻辑建议用if-else

**最佳实践**

1. 避免过度嵌套三目运算符

2. 保持表达式简单易懂

3. 适当添加括号提高可读性

   java

   ```
   int x = (a > b) ? (c + d) : (c - d);
   ```

> **注意**：三目运算符在编译后会转换为if-else结构，但代码更加简洁。

### 1.4.2 位运算符

- & 表示按位与运算符，就是按照二进制位进行与运算，同1为1，1,0为0(1-真 0-假)。
- |  表示按位或运算符，就是按照二进制位进行或运算，1,1为1，同0为0。
- ~  表示按位取反运算符，按照二进制位进行取反，1为0，0为1。
- ^  表示按位异或运算符，按照二进制位进行异或运算，相同为0，不同为1。

**代码示例**

```Java
public class TestBit {
    public static void main(String[] args) {
        byte b1 = 11;  // 二进制: 0000 1011
        byte b2 = 13;  // 二进制: 0000 1101
        
        System.out.println("b1 = " + b1); // 输出: b1 = 11
        System.out.println("b2 = " + b2); // 输出: b2 = 13
        
        // 位运算演示
        System.out.println("\n--- 位运算结果 ---");
        System.out.println("b1 & b2 = " + (b1 & b2));  // 0000 1001 => 9
        System.out.println("b1 | b2 = " + (b1 | b2));  // 0000 1111 => 15
        System.out.println("b1 ^ b2 = " + (b1 ^ b2));  // 0000 0110 => 6
        System.out.println("~b1 = " + (~b1));         // 1111 0100 => -12
        
        // 移位运算演示
        System.out.println("\n--- 移位运算结果 ---");
        System.out.println("b1 << 1 = " + (b1 << 1));  // 0001 0110 => 22
        System.out.println("b1 >> 1 = " + (b1 >> 1));  // 0000 0101 => 5
        System.out.println("b1 >>> 1 = " + (b1 >>> 1)); // 0000 0101 => 5
    }
}
```



# 四.  Java语言的流程控制

## 1.1 分支结构(重中之重)

### 基本概念

在某些特殊场合中需要进行判断并作出选择时，就需要使用分支结构。

#### **If分支结构**

**（1）语法格式**

```java
if (条件表达式) {
    语句块;
}
```

**（2）执行流程**

- 判断条件表达式是否成立
  => 若成立，则执行语句块；
  => 若不成立，则跳过语句块；

#### if-else分支结构

**（1）语法结构**

``````Java
if(条件表达式) {
	语句块1;
}else {
	语句块2;
}
``````

**（2）执行流程**

- 判断条件表达式是否成立

​	=>若成立，则执行语句块1;

​	=>否则执行语句块2;

**代码示例**

```Java
import java.util.Scanner;
public class IfElseTest {

    public static void main(String[] args) {
        // 1. 提示用户输入考试成绩并使用变量记录
        System.out.println("请输入您的考试成绩: ");
        Scanner sc = new Scanner(System.in);
        int score = sc.nextInt();
        
        // 2. 使用if-else分支结构判断是否及格并给出对应的提示
        if(score >= 60) {
            System.out.println("恭喜您考试通过了！");
        } else {
            System.out.println("下学期来补考吧！");
        }
        
        // 3. 打印一句经典语录
        System.out.println("世界上最遥远的距离不是生与死而是你在if我在else，看似相交却又永远分离！");
    }
}
```

## 1.2 循环结构

### 基本概念

​	在某些特殊场合中需要重复执行一段代码时，借助循环结构加以处理。

### for循环

**（1）语法格式**

``````
for(初始化表达式; 条件表达式; 修改初始值表达式) {
	循环体;
}
``````

**（2）执行流程**

- 执行初始化表达式 => 判断条件表达式是否成立

​		=> 若成立，则执行循环体 => 修改初始值表达式 => 判断条件表达式是否成立

​		=> 若不成立，则循环结束

**代码示例**

```Java
public class ForTest {

    public static void main(String[] args) throws Exception {
        // 使用for循环模拟ATM分次取款过程
        for(int money = 500; money >= 100; money -= 100) {
            System.out.println("当前账户余额：" + money + ", 正在出钞，请稍后...");
            Thread.sleep(5000); // 模拟5秒出钞过程
            System.out.println("请取走您的钞票！\n\n\n");
        }
        
        System.out.println("现在可以尽情地挥霍了...");
    }
}
```

### break和continue关键字的使用

#### 基本概念

- break关键字用于循环中表示跳出当前循环;
- continue关键字用于循环中表示结束本次循环继续下一次循环(会用);

**代码示例**

```Java
public class BreakContinueTest {

    public static void main(String[] args) {
        // 使用for循环演示continue关键字
        for(int i = 1; i <= 20; i++) {
            if(0 == i % 5) {
                continue; // 跳过能被5整除的数字
            }
            System.out.println("i = " + i); // 输出：1 2 3 4 6 7...19
        }
    }
}
```

## 1.3 双重for循环

**（1）语法格式**

``````
for(初始化表达式1; 条件表达式2; 修改初始值表达式3) {
	for(初始值表达式4; 条件表达式5; 修改初始值表达式6) {
		循环体;
	}
}
``````

**（2）执行流程**

- 执行表达式1 => 判断表达式2是否成立

​	=> 若成立，则执行表达式4 => 判断条件表达式5是否成立

​		=> 若成立，则执行循环体 => 执行表达式6 => 判断表达式5是否成立

​		=> 若不成立，则内层循环结束 => 执行表达式3 => 判断表达式2是否成立

​	=> 若不成立，则外层循环结束

**代码示例**

```Java
public class DoubleForDemo {
    public static void main(String[] args) {
        // 打印5行5列的星号矩阵
        for(int i = 1; i <= 5; i++) {         // 外层循环控制行数
            for(int j = 1; j <= 5; j++) {     // 内层循环控制列数
                System.out.print("* ");
            }
            System.out.println();             // 每行结束换行
        }
        
        // 打印九九乘法表
        System.out.println("\n九九乘法表：");
        for(int m = 1; m <= 9; m++) {
            for(int n = 1; n <= m; n++) {
                System.out.print(n + "×" + m + "=" + (m*n) + "\t");
            }
            System.out.println();
        }
    }
}
```

## 1.4 while循环

**（1）语法格式**

``````Java
while(条件表达式) {
	循环体;
}
``````

**（2）执行流程**

- 判断条件表达式是否成立

​	=> 若成立，则执行循环体 => 判断条件表达式是否成立

​	=> 若不成立，则循环结束

**代码示例**

``````java
/*
	编程实现while循环的使用
*/
public class WhileTest {

	public static void main(String[] args) {
        // 使用while循环打印1~10之间的所有整数
		int i = 1;
		while(i <= 10) {
			System.out.println("i = " + i);
            i++;
		}
	}
}
``````

**（3）注意事项**

- while循环和for循环可以完全互换;
- while(true)和for(; ;)表示无限循环;
- while循环主要用于明确循环条件但不明确循环次数的场合中;

​	for循环主要用于明确循环次数或范围的场合中;

## 1.5 switch-case分支结构

**（1）语法格式**

``````java
switch(变量/表达式) {
	case 字面值1: 语句块1; break;
	case 字面值2: 语句块2; break;
	...
	default:语句块;
}
``````

**（2）执行流程**

- 计算变量/表达式的数值 => 判断是否匹配字面值1

​		=> 若匹配，则执行语句块1 => 执行break跳出当前结构

​		=> 若不匹配，则判断是否匹配字面值2

​			=> 若匹配，则执行语句块2 => 执行break跳出当前结构

​			=> 若不匹配，则执行语句块n

**代码示例**

```
public class TestSwitchMenu {

    public static void main(String[] args) {
        // 显示系统菜单
        System.out.println("欢迎使用用户管理系统");
        System.out.println("1.显示所有用户");
        System.out.println("2.增加新用户");
        System.out.println("3.修改用户信息");
        System.out.println("4.删除用户信息");
        System.out.println("5.退出系统");

        // 1.获取用户输入
        System.out.println("请输入1 ~ 5之间的整数: ");
        Scanner sc = new Scanner(System.in);
        int choose = sc.nextInt();

        // 2.使用switch-case处理用户选择
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
                System.out.println("输入错误，请重新输入1~5之间的数字");
        }
    }
}
```



# 五. Java语言的数组声明与应用

## 1.1 数组的基本概念

### 1.1.1 一维数组

#### 基本概念

- 当需要在程序中记录单个数据内容时，则声明一个变量即可;
- 当需要在程序中记录多个类型相同的数据内容时，则声明一维数组即可，一维数组的本质激素在内存中申请一段连续的存储单元。

#### 声明方式

**（1）语法格式**

``````
数据类型[] 数组名称 = new 数据类型[数组的长度];
int[] arr = new int[5]; -表示声明一个长度为5，元素类型为int类型的一维数组
``````

**代码示例**

``````java
/*
	编程实现数组的声明和打印
*/
public class ArrarTest {
	
	public static void main(String[] args) {
		
		//1.声明一个长度为3，元素类型为int类型的一维数组
		int[] arr = new int[3];
		
		//2.打印数组的长度以及每个元素的数值
		System.out.println("数组的长度是：" + arr.length);	//3
        System.out.println("下标为0的元素是：" + arr[0]);  //0
        System.out.println("下标为1的元素是：" + arr[1]);  //0
        System.out.println("下标为2的元素是：" + arr[2]);  //0
        //编译ok 运行ArrarIndexOutOfBoundsException这个是数组下标越界异常
        //System.out.println("下标为3的元素是：" + arr[3]);
        
        System.out.println("-------------------------------------");
        //第二种方法
        for(int 1=0; i < arr.length; i++) {
            System.out.println("下标为" + i + "的元素是" + arr[i]);
        }
	}
}
``````

### 1.1.2 数组的增删改查之初始化操作

``````java
/*
	编程实现数组的增删改查操作
*/
public class ArrayOperationTest {

	public static void main(String[] args) {
		
		//1.声明一个长度为5，元素类型为int类型的一维数组
        int[] arr = new int[5];
        //打印所有元素值
        System.out.print("数组中的元素初始值为：");
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + ""); // 0 0 0
        }
        System.out.println();
        
        System.out.println("-------------------------------------");
        //2.使用10、20、30、40分别给数组中前四个位置元素赋值
        for(int i = 0; i < arr.length-1; i++) {
            arr[i] = (i+1)*10;
        }
        //打印所有元素
        System.out.print("数组赋值后的元素为：");
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + ""); //10 20 30 40 0
        }
        System.out.println();
        
        System.out.println("-------------------------------------");
        //3.将数据50插入
        for(int i = 0; i > 0; i--) {
            arr[i] = arr[i-1];
        }
        arr[0] = 50;
        //再次打印
        System.out.print("数组插入后的元素为：");
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + ""); //50 10 20 30 40
        }
        System.out.println();
        
        System.out.println("-------------------------------------");
        //4.将数据50从数组中删除，后续元素向前移动
        for(int i = 0; i < arr.length-1; i++) {
            arr[i] = arr[i+1];
        }
        arr[4] = 0;
        //再次打印
        System.out.print("数组删除后的元素为：");
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + ""); //10 20 30 40 0
        }
        System.out.println();
        
        System.out.println("-------------------------------------");
        //5.查找数组中是否包含元素20，若包含将元素20改为200
        for(int i = 0; i < arr.length; i++) {
            if(arr[i] == 20) {
                arr[i] = 200;
            }
        }
        //再次打印
        System.out.print("数组改查后的元素为：");
        for(int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + ""); //10 20 30 40 0
        }
        System.out.println();
	}
}
``````

### 1.1.3 二维数组的基本概念

#### 基本概念

- 一维数组本质上就是一段连续的存储单元，用于存放多个类型相同的数据内容;
- 二维数组本质上就是由多个一维数组组成(摞在一起)的数组，也就是说二维数组中的每个元素都是一个一维数组，而一维数组中的每个元素才是数据内容;

#### 声明方式

**（1）语法格式**

``````
数据类型[][] 数组名称 = new 数据类型[行数][列数];
int[][] brr = new int[2][3]; -声明一个具有2行3列元素类型为int类型的二维数组
其中行下标的范围是：0~1;
其中列下标的范围是：0~2;
``````

