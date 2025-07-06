# 计算机的体系结构

## 基本概念
计算机（computer）俗称"电脑"，是一种被广泛应用于各个领域的电子设备。计算机系统主要由两大部分组成：**计算机硬件**和**计算机软件**，二者协同工作实现信息处理与运算功能。

## 计算机硬件（Computer Hardware）
计算机硬件是构成计算机的物理实体，常见硬件组件包括：CPU、内存、硬盘、显卡、主板、键盘、显示器、鼠标等。以下是核心硬件的详细解析：

### CPU - 中央处理器
- **核心功能**：计算机的运算和控制核心，相当于人的大脑，负责处理计算机指令与软件数据
- **关键特性**：
  - 由运算器、控制器和高速缓存组成
  - 处理速度以GHz为单位（如3.6GHz）
  - 主流品牌：Intel、AMD、Apple M系列（ARM架构）

### 内存 - 随机存取存储器（RAM）
- **核心功能**：临时存储CPU正在处理的数据，支持高速读写
- **关键特性**：
  - CPU可直接访问，读写速度达纳秒级
  - 容量常见规格：8GB、16GB、32GB
  - 断电后数据丢失（易失性存储）
  - 常见类型：DDR4、DDR5

### 硬盘 - 外部存储设备
- **核心功能**：长期存储数据与程序，容量大且断电不丢失数据
- **关键特性**：
  - CPU需通过I/O接口访问，速度低于内存
  - 主流类型：
    - **机械硬盘（HDD）**：容量大（1TB+），价格低，速度较慢
    - **固态硬盘（SSD）**：速度快（读写超500MB/s），抗震性好，成本较高
  - 容量常见规格：256GB、512GB、1TB、2TB

### 输入/输出设备
- **标准输入设备**：键盘、鼠标、扫描仪等
- **标准输出设备**：显示器、打印机、扬声器等
- **典型接口**：USB、HDMI、VGA、音频接口

## 计算机软件（Computer Software）
计算机软件是运行在硬件上的程序、数据及相关文档的集合，分为**系统软件**和**应用软件**两大类。

### 系统软件
- **核心功能**：管理计算机硬件与软件资源，为应用程序提供运行环境
- **主流类型**：
  - **操作系统（OS）**：
    - Windows（7/10/11）：桌面端主流系统，兼容性强
    - macOS：苹果电脑专属系统，用户体验流畅
    - Linux：开源系统，常用于服务器与开发场景
    - Android/iOS：移动设备操作系统
  - **设备驱动程序**：连接硬件与操作系统的桥梁
  - **编译系统**：将源代码转换为可执行程序的工具

### 应用软件
- **核心功能**：满足用户具体需求的程序，运行在操作系统之上
- **常见分类**：
  - **办公软件**：Microsoft Office、WPS
  - **通信软件**：QQ、微信、钉钉
  - **多媒体软件**：Adobe系列（PS/AE）、视频播放器
  - **开发工具**：IDEA、VS Code、Postman
  - **娱乐软件**：游戏、音乐/视频平台

## 计算机体系结构层级模型
```
┌───────────────┐
│   使用者       │
└───────────────┘
        │
┌───────────────┐
│   应用软件     │ （如：微信、Office）
└───────────────┘
        │
┌───────────────┐
│   系统软件     │
├───────────────┤
│  ┌─────────┐  │
│  │  外壳   │  │ （如：Windows图形界面）
│  └─────────┘  │
│             │
│  ┌─────────┐  │
│  │  内核   │  │ （如：Windows内核NT）
│  └─────────┘  │
└───────────────┘
        │
┌───────────────┐
│   硬件设备     │ （CPU/内存/硬盘等）
└───────────────┘
```

## 存储容量单位与换算
### 标准二进制换算（操作系统视角）
```
1 TB（太字节） = 1024 GB（吉字节）
1 GB = 1024 MB（兆字节）
1 MB = 1024 KB（千字节）
1 KB = 1024 Byte（字节）
1 Byte（字节） = 8 bit（二进制位）
```

### 硬件厂商换算（十进制）
```
1 TB = 1000 GB
1 GB = 1000 MB
1 MB = 1000 KB
1 KB = 1000 Byte
```

### 容量差异解析
- **现象**：购买的1TB硬盘在系统中显示约931GB
- **原因**：
  - 硬件厂商按1000进制标注（1TB=10^12 Byte）
  - 操作系统按1024进制计算（1TB=2^40 Byte≈1.0995×10^12 Byte）
  - 实际可用容量 = 标注容量 × (1000/1024)^3
  - **示例**：1TB硬盘实际容量 = 1000^4 / 1024^4 ≈ 0.931 TB = 931 GB

### 字符编码与存储占用
- 1个英文字母/数字/符号：1 Byte（8 bit）
- 1个汉字（UTF-8编码）：3 Byte
- 1个汉字（GBK编码）：2 Byte
- 1张高清照片（JPG）：5-10 MB
- 1部高清电影（1080P）：1-2 GB

# Java语言的概述

## Java语言的背景
Java语言诞生于1995年，由"Java语言之父"詹姆斯·高斯林（James Gosling）开发。该语言最初隶属于Sun公司，2009年Sun被Oracle收购后，Java现由Oracle公司主导。作为编程语言界的常青树，Java长期在TIOBE、IEEE等编程语言排行榜中占据前列，广泛应用于企业级开发、安卓应用、大数据处理等领域。

## Java发展历史
- **1991年**：Sun公司启动"绿色计划"，James Gosling领导团队探索嵌入式系统编程语言。
- **1992年**：因C++在嵌入式场景的不足，开发新语言Oak，目标是消费电子设备的分布式系统。
- **1994年**：随互联网兴起，团队将Oak语言应用于万维网开发。
- **1995年**：因"Oak"商标已被注册，Sun将其更名为Java，提出"Write once, Run anywhere"（一次编写，处处运行）的口号。
- **1996年**：发布JDK 1.0，包含Java运行环境和开发工具，标志Java正式诞生。
- **1997年**：JDK 1.1发布，新增JDBC（数据库连接）、反射等核心功能，奠定Java语言基础。
- **1998年**：JDK 1.2发布，引入集合框架（如List、Map），将Java技术体系分为J2SE（标准版）、J2EE（企业版）、J2ME（微型版）。
- **2000年**：J2SE 1.3发布，HotSpot虚拟机成为默认JVM，提升性能。
- **2002年**：J2SE 1.4发布，提供NIO（新IO）、正则表达式等特性，Java走向成熟。
- **2004年**：Java 5（1.5）发布，语法重大升级，引入泛型、注解、自动装箱/拆箱等特性，命名方式不再使用"J2"前缀。
- **2009年**：Oracle收购Sun公司，获得Java技术主导权，后续发布JavaEE 6、Java 7等版本。
- **2014年**：Java 8发布，引入Lambda表达式、Stream API，是继Java 5后的第三个里程碑版本。
- **2018年**：Java 10发布，带来局部变量类型推断等新特性；同年Java 11发布，成为自Java 8后的首个长期支持（LTS）版本。
- **2023年**：Java 21发布，引入结构化并发、虚拟线程等前沿特性，持续保持语言活力。

## Java的主要版本
### Java SE（Java Platform, Standard Edition）
- **中文名**：Java平台标准版
- **定位**：Java语言的核心基础，包含语法规范、核心类库（如java.lang、java.util）和开发工具
- **应用场景**：Java基础学习、桌面应用开发（Swing/AWT）、小型工具开发
- **关键特性**：提供基础IO、网络编程、多线程、反射等核心功能

### Java EE（Java Platform, Enterprise Edition）
- **中文名**：Java平台企业版
- **定位**：面向企业级应用的开发框架，基于Java SE扩展企业级组件
- **核心技术**：Servlet、JSP、EJB、Spring框架、MyBatis、JPA（ORM）等
- **应用场景**：B/S架构Web应用（如电商平台、管理系统）、分布式服务、微服务架构
- **现状**：2018年更名为Jakarta EE，由Eclipse基金会管理，持续演进中

### Java ME（Java Platform, Micro Edition）
- **中文名**：Java平台微型版
- **定位**：面向嵌入式设备和移动终端的轻量级Java平台
- **历史应用**：早期手机应用（如诺基亚Symbian系统）、机顶盒、智能家电
- **现状**：随着Android/iOS平台的普及，Java ME已逐渐淘汰，其功能被Android开发替代

## 开发环境的搭建和使用
### JDK的下载和安装
#### 下载方式
- **官方渠道**：
  - Oracle JDK：[https://www.oracle.com/java/technologies/downloads/](https://www.oracle.com/java/technologies/downloads/)
  - 开源OpenJDK：[https://adoptium.net/](https://adoptium.net/)（推荐，免费且兼容Oracle JDK）
- **版本选择**：
  - 学习/企业开发：优先选择LTS版本（如Java 11、Java 17）
  - 尝新特性：可选择最新版本（如Java 21）

#### 安装方式
1. **绿色版（解压即用）**：
   - 下载zip/tar.gz包，解压到自定义目录（如`D:\java\jdk11`）
   - 无需安装程序，直接通过配置环境变量使用

2. **安装版（Windows/macOS）**：
   - 运行安装程序，按向导点击"下一步"
   - **注意**：安装路径避免包含中文或特殊字符（如`C:\Program Files\Java\jdk11`）

### 核心概念解析
#### JDK（Java Development Kit）
- **全称**：Java开发工具包
- **定位**：Java开发的核心工具集，是JRE的超集
- **包含内容**：
  - JRE（运行环境）
  - 编译器（javac.exe）、解释器（java.exe）
  - 调试工具（jdb.exe）、性能分析工具（jvisualvm.exe）
  - 开发类库（如rt.jar、tools.jar）
- **适用人群**：Java开发者必须安装

#### JRE（Java SE Runtime Environment）
- **全称**：Java SE运行时环境
- **定位**：运行Java程序的必要环境
- **包含内容**：
  - JVM（Java虚拟机）
  - 核心类库（rt.jar等）
  - 支持库（如font、locale资源）
- **适用人群**：仅需运行Java程序的用户（如普通电脑使用者）

#### JVM（Java Virtual Machine）
- **核心作用**：Java跨平台的关键，负责执行字节码（.class文件）
- **工作机制**：
  1. 加载.class文件到内存
  2. 验证字节码合法性
  3. 解释执行或编译为本地机器码
  4. 管理内存分配与垃圾回收（GC）
- **主流实现**：
  - HotSpot（Oracle JDK默认，性能优化强）
  - OpenJ9（IBM开发，内存占用低）
  - Zing（Azul Systems，低延迟企业级JVM）

#### javac.exe
- **功能**：Java编译器，将.java源文件编译为.class字节码文件
- **常用命令**：
  ```bash
  javac -d outDir srcFile.java  # 指定输出目录
  javac -cp lib1;lib2 srcFile.java  # 设置依赖库路径
  javac -encoding UTF-8 srcFile.java  # 指定编码格式
  ```

#### java.exe
- **功能**：Java运行命令，启动JVM执行字节码
- **常用命令**：
  ```bash
  java -jar app.jar  # 运行打包的jar程序
  java -Xmx2g -Xms1g MyApp  # 设置堆内存大小
  java -cp classes;lib/* MyApp  # 设置类路径
  ```

### Java程序的编写流程
1. **创建源文件**：
   - 新建文本文件，重命名为`HelloWorld.java`（注意扩展名改为.java）
   - **注意**：若文件扩展名不显示，需在系统设置中取消"隐藏已知文件类型的扩展名"

2. **编写代码**：
   ```java
   public class HelloWorld {
       public static void main(String[] args) {
           System.out.println("Hello, Java!");
       }
   }
   ```

3. **编译文件**：
   - 打开命令行（Windows+R输入cmd），切换到源文件所在目录
   - 执行编译命令：`javac HelloWorld.java`
   - 成功后生成`HelloWorld.class`字节码文件

4. **运行程序**：
   - 执行运行命令：`java HelloWorld`
   - 输出结果：`Hello, Java!`

### 常用快捷键
#### 通用操作：
- `Ctrl+S`：保存文件  
- `Ctrl+C`：复制选中内容  
- `Ctrl+V`：粘贴内容  
- `Ctrl+Z`：撤销操作  
- `Ctrl+A`：全选内容  

#### 系统操作：
- `Windows+D`：快速回到桌面  
- `Windows+E`：打开文件资源管理器  
- `Windows+L`：锁定计算机  
- `Windows+R`：打开"运行"对话框（输入cmd可启动命令行）  
- `Ctrl+Alt+Delete`：打开任务管理器  

#### 命令行操作：
- `方向键↑/↓`：切换历史命令  
- `Ctrl+Shift`：切换输入法（中文输入法下按Shift可切换中英文）  
- `Ctrl+C`：终止当前运行的程序  

## 环境变量的配置
### 基本概念
环境变量用于告知操作系统可执行文件的路径。配置后，可在任意目录执行`javac`/`java`命令，无需切换到JDK安装目录。

### 配置步骤（Windows 10）
1. **打开系统属性**：
   - 右键"此电脑" → "属性" → "高级系统设置"

2. **打开环境变量对话框**：
   - 点击"高级"选项卡 → "环境变量"按钮

3. **配置Path变量**：
   - 在"系统变量"中找到`Path` → 点击"编辑"
   - 点击"新建" → 输入JDK的`bin`目录路径（如`C:\Program Files\Java\jdk-11.0.21\bin`）
   - **注意**：不要删除原有Path内容，新增条目即可

4. **验证配置**：
   - 重启命令行（或按Win+R输入`cmd`）
   - 输入`javac -version`和`java -version`，若显示JDK版本信息则配置成功

### 配置原理
- 当在命令行输入`javac`时，系统会按Path变量中的路径顺序查找`javac.exe`
- 配置JDK的`bin`目录到Path后，系统可在任意目录找到该命令

## 跨平台原理
### "一次编写，到处运行"的实现机制
1. **编译阶段**：
   - Java源代码（.java）通过`javac`编译为平台中立的字节码（.class）
   - 字节码是一种二进制格式，不依赖具体操作系统

2. **运行阶段**：
   - 不同平台（Windows/macOS/Linux）安装对应版本的JVM
   - JVM负责将字节码转换为本地机器码执行
   - JVM屏蔽了底层硬件和操作系统差异，实现跨平台

### 核心技术点
- **字节码规范**：所有JVM必须支持统一的字节码格式，确保.class文件可在任意JVM运行
- **JNI（Java Native Interface）**：Java标准库通过JNI调用本地系统API，实现与平台交互
- **JVM自适应优化**：如HotSpot的JIT（即时编译）技术，动态优化热点代码执行效率

### 跨平台案例
- 同一个`HelloWorld.class`文件：
  - 在Windows系统中通过Windows版JVM运行
  - 在Linux服务器中通过Linux版JVM运行
  - 在Mac电脑中通过macOS版JVM运行
- 无需修改代码，只需在目标平台安装对应JVM即可运行

# Java语言的基本语法格式

## 变量和注释

### 基本概念
变量是Java程序中存储数据的基本单元，本质是在内存中申请的存储单元，其值可改变。声明变量需指定数据类型（决定存储容量）和变量名（便于访问）。

### 声明方式
```java
数据类型 变量名 = 初始值;
```

**代码示例**：
```java
/*
 * 编程实现变量的声明和使用
 */
public class VarTest {
    public static void main(String[] args) {
        // 1. 声明一个初始值为10，类型为int的变量
        int ia = 10;
        // 2. 打印变量值（+为字符串连接符）
        System.out.println("ia=" + ia); // 输出：ia=10
        
        System.out.println("---------------------");
        // 变量使用前必须声明
        // System.out.println("sa=" + sa); // 错误：变量未声明
        String sa;
        // System.out.println("sa=" + sa); // 错误：变量未初始化
        sa = "hello";
        System.out.println("sa=" + sa); // 输出：sa=hello
        
        // 变量不能重复声明
        // int ia = 20; // 错误：变量ia已定义
    }
}
```

### 标识符（变量名）的命名规则
1. **组成规则**：由字母、数字、下划线（`_`）和美元符号（`$`）组成，数字不能开头。  
   ✅ 合法示例：`name`、`age2`、`_score`、`$var`  
   ❌ 非法示例：`2num`、`my-name`

2. **关键字限制**：不能使用Java关键字（如`public`、`class`、`void`、`static`等）。

3. **大小写敏感**：长度无限制但不宜过长，`name`和`Name`是不同标识符。

4. **语义规范**：见名知意，支持中文但不推荐。  
   推荐：`year`、`month`、`studentCount`  
   不推荐：`a`、`x1`、`中文变量`

**代码示例**：
```java
/*
 * 编程实现姓名和年龄的输入输出
 */
import java.util.Scanner; // 导入Scanner类

public class VarIO {
    public static void main(String[] args) {
        // 1. 声明变量记录姓名和年龄
        String name;
        int age;
        
        // 2. 提示用户输入并存储
        System.out.println("请输入您的姓名和年龄：");
        Scanner sc = new Scanner(System.in); // 创建扫描器对象
        name = sc.next();                     // 读取字符串
        age = sc.nextInt();                   // 读取整数
        
        // 3. 打印结果
        System.out.println("name=" + name + ", age=" + age);
    }
}
```

### 注释
1. **单行注释**：`//` 从符号开始到行尾的内容为注释。  
   ```java
   int num = 10; // 声明一个整数变量
   ```

2. **多行注释**：`/* 注释内容 */` 符号间的内容为注释，不允许嵌套。  
   ```java
   /*
    * 这是一个多行注释
    * 可跨越多行
    */
   ```

## 数据类型

### 基本分类
Java数据类型分为两大类：
1. **基本数据类型**（8种）：  
   `byte`、`short`、`int`、`long`、`float`、`double`、`boolean`、`char`

2. **引用数据类型**：  
   数组、类、接口、注解、枚举

### 常用的进制
1. **十进制**：日常生活使用，权重为10^n（如123 = 1×10² + 2×10¹ + 3×10⁰）。

2. **二进制**：计算机底层使用，权重为2^n，最高位为符号位（0表示非负数，1表示负数）。  
   例：二进制`1010`表示十进制`10`。

### 进制之间的转换
#### 正十进制转二进制
1. **除2取余法**：用十进制数不断除以2，取余数后逆序排列。  
   例：45转二进制：  
   ```
   45 ÷ 2 = 22 余1  
   22 ÷ 2 = 11 余0  
   11 ÷ 2 = 5  余1  
   5 ÷ 2 = 2  余1  
   2 ÷ 2 = 1  余0  
   1 ÷ 2 = 0  余1  
   逆序余数：101101（即45的二进制为`101101`）
   ```

2. **拆分法**：将十进制数拆分为二进制权重和，有权重位写1，否则写0。  
   例：45 = 32+8+4+1 → 对应二进制位`101101`（补全8位为`00101101`）。

#### 正二进制转十进制
**加权法**：每个二进制位乘以对应权重后累加。  
例：`00101101`转十进制：  
```
0×2⁷ + 0×2⁶ + 1×2⁵ + 0×2⁴ + 1×2³ + 1×2² + 0×2¹ + 1×2⁰  
= 0 + 0 + 32 + 0 + 8 + 4 + 0 + 1 = 45
```

#### 负十进制转二进制
1. 先将绝对值转二进制，再按位取反加1（补码表示）。  
   例：-45转二进制：  
   - 绝对值45的二进制：`00101101`  
   - 按位取反：`11010010`  
   - 加1：`11010011`（即-45的二进制补码）

#### 负二进制转十进制
1. 先减1，再按位取反，最后加负号。  
   例：`11010011`转十进制：  
   - 减1：`11010010`  
   - 按位取反：`00101101`  
   - 转十进制：45 → 结果：-45

### 基本数据类型详解
| 类型      | 字节数 | 取值范围                           | 示例                   |
| --------- | ------ | ---------------------------------- | ---------------------- |
| `byte`    | 1      | -128 ~ 127                         | `byte b = 10;`         |
| `short`   | 2      | -32768 ~ 32767                     | `short s = 100;`       |
| `int`     | 4      | -2^31 ~ 2^31-1（约-21亿 ~ 21亿）   | `int num = 1000;`      |
| `long`    | 8      | -2^63 ~ 2^63-1（需加`L`后缀）      | `long l = 100000L;`    |
| `float`   | 4      | 单精度浮点数（需加`f`后缀）        | `float f = 3.14f;`     |
| `double`  | 8      | 双精度浮点数（默认后缀）           | `double d = 3.14;`     |
| `boolean` | 1      | `true` 或 `false`                  | `boolean flag = true;` |
| `char`    | 2      | Unicode字符（'\u0000' ~ '\uffff'） | `char c = 'A';`        |

**注意事项**：
- `long`类型变量需加`L`后缀（如`100L`）。
- `float`类型变量需加`f`后缀（如`3.14f`），否则默认为`double`。
- `char`使用单引号（`''`），字符串使用双引号（`""`）。

# 运算符与表达式

## 运算符

### 算术运算符
| 运算符 | 说明         | 示例         |
| ------ | ------------ | ------------ |
| `+`    | 加法         | `3 + 5 = 8`  |
| `-`    | 减法         | `5 - 3 = 2`  |
| `*`    | 乘法         | `3 * 5 = 15` |
| `/`    | 除法         | `5 / 3 = 1`  |
| `%`    | 取模（取余） | `5 % 3 = 2`  |

#### 注意事项
1. **整数除法特性**：两个整数相除结果为整数，小数部分直接舍弃。  
   例：`5 / 2 = 2`

2. **保留小数的方法**：
   - 将操作数强制转换为`double`：`(double)5 / 2 = 2.5`
   - 乘以`1.0`：`5 * 1.0 / 2 = 2.5`（推荐）

3. **除数限制**：
   - `0`不能作为除数（`5 / 0`会抛出`ArithmeticException`）
   - `0.0`可以作为除数，结果为无穷大（`5.0 / 0.0 = Infinity`）

4. **字符串连接符**：当`+`两侧有字符串时，作为连接符使用。  
   例：`"Hello" + 10 = "Hello10"`

#### 代码示例
```java
public class ArithmeticTest {
    public static void main(String[] args) {
        int ia = 10, ib = 2;
        
        // 基本算术运算
        System.out.println("ia + ib = " + (ia + ib)); // 12
        System.out.println("ia - ib = " + (ia - ib)); // 8
        System.out.println("ia * ib = " + (ia * ib)); // 20
        System.out.println("ia / ib = " + (ia / ib)); // 5
        System.out.println("ia % ib = " + (ia % ib)); // 0
        
        // 整数除法注意事项
        ia = 5;
        System.out.println(ia / ib);           // 2（整数除法）
        System.out.println(1.0 * ia / ib);     // 2.5（推荐方式）
        
        // 字符串连接示例
        System.out.println("结果：" + ia + ib); // 结果：52（字符串连接）
        System.out.println(ia + ib + "结果"); // 7结果（先算术后连接）
    }
}
```

#### 应用案例：时间转换
```java
import java.util.Scanner;

public class TimeArithmetic {
    public static void main(String[] args) {
        System.out.println("请输入一个整数类型的秒数：");
        Scanner sc = new Scanner(System.in);
        int seconds = sc.nextInt();
        
        int hours = seconds / 3600;         // 小时
        int minutes = (seconds % 3600) / 60; // 分钟
        int secs = seconds % 60;            // 剩余秒数
        
        System.out.println(seconds + "秒拆分为：" + hours + "时" + minutes + "分" + secs + "秒");
        
        // 字符串连接优先级演示
        System.out.println("" + hours + minutes + secs);   // 116（全连接）
        System.out.println(hours + "" + minutes + secs);   // 116
        System.out.println(hours + minutes + "" + secs);   // 26（先加后连接）
        System.out.println(hours + minutes + secs + "");   // 8（先加后连接）
    }
}
```

### 关系/比较运算符
| 运算符 | 说明     | 示例             |
| ------ | -------- | ---------------- |
| `==`   | 等于     | `3 == 5 → false` |
| `!=`   | 不等于   | `3 != 5 → true`  |
| `>`    | 大于     | `5 > 3 → true`   |
| `<`    | 小于     | `3 < 5 → true`   |
| `>=`   | 大于等于 | `5 >= 5 → true`  |
| `<=`   | 小于等于 | `3 <= 5 → true`  |

#### 特点
- 运算结果为`boolean`类型（`true`或`false`）
- 常用于条件判断语句（如`if`、`while`）

#### 代码示例
```java
public class RelationTest {
    public static void main(String[] args) {
        int a = 3, b = 5;
        
        System.out.println("a > b: " + (a > b));   // false
        System.out.println("a < b: " + (a < b));   // true
        System.out.println("a == b: " + (a == b)); // false
        System.out.println("a != b: " + (a != b)); // true
        System.out.println("a >= b: " + (a >= b)); // false
        System.out.println("a <= b: " + (a <= b)); // true
    }
}
```

#### 应用案例：数值判断
```java
import java.util.Scanner;

public class RelationJudgeTest {
    public static void main(String[] args) {
        System.out.println("请输入一个整数：");
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        
        // 判断是否为负数
        System.out.println(num + "是负数：" + (num < 0));
        
        // 判断是否为三位数（100-999）
        boolean isThreeDigit = (num >= 100) && (num <= 999);
        System.out.println(num + "是三位数：" + isThreeDigit);
    }
}
```

### 自增/自减运算符
| 运算符 | 说明              | 示例         |
| ------ | ----------------- | ------------ |
| `++`   | 自增（变量值加1） | `a++`或`++a` |
| `--`   | 自减（变量值减1） | `a--`或`--a` |

#### 前缀与后缀区别
- **前缀式（++a / --a）**：先自增/自减，再参与运算  
  例：`int b = ++a` → `a`先加1，再赋值给`b`
- **后缀式（a++ / a--）**：先参与运算，再自增/自减  
  例：`int b = a++` → 先赋值给`b`，`a`再加1

#### 代码示例
```java
public class IncrementTest {
    public static void main(String[] args) {
        int a = 10;
        
        // 自增演示
        System.out.println("a = " + a);       // 10
        System.out.println("a++ = " + (a++)); // 10（先返回值，再自增）
        System.out.println("a = " + a);       // 11
        System.out.println("++a = " + (++a)); // 12（先自增，再返回值）
        System.out.println("a = " + a);       // 12
        
        // 自减演示
        int b = 20;
        System.out.println("b = " + b);       // 20
        System.out.println("b-- = " + (b--)); // 20（先返回值，再自减）
        System.out.println("b = " + b);       // 19
        System.out.println("--b = " + (--b)); // 18（先自减，再返回值）
        System.out.println("b = " + b);       // 18
    }
}
```

### 逻辑运算符
| 运算符 | 说明           | 示例                    |
| ------ | -------------- | ----------------------- |
| `&&`   | 逻辑与（短路） | `true && false → false` |
| `||`   | 逻辑或（短路） | `true || false → true`  |
| `!`    | 逻辑非         | `!true → false`         |

#### 短路特性
- **逻辑与（&&）**：若第一个操作数为`false`，则直接返回`false`，不计算第二个操作数
- **逻辑或（||）**：若第一个操作数为`true`，则直接返回`true`，不计算第二个操作数

#### 代码示例
```java
public class LogicTest {
    public static void main(String[] args) {
        boolean a = true, b = false;
        
        System.out.println("a && b = " + (a && b)); // false
        System.out.println("a || b = " + (a || b)); // true
        System.out.println("!a = " + (!a));         // false
        System.out.println("!b = " + (!b));         // true
        
        // 短路特性测试
        int x = 5, y = 10;
        boolean result = (x++ > 10) && (y++ < 20);
        System.out.println("result = " + result); // false
        System.out.println("x = " + x);           // 6（x++执行了）
        System.out.println("y = " + y);           // 10（y++未执行）
        
        result = (x++ < 10) || (y++ < 20);
        System.out.println("result = " + result); // true
        System.out.println("x = " + x);           // 7（x++执行了）
        System.out.println("y = " + y);           // 10（y++未执行）
    }
}
```

#### 应用案例：条件判断
```java
import java.util.Scanner;

public class LogicJudgeTest {
    public static void main(String[] args) {
        System.out.println("请输入一个正整数：");
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        
        // 判断是否为偶数且大于100
        boolean isEvenAndLarge = (num % 2 == 0) && (num > 100);
        System.out.println(num + "是偶数且大于100：" + isEvenAndLarge);
        
        // 判断是否为3或5的倍数
        boolean isMultiple = (num % 3 == 0) || (num % 5 == 0);
        System.out.println(num + "是3或5的倍数：" + isMultiple);
    }
}
```

### 条件/三目运算符
#### 语法
```
条件表达式 ? 表达式1 : 表达式2
```

#### 执行流程
- 若条件表达式为`true`，则返回表达式1的值
- 若条件表达式为`false`，则返回表达式2的值

#### 代码示例
```java
import java.util.Scanner;

public class TernaryTest {
    public static void main(String[] args) {
        // 判断正负
        System.out.println("请输入一个整数：");
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        
        String result = (num < 0) ? "负数" : "非负数";
        System.out.println(num + "是" + result);
        
        // 求两个数的最大值
        System.out.println("请输入两个正整数：");
        int a = sc.nextInt();
        int b = sc.nextInt();
        
        int max = (a >= b) ? a : b;
        System.out.println("最大值是：" + max);
        
        // 多条件判断（嵌套三目）
        String grade = (num >= 90) ? "优秀" : 
                       (num >= 80) ? "良好" : 
                       (num >= 60) ? "及格" : "不及格";
        System.out.println("成绩等级：" + grade);
    }
}
```

### 赋值运算符
#### 简单赋值
- **运算符**：`=`
- **作用**：将右侧值赋给左侧变量，覆盖原有值
- **示例**：`int a = 5;`

#### 复合赋值
| 运算符 | 等价表达式  | 示例     |
| ------ | ----------- | -------- |
| `+=`   | `a = a + b` | `a += b` |
| `-=`   | `a = a - b` | `a -= b` |
| `*=`   | `a = a * b` | `a *= b` |
| `/=`   | `a = a / b` | `a /= b` |
| `%=`   | `a = a % b` | `a %= b` |

#### 代码示例
```java
public class AssignmentTest {
    public static void main(String[] args) {
        int a = 10;
        System.out.println("a = " + a); // 10
        
        // 简单赋值
        a = 20;
        System.out.println("a = " + a); // 20
        
        // 复合赋值
        a += 5;  // a = a + 5
        System.out.println("a += 5 → " + a); // 25
        
        a -= 10; // a = a - 10
        System.out.println("a -= 10 → " + a); // 15
        
        a *= 2;  // a = a * 2
        System.out.println("a *= 2 → " + a); // 30
        
        a /= 5;  // a = a / 5
        System.out.println("a /= 5 → " + a); // 6
        
        a %= 4;  // a = a % 4
        System.out.println("a %= 4 → " + a); // 2
    }
}
```

### 运算符优先级
| 优先级 | 运算符类别             | 运算符                            |
| ------ | ---------------------- | --------------------------------- |
| 1      | 括号                   | `()`                              |
| 2      | 单目运算符             | `++`, `--`, `!`, `~`              |
| 3      | 算术运算符（乘除取模） | `*`, `/`, `%`                     |
| 4      | 算术运算符（加减）     | `+`, `-`                          |
| 5      | 移位运算符             | `<<`, `>>`, `>>>`                 |
| 6      | 关系运算符             | `>`, `<`, `>=`, `<=`, `==`, `!=`  |
| 7      | 逻辑运算符（与）       | `&&`                              |
| 8      | 逻辑运算符（或）       | `||`                              |
| 9      | 条件运算符             | `? :`                             |
| 10     | 赋值运算符             | `=`, `+=`, `-=`, `*=`, `/=`, `%=` |

#### 注意事项
- 不确定优先级时，用`()`明确运算顺序
- 赋值运算符优先级很低，通常最后执行

#### 示例
```java
public class PriorityTest {
    public static void main(String[] args) {
        int a = 5, b = 3, c = 2;
        
        // 优先级演示
        int result1 = a + b * c;         // 5 + 3*2 = 11
        int result2 = (a + b) * c;       // (5+3)*2 = 16
        int result3 = a++ + --b;         // 5 + 2 = 7（a变为6，b变为2）
        int result4 = a > b && a < c || !false; // true && false || true = true
        
        System.out.println("result1 = " + result1); // 11
        System.out.println("result2 = " + result2); // 16
        System.out.println("result3 = " + result3); // 7
        System.out.println("result4 = " + result4); // true
    }
}
```

### 移位运算符
| 运算符 | 说明                | 示例                            |
| ------ | ------------------- | ------------------------------- |
| `<<`   | 左移（低位补0）     | `10 << 2 = 40`（1010 → 101000） |
| `>>`   | 右移（符号位填充）  | `10 >> 2 = 2`（1010 → 10）      |
| `>>>`  | 无符号右移（0填充） | `-10 >>> 2 = 1073741822`        |

#### 代码示例
```java
public class ShiftTest {
    public static void main(String[] args) {
        int num = 10; // 二进制：0000 0000 0000 0000 0000 0000 0000 1010
        
        System.out.println("num = " + num); // 10
        
        // 左移：乘以2^n
        System.out.println("num << 1 = " + (num << 1)); // 20（10*2^1）
        System.out.println("num << 2 = " + (
```

# Java语言的流程控制

## 分支结构

### 基本概念
在编程中，当需要根据不同条件做出判断和选择时，需要使用分支结构。Java提供了`if`、`if-else`、`if-else if-else`和`switch-case`四种分支结构。

### if分支结构
#### 语法格式
```java
if(条件表达式) {
    语句块;
}
```

#### 执行流程
1. 判断条件表达式是否成立
2. 若成立，执行语句块；若不成立，跳过语句块

#### 代码示例
```java
import java.util.Scanner;
public class IfTest {
    public static void main(String[] args) {
        System.out.println("请输入年龄：");
        Scanner sc = new Scanner(System.in);
        int age = sc.nextInt();
        
        if (age >= 18) {
            System.out.println("恭喜你已成年！");
        }
        
        System.out.println("欢迎来到成年人的世界");
    }
}
```

#### 应用案例：找最大值
```java
import java.util.Scanner;
public class IfMaxTest {
    public static void main(String[] args) {
        System.out.println("请输入两个整数：");
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        
        int max = a;
        if (b > max) {
            max = b;
        }
        System.out.println("最大值是：" + max);
    }
}
```

### if-else分支结构
#### 语法格式
```java
if(条件表达式) {
    语句块1;
} else {
    语句块2;
}
```

#### 执行流程
1. 判断条件表达式是否成立
2. 若成立，执行语句块1；若不成立，执行语句块2

#### 代码示例
```java
import java.util.Scanner;
public class IfElseTest {
    public static void main(String[] args) {
        System.out.println("请输入考试成绩：");
        Scanner sc = new Scanner(System.in);
        int score = sc.nextInt();
        
        if (score >= 60) {
            System.out.println("恭喜通过考试！");
        } else {
            System.out.println("请重新考试！");
        }
        
        System.out.println("“学习使人快乐”");
    }
}
```

### if-else if-else分支结构
#### 语法格式
```java
if(条件表达式1) {
    语句块1;
} else if(条件表达式2) {
    语句块2;
} 
...
else {
    语句块n;
}
```

#### 执行流程
1. 判断条件表达式1是否成立，若成立执行语句块1
2. 若不成立，判断条件表达式2是否成立，若成立执行语句块2
3. 依此类推，若所有条件都不成立，执行最后else中的语句块n

#### 代码示例
```java
import java.util.Scanner;
public class IfElseifElseTest {
    public static void main(String[] args) {
        System.out.println("请输入您的身份信息：");
        Scanner sc = new Scanner(System.in);
        String identity = sc.next();
        System.out.println("欢迎您，" + identity + "！");
        
        if (identity.equals("军人")) {
            System.out.println("请免费乘车");
        } else if (identity.equals("学生")) {
            System.out.println("请购买半价票");
        } else {
            System.out.println("全票价等着您");
        }
        
        System.out.println("祝您旅途愉快！");
    }
}
```

### switch-case分支结构
#### 语法格式
```java
switch(变量/表达式) {
    case 字面值1: 语句块1; break;
    case 字面值2: 语句块2; break;
    ...
    default: 语句块n;
}
```

#### 执行流程
1. 计算变量/表达式的值
2. 依次匹配case后的字面值
3. 匹配成功则执行对应语句块，遇到break跳出switch
4. 若所有case都不匹配，执行default语句块

#### 注意事项
- switch支持的数据类型：byte、short、char、int、枚举（JDK1.5+）、String（JDK1.7+）
- break用于跳出当前switch结构，若无break会发生"穿透"现象

#### 代码示例
```java
import java.util.Scanner;
public class TestSwitchMenu {
    public static void main(String[] args) {
        System.out.println("欢迎使用用户管理系统!");
        System.out.println("1.显示所有用户");
        System.out.println("2.增加新用户");
        System.out.println("3.修改用户信息");
        System.out.println("4.删除用户信息");
        System.out.println("5.退出系统");
        
        System.out.println("请输入1~5之间的整数：");
        Scanner scanner = new Scanner(System.in);
        int choice = scanner.nextInt();
        
        switch (choice) {
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
                System.out.println("输入错误，请重新输入！");
        }
    }
}
```

#### 应用案例：成绩等级判断
```java
import java.util.Scanner;
public class TestSwitchcase {
    public static void main(String[] args) {
        System.out.println("请输入您的考试成绩:");
        Scanner sc = new Scanner(System.in);
        int score = sc.nextInt();
        
        switch (score / 10) {
            case 10:
                System.out.println("满分");
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
        System.out.println("“学习使人快乐”");
    }
}
```

## 循环结构

### 基本概念
循环结构用于重复执行一段代码，Java提供了`for`、`while`和`do-while`三种循环结构（JDK中`do-while`使用较少，此处重点介绍前两种）。循环控制关键字包括`break`（跳出循环）和`continue`（跳过本次循环）。

### for循环
#### 语法格式
```java
for(初始化表达式; 条件表达式; 修改初始值表达式) {
    循环体;
}
```

#### 执行流程
1. 执行初始化表达式
2. 判断条件表达式是否成立
3. 若成立，执行循环体，然后执行修改初始值表达式，返回步骤2
4. 若不成立，循环结束

#### 代码示例
```java
public class ForTest {
    public static void main(String[] args) {
        // 打印10到1的整数
        for (int i = 10; i >= 1; i--) {
            System.out.println("i=" + i);
        }
        
        System.out.println("-------------------------");
        
        // 打印1到10的整数
        for (int i = 1; i <= 10; i++) {
            System.out.println("i=" + i);
        }
        
        System.out.println("-------------------------");
        
        // 打印1到100的奇数（三种方式）
        // 方式一：取余判断
        for (int i = 1; i <= 100; i++) {
            if (i % 2 != 0) {
                System.out.println("i=" + i);
            }
        }
        
        // 方式二：等差数列
        for (int i = 1; i <= 100; i += 2) {
            System.out.println("i=" + i);
        }
        
        // 方式三：通项公式
        for (int i = 1; i <= 50; i++) {
            System.out.println("i=" + (2 * i - 1));
        }
    }
}
```

#### 应用案例：累加和计算
```java
public class ForSumTest {
    public static void main(String[] args) {
        int sum = 0;
        for (int i = 1; i <= 100; i++) {
            sum += i;
        }
        System.out.println("1到100的累加和是:" + sum); // 5050
    }
}
```

### break和continue关键字
#### 作用
- `break`：跳出当前循环
- `continue`：结束本次循环，继续下一次循环

#### 代码示例
```java
public class BreakContinueTest {
    public static void main(String[] args) {
        for (int i = 1; i <= 20; i++) {
            if (i % 5 == 0) {
                continue; // 跳过5的倍数
            }
            if (i == 18) {
                break; // 当i=18时跳出循环
            }
            System.out.println("i=" + i);
        }
    }
}
```

### 无限循环
#### 语法格式
```java
for (;;) { // 等价于 while(true)
    // 循环体
    if (条件) break; // 配合break使用
}
```

#### 应用案例：聊天模拟
```java
import java.util.Scanner;
public class ForChatTest {
    public static void main(String[] args) {
        boolean flag = true;
        Scanner sc = new Scanner(System.in);
        
        for (;;) {
            System.out.println("请" + (flag ? "洪飞" : "建辉") + "输入要发送的内容:");
            String msg = sc.next();
            
            if (msg.equals("bye")) {
                System.out.println("聊天结束!");
                break;
            } else {
                System.out.println((flag ? "洪飞说：" : "建辉说：") + msg);
            }
            flag = !flag;
        }
        sc.close();
    }
}
```

### 双重循环
#### 语法格式
```java
for(外层初始化; 外层条件; 外层修改) {
    for(内层初始化; 内层条件; 内层修改) {
        循环体;
    }
}
```

#### 执行流程
1. 执行外层初始化表达式
2. 判断外层条件，若成立则执行内层循环
3. 内层循环执行完毕后，执行外层修改表达式，返回步骤2
4. 外层条件不成立时，双重循环结束

#### 注意事项
- 外层循环执行一次，内层循环执行一圈
- 常用于打印多行多列数据或矩阵运算

#### 代码示例
```java
public class ForForTest {
    public static void main(String[] args) {
        // 打印5行"厉害了我的哥"
        for (int i = 1; i <= 5; i++) {
            System.out.println("厉害了我的哥!");
        }
        
        System.out.println("--------------------");
        
        // 打印5列"厉害了我的哥"
        for (int j = 1; j <= 5; j++) {
            System.out.print("厉害了我的哥!");
        }
        System.out.println(); // 换行
        
        System.out.println("--------------------");
        
        // 打印5行5列"厉害了我的哥"
        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= 5; j++) {
                System.out.print("厉害了我的哥 ");
            }
            System.out.println(); // 每行结束换行
        }
    }
}
```

#### 应用案例：九九乘法表
```java
public class MultiplicationTable {
    public static void main(String[] args) {
        for (int i = 1; i <= 9; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(j + "×" + i + "=" + (i * j) + "\t");
            }
            System.out.println();
        }
    }
}
```

### while循环
#### 语法格式
```java
while(条件表达式) {
    循环体;
}
```

#### 执行流程
1. 判断条件表达式是否成立
2. 若成立，执行循环体，然后返回步骤1
3. 若不成立，循环结束

#### 注意事项
- while循环和for循环可互换，for更适合已知次数的循环
- `while(true)`等价于`for(;;)`，表示无限循环

#### 代码示例
```java
public class WhileTest {
    public static void main(String[] args) {
        // 使用while循环打印1到10的整数
        int i = 1;
        while (i <= 10) {
            System.out.println("i=" + i);
            i++;
        }
    }
}
```

#### 应用案例：分数累加和
```java
import java.util.Scanner;
public class WhileSumTest {
    public static void main(String[] args) {
        System.out.println("请输入一个正整数:");
        Scanner sc = new Scanner(System.in);
        int number = sc.nextInt();
        
        double sum = 0.0;
        int i = 1;
        while (i <= number) {
            sum += 1.0 / i;
            i++;
        }
        
        System.out.println("1 + 1/2 + 1/3 + ... + 1/" + number + " 的累加和为:" + sum);
        sc.close();
    }
}
```

### 循环结构对比
| 循环类型 | 语法特点                             | 适用场景               | 执行顺序               |
| -------- | ------------------------------------ | ---------------------- | ---------------------- |
| for      | 初始化、条件、修改集中在一行         | 已知循环次数或范围     | 先判断条件再执行循环体 |
| while    | 条件在前，循环体在后                 | 已知循环条件但未知次数 | 先判断条件再执行循环体 |
| do-while | 循环体在前，条件在后（至少执行一次） | 至少执行一次循环的场景 | 先执行循环体再判断条件 |

### 循环优化建议
1. 避免在循环中执行复杂运算，尽量提前计算
2. 数组遍历优先使用`for-each`循环（JDK1.5+）
3. 多层循环中，将长度固定的循环放在外层
4. 及时使用`break`/`continue`终止不必要的循环
5. 大循环中考虑使用`StringBuilder`代替`+`拼接字符串

```java
// 推荐的数组遍历方式（for-each）
int[] arr = {1, 2, 3, 4, 5};
for (int num : arr) {
    System.out.println(num);
}
```

# Java语言的数组声明与应用

## 一维数组

### 基本概念
- **变量**：用于存储单个数据
- **一维数组**：用于存储多个相同类型的数据，在内存中占据一段连续的存储单元

### 声明方式
#### 语法格式
```java
数据类型[] 数组名称 = new 数据类型[数组长度];
```
示例：
```java
int[] arr = new int[5]; // 声明长度为5的int数组
```

#### 初始化方式
1. **动态初始化**：指定数组长度，系统自动分配初始值
   ```java
   int[] arr = new int[3]; // 初始值：[0, 0, 0]
   ```

2. **静态初始化**：直接指定数组元素值
   ```java
   int[] arr = {10, 20, 30}; // 初始值：[10, 20, 30]
   ```

3. **复杂方式**：显式调用构造器
   ```java
   int[] arr = new int[]{1, 2, 3}; // 初始值：[1, 2, 3]
   ```

### 代码示例
```java
public class ArrayTest {
    public static void main(String[] args) {
        // 1. 声明并打印默认值
        int[] arr = new int[3];
        System.out.println("数组长度：" + arr.length); // 3
        System.out.println("默认值：");
        for (int i = 0; i < arr.length; i++) {
            System.out.println("arr[" + i + "] = " + arr[i]); // 0, 0, 0
        }

        // 2. 赋值并打印
        arr[0] = 11;
        arr[1] = 22;
        arr[2] = 33;
        System.out.println("赋值后：");
        for (int num : arr) {
            System.out.println(num); // 11, 22, 33
        }

        // 3. 静态初始化
        int[] iArr = {10, 20, 30, 40, 50};
        System.out.println("静态初始化：");
        for (int i = 0; i < iArr.length; i++) {
            System.out.println("iArr[" + i + "] = " + iArr[i]);
        }
    }
}
```

### 注意事项
1. **数组长度不可变**：一旦创建，长度无法修改
2. **下标越界**：访问超出`[0, length-1]`范围的下标会抛出`ArrayIndexOutOfBoundsException`
3. **默认值规则**：
   - 数值类型：`0`或`0.0`
   - 布尔类型：`false`
   - 引用类型：`null`

## 二维数组

### 基本概念
- **二维数组**：由多个一维数组组成的数组，每个元素都是一个一维数组
- **存储结构**：逻辑上是矩阵，物理上是连续存储的一维数组的集合

### 声明方式
#### 语法格式
```java
数据类型[][] 数组名称 = new 数据类型[行数][列数];
```
示例：
```java
int[][] arr = new int[2][3]; // 2行3列的int数组
```

#### 初始化方式
1. **规则二维数组**：每行元素个数相同
   ```java
   int[][] arr = {{1, 2, 3}, {4, 5, 6}}; // 2行3列
   ```

2. **不规则二维数组**：每行元素个数不同
   ```java
   int[][] arr = new int[3][];
   arr[0] = new int[2]; // 第1行2列
   arr[1] = new int[3]; // 第2行3列
   arr[2] = new int[4]; // 第3行4列
   ```

### 代码示例
```java
public class ArrayArrayTest {
    public static void main(String[] args) {
        // 1. 规则二维数组
        int[][] arr = {{1, 2, 3}, {4, 5, 6}};
        
        // 遍历方式1：普通for循环
        System.out.println("规则二维数组：");
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr[i].length; j++) {
                System.out.print(arr[i][j] + " ");
            }
            System.out.println();
        }
        
        // 2. 不规则二维数组
        int[][] crr = new int[3][];
        crr[0] = new int[2];
        crr[1] = new int[3];
        crr[2] = new int[4];
        
        // 赋值
        for (int i = 0; i < crr.length; i++) {
            for (int j = 0; j < crr[i].length; j++) {
                crr[i][j] = (i + 1) * 10 + j;
            }
        }
        
        // 遍历方式2：增强for循环
        System.out.println("不规则二维数组：");
        for (int[] row : crr) {
            for (int num : row) {
                System.out.print(num + " ");
            }
            System.out.println();
        }
    }
}
```

### 多维数组
Java支持三维及以上的多维数组，声明方式类似：
```java
// 三维数组：2个二维数组，每个二维数组有3行4列
int[][][] arr3D = new int[2][3][4];

// 初始化
arr3D[0][0][0] = 1;
// ...

// 遍历
for (int i = 0; i < arr3D.length; i++) {
    for (int j = 0; j < arr3D[i].length; j++) {
        for (int k = 0; k < arr3D[i][j].length; k++) {
            System.out.print(arr3D[i][j][k] + " ");
        }
        System.out.println();
    }
    System.out.println();
}
```

## 数组操作技巧

### 数组拷贝
```java
int[] src = {1, 2, 3};
int[] dest = new int[src.length];

// 方式1：System.arraycopy(源数组, 源起始位置, 目标数组, 目标起始位置, 长度)
System.arraycopy(src, 0, dest, 0, src.length);

// 方式2：Arrays.copyOf(源数组, 新长度)
int[] dest2 = Arrays.copyOf(src, src.length);

// 方式3：clone()方法
int[] dest3 = src.clone();
```

### 数组排序
```java
import java.util.Arrays;

int[] arr = {5, 3, 1, 4, 2};

// 升序排序
Arrays.sort(arr); // [1, 2, 3, 4, 5]

// 降序排序（需转换为包装类型）
Integer[] arrWrapper = Arrays.stream(arr).boxed().toArray(Integer[]::new);
Arrays.sort(arrWrapper, Collections.reverseOrder()); // [5, 4, 3, 2, 1]
```

### 数组查找
```java
import java.util.Arrays;

int[] arr = {10, 20, 30, 40, 50};

// 线性查找
int target = 30;
int index = -1;
for (int i = 0; i < arr.length; i++) {
    if (arr[i] == target) {
        index = i;
        break;
    }
}

// 二分查找（要求数组已排序）
int key = 40;
int pos = Arrays.binarySearch(arr, key); // 返回索引3
```

### 数组遍历方式
1. **普通for循环**：可修改元素
```java
for (int i = 0; i < arr.length; i++) {
    arr[i] *= 2;
}
```

2. **增强for循环**：简洁，只读
```java
for (int num : arr) {
    System.out.println(num);
}
```

3. **Java 8 Stream API**：函数式风格
```java
Arrays.stream(arr)
      .forEach(System.out::println);
```

## 常见错误与注意事项
1. **空指针异常**：未初始化数组直接访问
   ```java
   int[] arr;
   System.out.println(arr[0]); // 错误：NullPointerException
   ```

2. **数组越界**：访问超出合法范围的下标
   ```java
   int[] arr = new int[3];
   System.out.println(arr[3]); // 错误：ArrayIndexOutOfBoundsException
   ```

3. **引用传递问题**：数组是引用类型，赋值传递引用而非值
   ```java
   int[] a = {1, 2, 3};
   int[] b = a; // b和a指向同一数组
   b[0] = 100; // a[0]也变为100
   ```

## 应用案例

### 案例1：计算平均值
```java
public class AverageCalculator {
    public static void main(String[] args) {
        int[] scores = {85, 90, 78, 92, 88};
        int sum = 0;
        
        for (int score : scores) {
            sum += score;
        }
        
        double average = (double) sum / scores.length;
        System.out.printf("平均分：%.2f\n", average); // 86.60
    }
}
```

### 案例2：二维数组转置
```java
public class MatrixTranspose {
    public static void main(String[] args) {
        int[][] matrix = {{1, 2, 3}, {4, 5, 6}};
        int rows = matrix.length;
        int cols = matrix[0].length;
        
        // 创建转置后的数组
        int[][] transposed = new int[cols][rows];
        
        // 转置操作
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                transposed[j][i] = matrix[i][j];
            }
        }
        
        // 输出结果
        for (int[] row : transposed) {
            for (int num : row) {
                System.out.print(num + " ");
            }
            System.out.println();
        }
    }
}
```

### 案例3：杨辉三角
```java
public class PascalTriangle {
    public static void main(String[] args) {
        int n = 5;
        int[][] triangle = new int[n][];
        
        for (int i = 0; i < n; i++) {
            triangle[i] = new int[i + 1];
            for (int j = 0; j <= i; j++) {
                if (j == 0 || j == i) {
                    triangle[i][j] = 1;
                } else {
                    triangle[i][j] = triangle[i - 1][j - 1] + triangle[i - 1][j];
                }
                System.out.print(triangle[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

输出结果：
```
1 
1 1 
1 2 1 
1 3 3 1 
1 4 6 4 1 
```

# 理解面向对象思想和概念

## 面向对象编程的概念

### 什么是对象？
在面向对象编程中，**对象**是现实世界中实体的抽象表示。每个对象都有自己的**状态**（属性）和**行为**（方法）。例如：
- 一个人可以是一个对象，有姓名、年龄等属性，有说话、走路等行为
- 一辆汽车可以是一个对象，有颜色、型号等属性，有启动、加速等行为

### 什么是面向对象？
**面向对象**是一种编程范式，它以**对象**为中心，通过**封装**、**继承**和**多态**等机制来组织代码。面向对象的核心思想是：
- 将数据（属性）和操作数据的方法（行为）绑定在一起
- 通过抽象、分类和组合来构建复杂系统

### 什么是面向对象编程？
**面向对象编程**（OOP）是一种实现方式，它使用类和对象来组织代码。常见的面向对象编程语言包括Java、Python、C++、C#等。

### 面向对象与面向过程的对比
| 特性             | 面向对象编程 (OOP)                   | 面向过程编程 (POP)           |
| ---------------- | ------------------------------------ | ---------------------------- |
| 核心组织单元     | 对象（类的实例）                     | 函数和过程                   |
| 数据与方法的关系 | 数据和方法封装在一起                 | 数据和方法分离               |
| 代码复用方式     | 继承和组合                           | 函数调用和复制               |
| 设计思路         | 自下而上，从具体对象抽象出类         | 自上而下，将问题分解为子过程 |
| 适用场景         | 大型复杂系统、需要高可维护性和扩展性 | 简单任务、算法实现           |

### 面向对象编程的三大特征
要学好面向对象编程，需要深刻理解以下三大特征：
1. **封装**：将数据和操作封装在一起，隐藏内部实现细节，提供公共接口
2. **继承**：通过继承可以创建新类，复用现有类的属性和方法
3. **多态**：允许不同类的对象对同一消息做出不同响应

## 类、对象以及引用

### 对象和类的概念
- **对象**：是具体的实体，在内存中占据空间
- **类**：是对象的抽象模板，定义了对象的属性和方法

### 类的定义
在Java中，类使用`class`关键字定义：
```java
class 类名 {
    // 成员变量（属性）
    数据类型 变量名;
    
    // 成员方法（行为）
    返回值类型 方法名(参数列表) {
        方法体;
    }
}
```

**示例：定义Person类**
```java
class Person {
    // 成员变量（属性）
    String name;  // 姓名
    int age;      // 年龄
    
    // 成员方法（行为）
    void sayHello() {
        System.out.println("大家好，我是" + name + "，今年" + age + "岁了！");
    }
}
```

### 对象的创建
使用`new`关键字创建对象：
```java
类名 对象引用 = new 类名();
```

**示例：创建Person对象**
```java
Person p = new Person();  // 创建Person对象并赋值给引用变量p
p.name = "张三";          // 设置对象的属性
p.age = 20;
p.sayHello();             // 调用对象的方法
```

### 引用变量
- **引用**：是一个变量，存储对象在内存中的地址
- 引用变量可以指向同一类的不同对象
- 通过引用变量可以访问对象的属性和方法

**示例：多个引用指向同一对象**
```java
Person p1 = new Person();
p1.name = "张三";

Person p2 = p1;  // p2和p1指向同一个对象
p2.age = 20;

System.out.println(p1.age);  // 输出：20
```

## 成员方法

### 方法的定义
方法是类中定义的一段代码，用于实现特定的功能。方法包含以下部分：
```java
修饰符 返回值类型 方法名(参数列表) {
    方法体;
    return 返回值;  // 如果返回值类型不是void，必须有return语句
}
```

**示例：定义带参数和返回值的方法**
```java
class Calculator {
    // 加法方法，接收两个整数，返回它们的和
    int add(int a, int b) {
        return a + b;
    }
    
    // 打印信息的方法，无返回值
    void printInfo(String message) {
        System.out.println("计算结果：" + message);
    }
}
```

### 方法的调用
通过对象引用调用方法：
```java
Calculator calc = new Calculator();
int result = calc.add(3, 5);  // 调用add方法
calc.printInfo("3 + 5 = " + result);  // 调用printInfo方法
```

### 参数传递
Java中参数传递分为两种：
1. **基本数据类型**：传递的是值的副本
2. **引用数据类型**：传递的是引用（内存地址）

**示例：参数传递演示**
```java
class Demo {
    // 基本数据类型参数
    void changeValue(int x) {
        x = 100;
    }
    
    // 引用数据类型参数
    void changeName(Person p) {
        p.name = "李四";
    }
}

// 测试代码
public static void main(String[] args) {
    Demo demo = new Demo();
    
    int num = 10;
    demo.changeValue(num);
    System.out.println(num);  // 输出：10（基本类型参数传递的是值的副本）
    
    Person person = new Person();
    person.name = "张三";
    demo.changeName(person);
    System.out.println(person.name);  // 输出：李四（引用类型参数传递的是内存地址）
}
```

### 方法重载（Overload）
方法重载是指在同一个类中定义多个同名但参数列表不同的方法。编译器根据调用时的实参类型和数量来决定调用哪个方法。

**示例：方法重载**
```java
class MathUtils {
    // 计算两个整数的和
    int add(int a, int b) {
        return a + b;
    }
    
    // 计算三个整数的和
    int add(int a, int b, int c) {
        return a + b + c;
    }
    
    // 计算两个小数的和
    double add(double a, double b) {
        return a + b;
    }
}
```

### 构造方法
构造方法是一种特殊的方法，用于创建对象时初始化对象的属性。构造方法具有以下特点：
- 方法名与类名相同
- 没有返回值类型（连void都没有）
- 可以有参数，也可以无参数
- 如果没有显式定义构造方法，Java会提供一个默认的无参构造方法

**示例：构造方法的使用**
```java
class Person {
    String name;
    int age;
    
    // 无参构造方法
    public Person() {
        name = "未知";
        age = 0;
    }
    
    // 带参数的构造方法
    public Person(String name, int age) {
        this.name = name;  // 使用this关键字区分成员变量和参数
        this.age = age;
    }
    
    void introduce() {
        System.out.println("我是" + name + "，今年" + age + "岁。");
    }
}

// 测试代码
public static void main(String[] args) {
    Person p1 = new Person();  // 调用无参构造方法
    p1.introduce();  // 输出：我是未知，今年0岁。
    
    Person p2 = new Person("张三", 20);  // 调用带参构造方法
    p2.introduce();  // 输出：我是张三，今年20岁。
}
```

## 应用案例

### 案例1：银行账户类
```java
class BankAccount {
    // 成员变量
    private String accountNumber;  // 账户号码
    private double balance;        // 账户余额
    
    // 构造方法
    public BankAccount(String accountNumber, double initialBalance) {
        this.accountNumber = accountNumber;
        this.balance = initialBalance;
    }
    
    // 存款方法
    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("存款成功，当前余额：" + balance);
        } else {
            System.out.println("存款金额必须大于0");
        }
    }
    
    // 取款方法
    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("取款成功，当前余额：" + balance);
        } else {
            System.out.println("取款失败，余额不足或金额无效");
        }
    }
    
    // 查询余额方法
    public double getBalance() {
        return balance;
    }
    
    // 获取账户信息
    public void showInfo() {
        System.out.println("账户号码：" + accountNumber);
        System.out.println("当前余额：" + balance);
    }
}

// 测试代码
public static void main(String[] args) {
    BankAccount account = new BankAccount("123456", 1000.0);
    account.showInfo();  // 显示账户信息
    
    account.deposit(500.0);  // 存款500
    account.withdraw(200.0); // 取款200
    
    System.out.println("当前余额：" + account.getBalance());  // 直接获取余额
}
```

### 案例2：矩形类
```java
class Rectangle {
    // 成员变量
    private double length;  // 长
    private double width;   // 宽
    
    // 构造方法
    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }
    
    // 计算面积
    public double getArea() {
        return length * width;
    }
    
    // 计算周长
    public double getPerimeter() {
        return 2 * (length + width);
    }
    
    // 显示矩形信息
    public void showInfo() {
        System.out.println("矩形信息：");
        System.out.println("长：" + length + "，宽：" + width);
        System.out.println("面积：" + getArea());
        System.out.println("周长：" + getPerimeter());
    }
}

// 测试代码
public static void main(String[] args) {
    Rectangle rect = new Rectangle(5.0, 3.0);
    rect.showInfo();
}
```

### 案例3：学生类
```java
class Student {
    // 成员变量
    private String name;     // 姓名
    private int age;         // 年龄
    private String studentId;// 学号
    private double[] scores; // 成绩数组
    
    // 构造方法
    public Student(String name, int age, String studentId, double[] scores) {
        this.name = name;
        this.age = age;
        this.studentId = studentId;
        this.scores = scores;
    }
    
    // 计算平均成绩
    public double calculateAverage() {
        if (scores == null || scores.length == 0) {
            return 0;
        }
        
        double sum = 0;
        for (double score : scores) {
            sum += score;
        }
        
        return sum / scores.length;
    }
    
    // 显示学生信息
    public void showInfo() {
        System.out.println("学生信息：");
        System.out.println("姓名：" + name);
        System.out.println("年龄：" + age);
        System.out.println("学号：" + studentId);
        
        System.out.print("成绩：");
        for (double score : scores) {
            System.out.print(score + " ");
        }
        System.out.println();
        
        System.out.println("平均成绩：" + calculateAverage());
    }
}

// 测试代码
public static void main(String[] args) {
    double[] scores = {85.5, 90.0, 78.5, 92.0};
    Student student = new Student("李四", 21, "2025001", scores);
    student.showInfo();
}
```

# 构造方法及方法重载

## 构造方法

### 基本概念
构造方法是一种特殊的方法，用于在创建对象时初始化对象的属性。它具有以下特点：
- 方法名与类名完全相同
- 没有返回值类型（包括void）
- 在使用`new`关键字创建对象时自动调用

### 语法格式
```java
class 类名 {
    类名(参数列表) {
        // 构造方法体
    }
}
```

### 构造方法的作用
1. 初始化对象的成员变量
2. 为对象分配初始状态
3. 执行对象创建时需要的其他操作

### 默认构造方法
- 当类中没有显式定义任何构造方法时，编译器会自动生成一个无参的默认构造方法
- 默认构造方法的方法体为空
- 若类中定义了至少一个构造方法，编译器不再生成默认构造方法

### 代码示例
```java
public class Person {
    String name;  // 姓名
    int age;      // 年龄

    // 无参构造方法
    public Person() {
        name = "默认姓名";
        age = 0;
        System.out.println("无参构造方法被调用");
    }

    // 带参数的构造方法
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
        System.out.println("带参数的构造方法被调用");
    }

    // 显示信息的方法
    public void showInfo() {
        System.out.println("姓名：" + name + "，年龄：" + age);
    }

    public static void main(String[] args) {
        // 使用无参构造方法创建对象
        Person p1 = new Person();
        p1.showInfo();

        // 使用带参数的构造方法创建对象
        Person p2 = new Person("张三", 25);
        p2.showInfo();
    }
}
```

## 方法重载（Overload）

### 基本概念
方法重载是指在同一个类中定义多个同名方法，但参数列表不同（参数个数、类型或顺序不同）。编译器会根据调用时的实参类型和数量选择合适的方法。

### 重载的条件
1. 方法名必须相同
2. 参数列表必须不同（参数个数、类型或顺序不同）
3. 返回值类型可以不同，但建议保持一致
4. 与形参变量名无关

### 重载的形式
1. **参数个数不同**：`void method() {}` 和 `void method(int a) {}`
2. **参数类型不同**：`void method(int a) {}` 和 `void method(double a) {}`
3. **参数顺序不同**：`void method(int a, double b) {}` 和 `void method(double b, int a) {}`

### 代码示例
```java
public class OverloadDemo {
    // 计算两个整数的和
    public int add(int a, int b) {
        return a + b;
    }

    // 计算三个整数的和（参数个数不同）
    public int add(int a, int b, int c) {
        return a + b + c;
    }

    // 计算两个浮点数的和（参数类型不同）
    public double add(double a, double b) {
        return a + b;
    }

    // 参数顺序不同的重载
    public String add(String a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        OverloadDemo demo = new OverloadDemo();
        
        System.out.println("整数和：" + demo.add(5, 3));         // 8
        System.out.println("三数和：" + demo.add(5, 3, 2));      // 10
        System.out.println("浮点数和：" + demo.add(3.5, 2.1));   // 5.6
        System.out.println("字符串连接：" + demo.add("结果：", 8)); // 结果：8
    }
}
```

### 方法重载的优势
- 提高代码可读性：使用相同的方法名表示相似功能
- 减少记忆负担：调用者只需记住一个方法名
- 增强代码灵活性：适应不同参数类型的需求

## this关键字

### 基本概念
`this`关键字代表当前对象，在不同场景中有不同含义：
- 在构造方法中：代表正在创建的对象
- 在成员方法中：代表调用该方法的对象

### 主要用途
1. **区分成员变量和局部变量**：当方法参数与成员变量同名时，用`this`指定成员变量
2. **调用本类的其他构造方法**：在构造方法中使用`this(参数)`调用其他构造方法
3. **作为方法返回值**：返回当前对象，支持链式调用

### 代码示例
```java
public class ThisDemo {
    private String name;
    private int age;

    // 构造方法中使用this区分参数和成员变量
    public ThisDemo(String name, int age) {
        this.name = name;  // this.name指成员变量，name指参数
        this.age = age;
    }

    // 构造方法中使用this调用其他构造方法
    public ThisDemo() {
        this("默认姓名", 0);  // 调用有参构造方法
        System.out.println("无参构造方法");
    }

    // 成员方法中使用this
    public void showInfo() {
        System.out.println("姓名：" + this.name + "，年龄：" + this.age);
    }

    // 返回this实现链式调用
    public ThisDemo setName(String name) {
        this.name = name;
        return this;  // 返回当前对象
    }

    public static void main(String[] args) {
        // 使用无参构造方法创建对象，会调用有参构造方法
        ThisDemo demo1 = new ThisDemo();
        demo1.showInfo();  // 姓名：默认姓名，年龄：0

        // 使用有参构造方法创建对象
        ThisDemo demo2 = new ThisDemo("张三", 25);
        demo2.showInfo();  // 姓名：张三，年龄：25

        // 链式调用
        demo2.setName("李四").showInfo();  // 姓名：李四，年龄：25
    }
}
```

## 方法的参数传递

### 基本数据类型的传递
- 传递的是值的副本
- 形参的改变不会影响实参

### 引用数据类型的传递
- 传递的是对象的引用（内存地址）
- 形参指向的对象内容改变会影响实参
- 形参改变指向后，不再影响实参

### 代码示例
```java
public class ParameterDemo {
    // 基本数据类型参数传递
    public void changeBasic(int num) {
        num = 100;  // 改变形参值
        System.out.println("方法内基本类型参数：" + num);
    }

    // 引用数据类型参数传递（修改对象内容）
    public void changeArray(int[] arr) {
        arr[0] = 100;  // 修改数组元素
        System.out.println("方法内数组参数：" + arr[0]);
    }

    // 引用数据类型参数传递（改变引用指向）
    public void changeReference(int[] arr) {
        arr = new int[2];  // 形参指向新数组
        arr[0] = 200;
        System.out.println("方法内新数组参数：" + arr[0]);
    }

    public static void main(String[] args) {
        ParameterDemo demo = new ParameterDemo();
        
        // 基本类型参数测试
        int basic = 50;
        demo.changeBasic(basic);
        System.out.println("基本类型实参：" + basic);  // 输出：50（未改变）
        
        // 引用类型参数测试（修改内容）
        int[] array = {10, 20, 30};
        demo.changeArray(array);
        System.out.println("数组实参：" + array[0]);  // 输出：100（已改变）
        
        // 引用类型参数测试（改变指向）
        int[] array2 = {10, 20, 30};
        demo.changeReference(array2);
        System.out.println("数组实参2：" + array2[0]);  // 输出：10（未改变）
    }
}
```

## 递归调用

### 基本概念
递归是指在方法内部调用自身的编程方式。递归需要满足两个条件：
1. 递归终止条件：存在不再继续递归的情况
2. 递归表达式：问题可以分解为更小的同类问题

### 经典案例：阶乘计算
```java
public class RecursionDemo {
    // 递归方法：计算n的阶乘
    public int factorial(int n) {
        // 递归终止条件
        if (n == 1) {
            return 1;
        }
        // 递归表达式：n! = n * (n-1)!
        return n * factorial(n - 1);
    }
    
    // 非递归方法：使用循环计算阶乘
    public int factorialIterative(int n) {
        int result = 1;
        for (int i = 1; i <= n; i++) {
            result *= i;
        }
        return result;
    }
    
    public static void main(String[] args) {
        RecursionDemo demo = new RecursionDemo();
        int n = 5;
        
        System.out.println(n + "的阶乘（递归）：" + demo.factorial(n));    // 120
        System.out.println(n + "的阶乘（迭代）：" + demo.factorialIterative(n));  // 120
    }
}
```

### 递归的优缺点
- **优点**：
  - 代码简洁，逻辑清晰
  - 适合解决具有递归性质的问题（如树结构遍历）
- **缺点**：
  - 递归深度过大可能导致栈溢出（StackOverflowError）
  - 性能通常比迭代方式差
  - 调试困难

### 递归与迭代对比
| 特性       | 递归                    | 迭代               |
| ---------- | ----------------------- | ------------------ |
| 实现方式   | 方法自身调用            | 循环结构           |
| 空间复杂度 | 较高（栈开销）          | 较低               |
| 时间复杂度 | 可能重复计算            | 通常更高效         |
| 代码可读性 | 更简洁                  | 可能更复杂         |
| 适用场景   | 树/图遍历、数学递归问题 | 数值计算、循环操作 |

## 综合案例：员工管理系统

### 员工类设计
```java
public class Employee {
    private String id;       // 员工编号
    private String name;     // 姓名
    private double salary;   // 薪资
    private Department dept; // 所属部门

    // 构造方法重载
    public Employee() {
        this("未知编号", "未知姓名", 0.0);
    }

    public Employee(String id, String name, double salary) {
        this.id = id;
        this.name = name;
        this.salary = salary;
    }

    public Employee(String id, String name, double salary, Department dept) {
        this(id, name, salary);
        this.dept = dept;
    }

    // Getter和Setter方法（使用this）
    public String getId() {
        return id;
    }

    public void setId(String id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    public Department getDept() {
        return dept;
    }

    public void setDept(Department dept) {
        this.dept = dept;
    }

    // 显示员工信息
    public void showInfo() {
        System.out.println("员工编号：" + id);
        System.out.println("姓名：" + name);
        System.out.println("薪资：" + salary);
        if (dept != null) {
            System.out.println("所属部门：" + dept.getName());
        }
    }
}
```

### 部门类设计
```java
public class Department {
    private String id;   // 部门编号
    private String name; // 部门名称

    // 构造方法
    public Department(String id, String name) {
        this.id = id;
        this.name = name;
    }

    // Getter和Setter
    public String getId() {
        return id;
    }

    public void setId(String id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    // 显示部门信息
    public void showInfo() {
        System.out.println("部门编号：" + id);
        System.out.println("部门名称：" + name);
    }
}
```

### 测试类
```java
public class EmployeeSystem {
    // 计算员工薪资增长（基本类型参数）
    public void raiseSalary(Employee emp, double percent) {
        double newSalary = emp.getSalary() * (1 + percent / 100);
        emp.setSalary(newSalary);
        System.out.println(emp.getName() + "的薪资增长" + percent + "%，新薪资：" + newSalary);
    }

    // 转移员工部门（引用类型参数）
    public void transferDepartment(Employee emp, Department newDept) {
        Department oldDept = emp.getDept();
        emp.setDept(newDept);
        if (oldDept != null) {
            System.out.println(emp.getName() + "从" + oldDept.getName() + "转移到" + newDept.getName());
        } else {
            System.out.println(emp.getName() + "加入" + newDept.getName());
        }
    }

    public static void main(String[] args) {
        // 创建部门
        Department devDept = new Department("D001", "研发部");
        Department hrDept = new Department("D002", "人事部");

        // 创建员工（使用不同构造方法）
        Employee emp1 = new Employee("E001", "张三", 10000.0, devDept);
        Employee emp2 = new Employee("E002", "李四", 8000.0);

        // 显示员工信息
        System.out.println("=== 员工信息 ===");
        emp1.showInfo();
        emp2.showInfo();

        // 测试方法调用
        EmployeeSystem system = new EmployeeSystem();
        system.raiseSalary(emp1, 10);  // 涨薪10%
        system.transferDepartment(emp2, hrDept);  // 转移部门

        // 显示更新后信息
        System.out.println("\n=== 更新后员工信息 ===");
        emp1.showInfo();
        emp2.showInfo();
    }
}
```

### 输出结果
```
=== 员工信息 ===
员工编号：E001
姓名：张三
薪资：10000.0
所属部门：研发部
员工编号：E002
姓名：李四
薪资：8000.0

张三的薪资增长10.0%，新薪资：11000.0
李四加入人事部

=== 更新后员工信息 ===
员工编号：E001
姓名：张三
薪资：11000.0
所属部门：研发部
员工编号：E002
姓名：李四
薪资：8000.0
所属部门：人事部
```

# 面向对象的封装特性和static关键字

## 封装

### 基本概念
封装是面向对象编程的三大特性之一，它通过将数据（成员变量）和操作数据的方法绑定在一起，并隐藏内部实现细节，只对外提供必要的接口，从而保证数据的安全性和完整性。

### 实现步骤
1. **私有化成员变量**：使用`private`关键字修饰成员变量，限制直接访问
2. **提供公共的访问方法**：通过`getter`和`setter`方法控制成员变量的访问和修改
3. **添加数据验证逻辑**：在`setter`方法中添加数据验证，确保数据的合理性

### 代码示例
```java
public class Car {
    // 1. 私有化成员变量
    private String brand;  // 品牌
    private String color;  // 颜色
    private int price;     // 价格
    
    // 无参构造方法
    public Car() {
    }
    
    // 带参构造方法
    public Car(String brand, String color, int price) {
        setBrand(brand);
        setColor(color);
        setPrice(price);
    }
    
    // 2. 提供公共的getter和setter方法
    public String getBrand() {
        return brand;
    }
    
    public void setBrand(String brand) {
        this.brand = brand;
    }
    
    public String getColor() {
        return color;
    }
    
    public void setColor(String color) {
        this.color = color;
    }
    
    public int getPrice() {
        return price;
    }
    
    public void setPrice(int price) {
        // 3. 添加数据验证逻辑
        if (price <= 0) {
            System.out.println("价格必须大于0");
            return;
        }
        this.price = price;
    }
    
    // 显示汽车信息
    public void showInfo() {
        System.out.println("品牌：" + brand + "，颜色：" + color + "，价格：" + price);
    }
}
```

### 封装的优点
1. **数据安全性**：防止外部直接访问和修改数据，通过方法控制数据的合法性
2. **可维护性**：内部实现可以自由修改，只要接口不变，不会影响外部调用
3. **隐藏实现细节**：降低系统的耦合度，提高代码的独立性

## static关键字

### 基本概念
`static`关键字用于修饰类的成员（成员变量、成员方法、代码块），使其成为类层级的成员，被所有对象共享。静态成员属于类，而不属于某个具体的对象。

### 静态变量
- **特点**：被所有对象共享，在内存中只有一份拷贝
- **生命周期**：随着类的加载而创建，随着类的卸载而销毁
- **访问方式**：推荐使用`类名.静态变量名`访问

### 静态方法
- **特点**：属于类，不属于对象，不能使用`this`关键字
- **访问限制**：只能访问静态成员（静态变量和静态方法）
- **调用方式**：推荐使用`类名.静态方法名`调用

### 代码示例
```java
public class Student {
    private String name;  // 实例变量：每个对象独立拥有
    private int age;      // 实例变量
    
    public static int count;  // 静态变量：所有对象共享
    
    public Student(String name, int age) {
        this.name = name;
        this.age = age;
        count++;  // 每创建一个对象，计数器加1
    }
    
    // 实例方法：可以访问实例变量和静态变量
    public void showInfo() {
        System.out.println("姓名：" + name + "，年龄：" + age + "，总人数：" + count);
    }
    
    // 静态方法：只能访问静态变量
    public static void printCount() {
        System.out.println("总人数：" + count);
        // 以下代码会报错，静态方法不能访问实例变量
        // System.out.println(name);  // 错误
    }
}
```

### 静态代码块
- **作用**：用于类的初始化操作，在类加载时执行，且只执行一次
- **语法**：
  ```java
  static {
      // 静态代码块
  }
  ```

### 代码示例
```java
public class StaticBlockDemo {
    public static int num;
    
    static {
        System.out.println("静态代码块执行");
        num = 100;  // 初始化静态变量
    }
    
    public static void main(String[] args) {
        System.out.println("num = " + num);  // 输出100
    }
}
```

## 单例设计模式

### 基本概念
单例设计模式是一种创建型设计模式，确保一个类只有一个实例，并提供一个全局访问点。常用于需要严格控制实例数量的场景，如配置管理器、数据库连接池等。

### 实现步骤
1. **私有化构造方法**：防止外部直接创建对象
2. **在类内部创建唯一实例**：使用静态变量保存
3. **提供公共的静态访问方法**：返回该实例

### 饿汉式实现
```java
public class Singleton {
    // 1. 私有化构造方法
    private Singleton() {
    }
    
    // 2. 在类内部创建唯一实例（饿汉式：类加载时就创建）
    private static final Singleton INSTANCE = new Singleton();
    
    // 3. 提供公共的静态访问方法
    public static Singleton getInstance() {
        return INSTANCE;
    }
}
```

### 懒汉式实现（线程安全）
```java
public class Singleton {
    // 1. 私有化构造方法
    private Singleton() {
    }
    
    // 2. 声明静态变量（懒汉式：延迟到第一次使用时创建）
    private static volatile Singleton INSTANCE;
    
    // 3. 提供公共的静态访问方法（线程安全）
    public static synchronized Singleton getInstance() {
        if (INSTANCE == null) {
            INSTANCE = new Singleton();
        }
        return INSTANCE;
    }
}
```

### 饿汉式 vs 懒汉式
| 特点         | 饿汉式                     | 懒汉式             |
| ------------ | -------------------------- | ------------------ |
| 实例创建时机 | 类加载时                   | 第一次调用时       |
| 线程安全性   | 天生线程安全               | 需要额外同步措施   |
| 优点         | 简单，无线程安全问题       | 延迟加载，节省资源 |
| 缺点         | 类加载即创建，可能浪费资源 | 实现复杂，性能稍低 |

## 继承

### 基本概念
继承是面向对象编程的另一个重要特性，它允许一个类（子类）继承另一个类（父类）的属性和方法，从而实现代码复用和扩展。

### 语法格式
```java
class 子类 extends 父类 {
    // 子类特有的属性和方法
}
```

### 继承的特点
1. **子类继承父类的成员**：包括成员变量和方法，但不包括构造方法
2. **单继承**：Java只支持单继承，即一个子类只能有一个直接父类
3. **传递性**：A继承B，B继承C，则A间接继承C
4. **is-a关系**：子类是父类的一种特殊类型

### 代码示例
```java
// 父类：Person
public class Person {
    private String name;
    private int age;
    
    public Person() {
    }
    
    public Person(String name, int age) {
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
    
    public void eat() {
        System.out.println(name + "正在吃饭...");
    }
    
    public void sleep() {
        System.out.println(name + "正在睡觉...");
    }
}

// 子类：Student
public class Student extends Person {
    private String studentId;  // 学号
    
    public Student() {
    }
    
    public Student(String name, int age, String studentId) {
        super(name, age);  // 调用父类的构造方法
        this.studentId = studentId;
    }
    
    public String getStudentId() {
        return studentId;
    }
    
    public void setStudentId(String studentId) {
        this.studentId = studentId;
    }
    
    // 子类特有的方法
    public void study() {
        System.out.println(getName() + "正在学习...");
    }
}
```

### 方法重写（Override）
- **概念**：子类重新定义父类中已有的方法
- **要求**：
  - 方法名、参数列表、返回值类型必须相同（JDK 1.5+允许返回子类类型）
  - 访问权限不能更严格（可以更宽松）
  - 不能抛出比父类更大的异常

### 代码示例
```java
// 父类
public class Animal {
    public void makeSound() {
        System.out.println("动物发出声音");
    }
}

// 子类
public class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("汪汪汪");
    }
}

// 测试类
public class Test {
    public static void main(String[] args) {
        Animal animal = new Animal();
        animal.makeSound();  // 输出：动物发出声音
        
        Dog dog = new Dog();
        dog.makeSound();     // 输出：汪汪汪
    }
}
```

## 访问控制符

### 访问控制级别
Java提供四种访问控制符，用于控制类、成员变量和方法的访问权限：

| 访问控制符  | 本类 | 同包类 | 子类 | 其他包类 |
| ----------- | ---- | ------ | ---- | -------- |
| `private`   | ✅    | ❌      | ❌    | ❌        |
| 默认        | ✅    | ✅      | ❌    | ❌        |
| `protected` | ✅    | ✅      | ✅    | ❌        |
| `public`    | ✅    | ✅      | ✅    | ✅        |

### 使用原则
- **成员变量**：通常使用`private`修饰，实现封装
- **方法**：通常使用`public`修饰，提供公共接口
- **构造方法**：根据需要选择访问控制符，单例模式使用`private`

### 包（Package）
- **作用**：组织类，避免命名冲突，控制访问权限
- **声明格式**：
  ```java
  package com.example.demo;
  ```
- **导入包**：
  ```java
  import com.example.demo.MyClass;
  ```

## final关键字

### 基本概念
`final`关键字表示"最终的"，可以修饰类、方法和变量：
- **修饰类**：类不能被继承（如`String`类）
- **修饰方法**：方法不能被重写（但可以被继承）
- **修饰变量**：变量成为常量，只能赋值一次

### 代码示例
```java
// 1. final修饰类：不能被继承
final class FinalClass {
    // 类的内容
}

// 以下代码会报错，因为FinalClass不能被继承
// class SubClass extends FinalClass {}

class Parent {
    // 2. final修饰方法：不能被重写
    public final void show() {
        System.out.println("Parent show()");
    }
}

class Child extends Parent {
    // 以下代码会报错，因为show()方法是final的
    // @Override
    // public void show() {
    //     System.out.println("Child show()");
    // }
}

class Constants {
    // 3. final修饰变量：常量，必须初始化且不能修改
    public final int MAX_VALUE = 100;
    public static final double PI = 3.14159;  // 静态常量
}
```

### 常量的命名规范
Java中常量通常使用全大写字母，单词间用下划线分隔：
```java
public static final int MAX_SIZE = 100;
public static final String DEFAULT_NAME = "unknown";
```

## 综合案例：银行账户系统

### 账户类设计
```java
public class Account {
    // 1. 封装成员变量
    private String accountNumber;  // 账号
    private String owner;          // 户主
    private double balance;        // 余额
    
    // 2. 静态变量：记录账户总数
    public static int totalAccounts = 0;
    
    // 3. 常量：利率
    public static final double INTEREST_RATE = 0.03;
    
    // 4. 构造方法
    public Account(String accountNumber, String owner, double balance) {
        this.accountNumber = accountNumber;
        this.owner = owner;
        this.balance = balance;
        totalAccounts++;  // 账户总数加1
    }
    
    // 5. getter和setter方法
    public String getAccountNumber() {
        return accountNumber;
    }
    
    public String getOwner() {
        return owner;
    }
    
    public void setOwner(String owner) {
        this.owner = owner;
    }
    
    public double getBalance() {
        return balance;
    }
    
    // 6. 业务方法
    public void deposit(double amount) {
        if (amount <= 0) {
            System.out.println("存款金额必须大于0");
            return;
        }
        balance += amount;
        System.out.println("存款成功，当前余额：" + balance);
    }
    
    public void withdraw(double amount) {
        if (amount <= 0) {
            System.out.println("取款金额必须大于0");
            return;
        }
        if (amount > balance) {
            System.out.println("余额不足");
            return;
        }
        balance -= amount;
        System.out.println("取款成功，当前余额：" + balance);
    }
    
    // 7. 静态方法：获取总账户数
    public static int getTotalAccounts() {
        return totalAccounts;
    }
    
    // 8. 显示账户信息
    public void showInfo() {
        System.out.println("账号：" + accountNumber);
        System.out.println("户主：" + owner);
        System.out.println("余额：" + balance);
        System.out.println("年利率：" + INTEREST_RATE * 100 + "%");
    }
}
```

### 测试类
```java
public class BankSystem {
    public static void main(String[] args) {
        // 创建账户
        Account account1 = new Account("1001", "张三", 1000.0);
        Account account2 = new Account("1002", "李四", 2000.0);
        
        // 显示账户信息
        System.out.println("=== 账户1信息 ===");
        account1.showInfo();
        
        System.out.println("\n=== 账户2信息 ===");
        account2.showInfo();
        
        // 账户操作
        System.out.println("\n=== 账户1操作 ===");
        account1.deposit(500);
        account1.withdraw(300);
        
        // 静态方法调用
        System.out.println("\n当前账户总数：" + Account.getTotalAccounts());
    }
}
```

### 输出结果
```
=== 账户1信息 ===
账号：1001
户主：张三
余额：1000.0
年利率：3.0%

=== 账户2信息 ===
账号：1002
户主：李四
余额：2000.0
年利率：3.0%

=== 账户1操作 ===
存款成功，当前余额：1500.0
取款成功，当前余额：1200.0

当前账户总数：2
```

# 面向对象的多态特性及抽象类和接口

## 多态

### 基本概念

多态主要指同一种事物表现出来的多种形态。

- 饮料：可乐、雪碧、脉动、乐虎、红牛
- 宠物：狗、猫、鸟、乌龟、鱼
- 人：学生、教师、工人

### 语法格式

父类类型 引用变量名 = new 子类类型();

**示例**：

```java
Person pw = new Worker();
pw.show();
```

### 练习

编程实现Person类的封装，特有：姓名和年龄，要求提供打印所有特征的行为。  
编程实现Worker类的封装继承Person类，特征有：薪水。

### 多态的效果

1. 当父类的引用指向子类的对象时，父类的引用可以直接调用父类独有的方法。
2. 当父类的引用指向子类的对象时，父类的引用不可以直接调用子类独有的方法。
3. 对于父子类都有的非静态成员方法：编译阶段调用父类版本，运行阶段调用子类重写后的版本。
4. 对于父子类都有的静态方法：编译和运行阶段调用父类版本，隶属于类层级，与指向的对象无关。

### 代码示例

```java
public class Person {
    private String name;
    private int age;

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
        if (age > 0 && age < 150) {
            this.age = age;
        } else {
            System.out.println("年龄不合理！！！");
        }
    }

    public void show() {
        System.out.println("我是" + getName() + "，今年" + getAge() + "岁了！");
    }
}
```

```java
public class Worker extends Person {
    private int salary;

    public Worker() {
        super();
    }

    public Worker(String name, int age, int salary) {
        super(name, age);
        setSalary(salary);
    }

    public int getSalary() {
        return salary;
    }

    public void setSalary(int salary) {
        if (salary >= 0) {
            this.salary = salary;
        } else {
            System.out.println("薪资不能为负数！");
        }
    }
}
```

```java
public class PersonWorkerTest {
    public static void main(String[] args) {
        // 情况1：父类引用指向父类对象（无多态）
        Person p = new Person("zhangfei", 30);
        p.show();

        // 情况2：子类引用指向子类对象（无多态）
        Worker w = new Worker("guanyu", 35, 4000);
        w.show();

        // 情况3：父类引用指向子类对象（多态）
        Person pw = new Worker("liubei", 40, 8000);
        pw.show();
    }
}
```

### 引用数据类型之间的转换

1. **类型转换分类**：
   - 自动类型转换：从小范围到大范围（子类到父类）
   - 强制类型转换：从大范围到小范围（父类到子类）
2. 引用数据类型之间的转换必须发生在父子类之间，否则编译报错。
3. 若转换到的目标类型是子类类型但不是该引用真正指向的子类类型，编译通过，运行阶段发生类型转换异常。
4. 避免错误：使用`instanceof`判断，格式为`if(引用变量名 instanceof 数据类型)`。

### 多态的意义

多态的实际意义在于可以屏蔽不同子类的差异性实现通用的编程，但可以调用不同的方法带来不同的结果。

## 抽象类

### 抽象方法的概念

抽象方法是指不能具体实现的方法，没有方法体并使用`abstract`关键字修饰。  
**语法格式**：

```
访问控制符 abstract 返回值类型 方法名称(形参列表);
```

**示例**：

```java
public abstract void cry();
```

### 抽象类的概念

抽象类是指不能具体实例化的类，不能创建对象并使用`abstract`关键字修饰。

### 注意事项

1. 抽象类中可以有成员变量、构造方法以及成员方法。
2. 抽象类中可以有抽象方法也可以没有抽象方法。
3. 拥有抽象方法的类必须是抽象类，严格来说，具有抽象方法并且使用`abstract`关键字修饰的类才算真正意义上的抽象类。

### 实际意义

抽象类的意义不在于自身创建对象而在于被继承，当一个类继承抽象类后必须重写抽象类中的抽象方法，否则该类也变成抽象类。抽象类对子类具有强制性和规范性，因此叫做模板设计模式。

### 经验分享

开发中推荐使用多态的语法格式，当父类的引用指向子类的对象时，父类引用直接调用的所有方法一定是父类拥有的方法，若希望更换子类时，只需要将`new`关键字后面的类型修改而其它地方无需更改立即生效，从而提高了代码的可维护性。缺点是父类引用不能直接访问子类独有的方法，需要强转。

## 接口

### 基本概念

接口是一种比抽象类还抽象的类，体现为所有成员方法都是抽象方法。  

- 定义类的关键字是`class`，定义接口的关键字是`interface`。
- 继承类的关键字是`extends`，实现接口的关键字是`implements`。

### 代码示例

```java
package cn.learn.day10;

public interface InterfaceTest {
    // 接口常量声明（默认public static final可省略）
    int CNT = 1;  // 等价于 public static final int CNT = 1
    
    // 抽象方法声明（默认public abstract可省略）
    void show();  // 等价于 public abstract void show()
}
```

### 类和接口之间的关系

| 关系类型           | 表达关键字   | 支持特性   |
| ------------------ | ------------ | ---------- |
| 类和类之间的关系   | `extends`    | 支持单继承 |
| 类和接口之间的关系 | `implements` | 支持多实现 |
| 接口之间的关系     | `extends`    | 支持多继承 |

### 接口实现示例

```java
public interface Metal {
    // 声明抽象方法（描述金属发光行为）
    public abstract void shine();
}
```

```java
public interface Money {
    // 声明抽象方法（定义货币购买行为规范）
    public abstract void buy();
}
```

```java
public class Gold implements Money, Metal {
    @Override
    public void shine() {
        System.out.println("发出了金黄色的光芒...");
    }

    @Override
    public void buy() {
        System.out.println("买了好多好吃的..."); 
    }
    public static void main(String[] args) {
        // 接口类型的引用指向实现类的对象，形成了多态
        Metal mt = new Gold();
        mt.shine();
        
        System.out.println("------------------------");
        
        Money mn = new Gold();
        mn.buy();
    }
}
```

### 抽象类和接口之间的区别

1. 定义抽象类的关键字是`abstract class`，定义接口的关键字是`interface`。
2. 继承抽象类的关键字是`extend`，实现接口的关键字是`implements`。
3. 继承抽象类支持单继承，实现接口可以多实现。
4. 抽象类中可以有构造方法，接口中不可以有构造方法。
5. 抽象类中可以有成员变量，接口中只可以有常量。
6. 抽象类中可以有成员方法，接口中只可以有抽象方法。
7. 抽象类中增加方法可以不影响子类，接口中增加方法通常都影响子类。
8. 从JDK1.8开始允许接口中出现非抽象方法，但需要使用`default`关键字修饰。

## 匿名内部类

### 语法格式

```
接口/父类类型 引用变量名 = new 接口/父类类型(){方法的重写};
```

### 示例

```java
public interface A {
    public abstract void show();
}
```

```java
public class ATest implements A {
    // A是个接口类型，因此下面就是接口类型的引用作为方法的形参
    public static void test(A a) {
        // 在编译阶段调用A接口中的show方法，在运行阶段调用实现类中重写的版本
        a.show();
    }
    public static void main(String[] args) {
        // A是个接口类型，比抽象类还抽象，不能创建对象
        // ATest.test(new A());// error
        ATest.test(new subA());
    }
}
```

## 内部类

### 基本概念

当一个类的定义出现在另外一个类的类体中时，这个类叫做内部类，内部类所在的类叫做外部类。  
类中的内容：成员变量、成员方法、构造方法、静态成员、构造块和静态代码块、内部类。

### 语法格式

```java
class 外部类名 {
    class 内部类名 {
        内部类的类体；
    }
}
```

**示例**：

```java
class A {
    class B {
    }
}
```

### 实际作用

当一个类存在的价值仅仅是为某一个类单独服务时，可将这个类定义为所服务类中的内部类，这样可以隐藏该类的实现细节并且可以方便的访问外部类的私有成员而不再需要提供公有的get和set方法。

### 基本分类

1. **普通内部类**：直接将一个类的定义放在另外一个类的类体中，隶属于对象层级。
2. **静态内部类**：使用`static`关键字修饰的内部类，隶属于类层级。
3. **局部内部类**：直接将一个类的定义放在方法体的内部，作用范围是从声明开始一直到方法体结束。

### 代码示例

```java
public class TestInner {
    private int cnt = 1;

    // 在类体中定义一个普通内部类 隶属于对象层级
    class Inner {
        void show() {
            System.out.println("cnt = " + cnt);
        }
    }

    public static void main(String[] args) {
        // 声明外部类的引用指向外部类的对象
        TestInner ti = new TestInner();
        // 声明内部类的引用指向内部类的对象后调用show方法
        Inner in = ti.new Inner();
        in.show();
    }
}
```

```java
public class TestStaticInner {
    private int cnt = 1;        // 实例变量（对象层级）
    private static int snt = 2; // 类变量（类层级）

    static class Inner {        // 静态内部类（类层级）
        void show() {
            // System.out.println(cnt);  // 编译错误！
            System.out.println("snt = " + snt); // 允许访问
        }
    }
}
```

# JavaSE核心类库

## Object类

## 常用的包

### java.lang包

- 该包是Java语言中的核心包，由Java虚拟机自动导入。
- **示例类**：
  - String类
  - System类等

### java.util包

- 该包是Java语言中的工具包，包含大量的工具类和集合类等。
- **示例类**：
  - Scanner类
  - Random类等

### java.io包

- 该包是Java语言中的输入输出包，包含大量读写文件的类等。
- **示例类**：
  - FileOutputStream类
  - FileInputStream类等

### java.net包

- 该包是Java语言中的网络包，包含大量网络编程的类等。
- **示例类**：
  - ServerSocket类
  - Socket类等

