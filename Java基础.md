

# Java基础

## 计算机的体系结构

- 基本概念

  * 计算机（Computer）俗称“电脑”，是现代一种被用于高级计算，使用非常广泛的设备，主要有硬件软件两部分构成。

  - 计算机硬件是客观存在的各种计算机相关设备，而计算机的软件是用于控制各种硬件设备完成各种功能。

    


## 常见的计算机硬件

计算机中常见的硬件有：CPU、内存、硬盘、显卡、键盘、显示器、鼠标...

- CPU

  - 中央处理器，是计算机中最核心的部件，相当于人的大脑

  - 主要用于处理各种计算机的指令以及软件中的数据等。


- 内存

  - 是计算机中的存储部件。

  - 主要用于临时存放CPU访问的数据内容，CPU直接访问且效率高。 

  - 容量小，一旦断电会造成数据的丢失。

  - 拓展
    - 1Tb = 1024Gb
    - 1GB = 1024Mb
    - 1Mb = 1024Kb
    - 1Kb = 1024bytb（字节） 通常一个英文字母占1个字节，一个汉字占2个字节
    - 1byte = 8bit（二进 制位）在计算机的底层识别0和1组成的二进制序列


- 硬盘

  - 是计算机中的存储部件。

  - CPU不能直接访问硬盘中的数据，因此效率比较低。

  - 容量大，若断电不会造成数据的丢失。


## 常见的计算机软件

- 计算机常见的软件主要分为两部分：	系统软件 和 应用软件。
- 其中系统软件主要指操作系统，主流操作系统:Windows/Unix/Linux/ios/Android
- 其中应用软件主要指安装在操作系统之上的软件:QQ、迅雷、火狐浏览器…..

## 计算机的体系结构

使用者 => 应用软件 => 系统软件 => 硬件设备 => 其中系统软件分为：内核（Kernel）和外壳（Shell）



## Java语言的概述

- jdk的下载和安装
  - 官网下载
  - 搜索下载

- 相关概念
  - jdk - Java开发工具包，只要做Java开发就需要下载和安装该软件。
  - jre - Java运行时环境信息，只要运行Java程序就需要下载和安装该软件。
  - jvm - Java虚拟机，时Java程序与计算机操作系统之间的桥梁
  - javac.exe - Java语言的编译器，主要用于将Java源代码编译生成字节码文件。
  - java.exe - Java语言的解释器，主要用于启动Java虚拟机对字节码文件进行解释执行。

- Java程序的编写流程
  - 新建文本文档，修改文件名后缀为.java；
  - 编写代码后保存；
  - 在命令行窗口中使用切换到你写的.java文件的所在路径；
  - 使用javac *.java进行编译,生成 *.class的字节码文件；
  - 使用java xxx进行解释执行，打印结果

- 第一个Java程序

  ```java
  public class HelloWorld {
      public static void main(String[] args) {
          System.out.println("Hello World!");
      }
  }
  ```

- 环境变量配置
  - 如若希望可以在任意路径的命令行窗口使用java javac等命令执行文件，需将可执行文件的路径信息配置到环境变量Path中。
  - 计算机=>右键，选择属性=>高级系统设置=>高级=>环境变量=>系统变量找到Path，点击编辑=>将javac.exe所在的路径信息复制到Path变量值的最前面，加上英文版的分号 =>一路点击确定即可



## 变量和注释

- 基本概念

  - 当需要在Java程序中记录单个数据内容时，则声明一个变量即可，而声明变量的本质就是在内存空间中申请一块存储单元，由于该存储单元的数值可以改变，因此得名为"变量”。
  - 由于存放数据内容的大小不同导致所需存储单元的容量不同，在Java语言中使用数据类型加以描述，为了便于下次访问还需要指定变量的名称。

- 声明方式

  - 数据类型 变量名 = 初始值；如int a = 10；

- 标识符命名规则

  - 要求由数字、字母、下划线以及$组成，不能以数字开头。如name、name_1...
  - 要求不能使用Java中的关键字。如public、class、if...
  - 区分大小写，没有长度限制但不宜过长。如name和Name不是同一变量，但不推荐这种写法
  - 做到见名知意。

- 示例：

  ```java
  import java.util.Scanner;
  
  public class demo1 {
      public static void main(String[] args) {
          //提示输入姓名和年龄
          System.out.println("请输入姓名和年龄：");
          Scanner sc = new Scanner(System.in);
        	//、变量随时用随生成
          name = sc.next();
          age = sc.nextInt();
          //打印姓名和年龄
          System.out.println("姓名："+name+"，年龄："+age);
      }
  }
  ```

- 注释

  - //单行注释，从//开始到当前行末尾都是注释。
  - /* */多行注释，从 / *开始到 */结束都是注释内容。（不允许嵌套使用）

## 数据类型

- 基本分类

  - 在Java语言中分为两大类

    - 基本数据类型
      - byte、shortint、long、float、double、boolean、char

    - 引用数据类型
      - 数组、类、接口、注解、枚举

- 常见的进制
  - 在日常生活中使用10进制，权重10^0、10^1……
  - 在计算机底层采用二进制，权重2^0、2^1……
  - 二进制最高位代表符号位，若是0则为非负数，1代表复数。

- 进制之间的转换

  - 正十进制转二进制
    - 除2取余发，使用十进制整数不断地除以2直到商为0时将余数逆序排序即可
    - 拆分发，将十进制整数拆分为若干个二进制权重的和，若有该权重下面写1，否则写0

  - 正二进制转十进制
    - 加权法，使用二进制中的每个数字乘以当前位的权重再累加起来。

  - 负十进制转换为二进制
    - 先将十进制的绝对值转换为二进制，进行按位取反再加1。

  - 负二进制转换为十进制
    - 先减1再按位取反，然后合并为添加负号



## 运算符

- 算数运算符

  - +表示加法运算符	/表示除法运算符	-表示减法运算符	%表示取模/取余运算符
    *表示乘法运算符

    ```java
    public class demo {
        public static void main(String[] args) {
            // 定义两个整数变量 a 和 b
            int a = 10;
            int b = 3;
    
            // 使用加法运算符 +
            int sum = a + b;
            System.out.println("a + b = " + sum); // 输出结果：a + b = 13
    
            // 使用减法运算符 -
            int difference = a - b;
            System.out.println("a - b = " + difference); // 输出结果：a - b = 7
    
            // 使用乘法运算符 *
            int product = a * b;
            System.out.println("a * b = " + product); // 输出结果：a * b = 30
    
            // 使用除法运算符 /
            int quotient = a / b;
            System.out.println("a / b = " + quotient); // 输出结果：a / b = 3（整数除法）
    
            // 使用取模运算符 %
            int remainder = a % b;
            System.out.println("a % b = " + remainder); // 输出结果：a % b = 1（余数）
        }
    }
    ```

  - 说明

    - 在Java语言中两个整数相除时结果只保留整数部分丢弃小数部分
    - 若希望保留小数部分，则处理方式如下:
      - a.将其中任意一个操作数强转为double类型进行运算即可;
      - b.让其中任意一个操作数乘W1.0后进行运算即可(推荐);

    - 0不能做除数，0.0可以做除数但结果是无穷；
    - +既可以作为算术运算符也可以作为字符串连接符，区分方式如下对待，结果字符串只要+两端的操作数中有一个是字符串类型，则按照字符串连接符。

- 关系/比较预算符

  - ">"表示是否大于运算符	"<"表示是否小于运算符	"=="表示是否等于运算符
    ">="表示是否大于等于运算符	"<="表示是否小于等于运算符	"！="表示是否不等于运算符

  - 所有以关系运算符作为最终运算符的表达式结果一定是boolean类型，只有true和false

    ```java
    public class demo {
        public static void main(String[] args) {
            int ia = 3;
            int ib = 2;
            System.out.println("ia = " + ia); // ia = 3
            System.out.println("ib = " + ib); // ib = 2
    
            System.out.println("---------------------------------------------");
            // 使用关系运算符进行比较并打印结果
            System.out.println(ia > ib);     // true
            System.out.println(ia >= ib);    // true
            System.out.println(ia < ib);     // false
            System.out.println(ia <= ib);    // false
            System.out.println(ia == ib);    // false
            System.out.println(ia != ib);    // true
        }
    }
    ```

- 自增减运算符

  - ++自增运算符，--自减运算符，使变量自身数值加减1。

    ```java
    public class demo {
        public static void main(String[] args) {
            // 定义一个整数变量
            int num = 5;
    
            // 前置自增：先增加再使用
            System.out.println("前置自增: " + ++num); // 输出 6，因为 num 先加 1 变为 6，然后输出 6
            System.out.println("num 的当前值: " + num); // 输出 6
    
            // 后置自增：先使用再增加
            System.out.println("后置自增: " + num++); // 输出 6，因为 num 先输出 6，然后加 1 变为 7
            System.out.println("num 的当前值: " + num); // 输出 7
    
            // 前置自减：先减少再使用
            System.out.println("前置自减: " + --num); // 输出 6，因为 num 先减 1 变为 6，然后输出 6
            System.out.println("num 的当前值: " + num); // 输出 6
    
            // 后置自减：先使用再减少
            System.out.println("后置自减: " + num--); // 输出 6，因为 num 先输出 6，然后减 1 变为 5
            System.out.println("num 的当前值: " + num); // 输出 5
    
            // 总结：前置运算符（++num 或 --num）会在使用变量值之前改变其值，
            // 而后置运算符（num++ 或 num--）会在使用变量值之后改变其值。
        }
    }
    ```

- 逻辑运算符

  - &&表示逻辑与，相当于“并且”，同真为真，一假为假。

  - ||表示逻辑或，相当于“或者”，一真为真，同假为假。

  - ！表示逻辑非，相当于“取反”，真的是假的，假的是真的。

  - 逻辑运算符两端的操作数都是boolean类型的，结果也是boolean。

    - 短路特性：对于逻辑与来说，若第一个为假则不看第二个；对逻辑或来说，第一个是真，第二个也不看。

      ```java
      public class demo {
          public static void main(String[] args) {
              int ia = 3;
              int ib = 2;
              System.out.println("ia = " + ia); // ia = 3
              System.out.println("ib = " + ib); // ib = 2
      
              System.out.println("---------------------------------------------");
              // 使用关系运算符进行比较并打印结果
              System.out.println(ia > ib);     // true
              System.out.println(ia >= ib);    // true
              System.out.println(ia < ib);     // false
              System.out.println(ia <= ib);    // false
              System.out.println(ia == ib);    // false
              System.out.println(ia != ib);    // true
      
              System.out.println("---------------------------------------------");
              // 短路原则示例
      
              // 短路与 (&&)
              boolean resultAnd = (ia > 0 && printAndCheck(ib > 0));
              System.out.println("Result of (ia > 0 && ib > 0): " + resultAnd);
      
              // 短路或 (||)
              boolean resultOr = (ia < 0 || printAndCheck(ib > 0));
              System.out.println("Result of (ia < 0 || ib > 0): " + resultOr);
          }
      
          // 辅助方法，用于检查短路原则
          private static boolean printAndCheck(boolean condition) {
              System.out.println("Checking condition: " + condition);
              return condition;
          }
      }
      ```

- 条件运算符

  - 三目运算符（？：）怎么说呢，先看问号前面的条件表达式，为true则取：前的表达式，反之取：之后的表达式。

- 赋值运算符

  - 简单赋值
    - 将右边的给左边。

  - 复合赋值
    - +=、-=、*=……

- 运算符优先级

  - （）极高

  - = 极低

    ```java
    public class demo {
        public static void main(String[] args) {
            // 定义变量
            int a = 10;
            int b = 5;
            int c = 2;
            int d = 3;
    
            // 示例表达式：a + b * c - d / c
            int result = a + b * c - d / c;
            System.out.println("Result of a + b * c - d / c: " + result);
    
            // 分步解释表达式的计算过程
            // 1. 乘法和除法（* 和 /）优先级高于加法和减法（+ 和 -）
            //    b * c = 5 * 2 = 10
            //    d / c = 3 / 2 = 1 (整数除法)
            // 2. 然后进行加法和减法
            //    a + 10 - 1 = 10 + 10 - 1 = 19
    
            // 使用括号改变优先级
            int resultWithParentheses = (a + b) * (c - d / c);
            System.out.println("Result with parentheses (a + b) * (c - d / c): " + resultWithParentheses);
    
            // 分步解释表达式的计算过程
            // 1. 先计算括号内的表达式
            //    a + b = 10 + 5 = 15
            //    d / c = 3 / 2 = 1 (整数除法)
            //    c - 1 = 2 - 1 = 1
            // 2. 然后进行乘法
            //    15 * 1 = 15
    
            // 结合逻辑运算符的优先级
            boolean flag1 = true;
            boolean flag2 = false;
            int x = 1;
            int y = 2;
    
            boolean logicalResult = (x > 0 && y > 0) || (flag1 && !flag2);
            System.out.println("Logical result (x > 0 && y > 0) || (flag1 && !flag2): " + logicalResult);
    
            // 分步解释逻辑表达式的计算过程
            // 1. 先计算关系表达式
            //    x > 0 = true
            //    y > 0 = true
            //    flag1 = true
            //    !flag2 = true (flag2 的否定)
            // 2. 然后进行逻辑与（&&）和逻辑或（||）运算
            //    (true && true) || (true && true) = true || true = true
        }
    }
    ```

- 字符串连接符

  - +

- 移位运算符

  - "<<"表示左移运算符，用于将数据的二进制位向左移动，右边使用0补充。
  - ">>"表示右移运算符,用于将数据的二进制位向右移动，左边使用符号位补充。
  - ">>>"表示逻辑右移运算符,用于将数据的二进制位向右移动，左边使用0补充。

- 位运算符

  - &表示按位与运算符，就是按照二进制位进行与运算，同1为1，一0为0(1-真 0-假)。
  - |表示按位或运算符，就是按照二进制位进行或运算，一1为1，同0为0.表示按位取反运算符。
  - ~按照二进制位进行取反，1为0，0为1.表示按位异或运算符。
  - ^按照二进制位进行异或运算，相同为0，不同为1。

## 分支结构

- 基本概念

  - 在某些特殊场合中需要进行判断并做出选择时，就需要使用分支结构

- if分支结构

  - if(条件表达式){

    ​	语句块;

    }

  - 执行流程

    - 判断条件表达式是否成立	
      - 若成立，则执行语句块
      - 不成立，则跳过语句块

- if-else-else分支结构

  - if（条件）{

    ​	语句；

    }else if（条件）{

    ​	语句；

    }else{

    ​	语句；

    }

  ```java
  public class demo4 {
      public static void main(String[] args) {
          // 定义一个学生的分数
          int score = 85;
  
          // 使用 if-else 条件判断进行成绩评级
          if (score >= 90) {
              System.out.println("你的成绩是 A");
          } else if (score >= 80) {
              System.out.println("你的成绩是 B");
          } else if (score >= 70) {
              System.out.println("你的成绩是 C");
          } else if (score >= 60) {
              System.out.println("你的成绩是 D");
          } else {
              System.out.println("你的成绩是 E，不及格");
          }
      }
  }
  ```

## 循环结构

- 基本概念

  - 在某些特殊场合中需要重复执行一段代码时，借助循环结构加以处理。

- for循环

  - 语法结构

  - for（初始化表达式；条件表达式；修改初始值表达式）{

    ​	循环体；

    }

  - 执行流程

  - 执行初始化表达式=>判断条件表达式是否成立=>若成立，则执行循环体=>修改初始值表达式=>判断条件表达式是否成立=>若不成立，则循环结束

- break和continue关键字

  - break关键字用于循环中表示跳出当前循环;

  - continue关键字用于循环中表示结束本次循环继续下一次循环。

  - 

  - ```java
    public static void main(String[] args) {
        int sum = 0;
    
        for (int i = 1; i <= 10; i++) {
            if (i == 6) {
                break; // 当i等于6时退出循环
            }
            if (i % 2 == 0) {
                continue; // 如果i是偶数，则跳过当前迭代
            }
            sum += i;
            System.out.println("累加结果：" + sum);
        }
    
        System.out.println("最终累加结果：" + sum);
    }
    ```

- 特殊的循环

  - for(；；)这种没有循环条件的循环叫做无限循环，俗称"死循环”

- 双重循环

  - 语法格式

  - for（初始表达式1；条件表达式2；修改初始值表达式3）{

    ​	for（初始表达式4；条件表达式5；修改初始值表达式6）{

    ​		循环体；

    ​	}

    }

  - 来点干货，怎么说呢来到双重循环，空间复杂度来到O(n^2)，大体流程就是第一层循环进来，要把里面的循环走到底或者在遇到break和return等才会结束，来进行第一层循环的下一次。

```java
public static void main(String[] args) {
    int n = 5; // 控制菱形的高度（上半部分）

    // 打印上半部分（含中间行）
    for (int i = 1; i <= n; i++) {
        // 打印空格
        for (int j = 1; j <= n - i; j++) {
            System.out.print(" ");
        }
        // 打印星号
        for (int k = 1; k <= 2 * i - 1; k++) {
            System.out.print("*");
        }
        System.out.println();
    }

    // 打印下半部分（不含中间行）
    for (int i = n - 1; i >= 1; i--) {
        // 打印空格
        for (int j = 1; j <= n - i; j++) {
            System.out.print(" ");
        }
        // 打印星号
        for (int k = 1; k <= 2 * i - 1; k++) {
            System.out.print("*");
        }
        System.out.println();
    }
}
```

- while循环

  - 语法格式

  - while（条件表达式）{

    ​	循环体；

    }

  - 和for差不多吧，就是初始值和修改初始值要换个地方，后续的变种和衍生，我的评价是不如for一根。

```java
/**
     * 看吧实现相同的功能，但是初始值的定义和变化没有固定的位置，显得不够严谨
     */
    public static void main(String[] args) {
        int n = 5; // 控制菱形上半部分的行数（含中间行）

        int i = 1;
        // 打印上半部分
        while (i <= n) {
            int j = 1;
            // 打印空格
            while (j <= n - i) {
                System.out.print(" ");
                j++;
            }

            j = 1;
            // 打印星号
            while (j <= 2 * i - 1) {
                System.out.print("*");
                j++;
            }

            System.out.println();
            i++;
        }

        i = n - 1;
        // 打印下半部分
        while (i >= 1) {
            int j = 1;
            // 打印空格
            while (j <= n - i) {
                System.out.print(" ");
                j++;
            }

            j = 1;
            // 打印星号
            while (j <= 2 * i - 1) {
                System.out.print("*");
                j++;
            }

            System.out.println();
            i--;
        }
    }
```

## 分支结构

- switch-case分支结构

  - 语法

  - switch（变量/表达式）{

    case 字面值1 ： 语句块1；break；

    case 字面值2 ： 语句块2；break；

    ……

    default：语句块n；

    }

  - 怎么说呢，像之前的if-else if-……-else的多分支结构。八百年用一次，学了之后在两年后的McpServer调用tools的时候用了一次（官方还不推荐使用这种方式）。

```java
public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    System.out.print("请输入一个数字（1-4）：");
    int choice = scanner.nextInt();

    switch (choice) {
        case 1:
            System.out.println("你选择了：选项一");
            break;
        case 2:
            System.out.println("你选择了：选项二");
            break;
        case 3:
            System.out.println("你选择了：选项三");
            break;
        case 4:
            System.out.println("你选择了：选项四");
            break;
        default:
            System.out.println("输入错误：请输入1到4之间的数字");
            break;
    }

    scanner.close();
}
```



## 一维数组

- 基本概念

  - 当需要存放同一类型的多个数据是可以声明数组。在空间上看就是在内存上申请一段连续的存储单元。

- 声明方式

  - 数据类型[] 数组名 = new 数据类型 [数组长度]；

  - 如int[] arr = {1, 2, 3, 4, 5};

    int[] arr = new int[5]; 

- 想要访问数组中的数据是根据数组的下标来访问的，下标从0开始。

- 数据初始化

  ```java
  public static void main(String[] args) {
          // 声明一个长度为5的double数组
          double[] numbers = {1.12, 2.56, 3.45, 4.62, 5.56};
          
  		//单个赋值
          numbers[2] = 3.21;
      
      	// 打印数组元素
          for (int i = 0; i < numbers.length; i++) {
              System.out.println("numbers[" + i + "] = " + numbers[i]);
          }
      }
  ```

- 数组的增删改查

  ```java
  public static void main(String[] args) {
          // 初始化数组
          int[] arr = {10, 20, 30, 40};
  
          System.out.println("原始数组：" + Arrays.toString(arr));
  
          // 修改元素（Update）
          int indexToUpdate = 1;
          int newValue = 25;
          if (indexToUpdate >= 0 && indexToUpdate < arr.length) {
              arr[indexToUpdate] = newValue;
              System.out.println("修改后数组：" + Arrays.toString(arr));
          }
  
          // 查询元素（Read）
          int valueToFind = 30;
          boolean found = false;
          for (int i = 0; i < arr.length; i++) {
              if (arr[i] == valueToFind) {
                  System.out.println("找到值 " + valueToFind + " 在索引 " + i);
                  found = true;
                  break;
              }
          }
          if (!found) {
              System.out.println("未找到值：" + valueToFind);
          }
  
          // 新增元素（Add）到指定位置
          for (int i = arr.length - 1; i > 0; i--) {
              arr[i] = arr[i - 1];
          }
          arr[0] = 50;
          System.out.println("新增后数组：" + Arrays.toString(arr));
  
          // 删除元素（Delete）指定索引处的元素
          int indexToDelete = 2;
          if (indexToDelete >= 0 && indexToDelete < arr.length) {
              for (int i = indexToDelete; i < arr.length - 1; i++) {
                  arr[i] = arr[i + 1];
              }
              arr[arr.length - 1] = 0; // 可选：将最后一个元素置为0（或其它默认值）
              System.out.println("删除后数组：" + Arrays.toString(arr));
          }
      }
  ```

- 关于这段代码有几个注意点

  - toString是java自带的工具包中Arrays包的方法，这里的运用是将数组内容包括[] ,等符号转成一个字符串。
  - length是数组的一个属性，其值描述的是数组的长度。

## 二维数组

- 基本概念
  - 如果说从单个元素到数组是从点到线的话，那么从一维数组到二维数组就是从线到面。也就是说二维数组中的每一个元素都是一个一维数组。

```java
public static void main(String[] args) {
    // 1. 二维数组的声明和静态初始化
    int[][] array = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
    };

    // 2. 二维数组的访问
    int value = array[1][2]; // 访问第二行第三列的元素
    System.out.println("array[1][2] 的值为: " + value);

    // 3. 二维数组的遍历
    System.out.println("二维数组的所有元素为:");
    for (int i = 0; i < array.length; i++) { // 外层循环遍历行
        for (int j = 0; j < array[i].length; j++) { // 内层循环遍历列
            System.out.print(array[i][j] + " ");
        }
        System.out.println(); // 每行结束后换行
    }

    // 4. 二维数组的动态初始化
    int[][] dynamicArray = new int[3][3];

    // 逐个元素赋值
    for (int i = 0; i < dynamicArray.length; i++) {
        for (int j = 0; j < dynamicArray[i].length; j++) {
            dynamicArray[i][j] = i * 3 + j + 1;
        }
    }

    // 遍历动态初始化的二维数组
    System.out.println("动态初始化的二维数组的所有元素为:");
    for (int i = 0; i < dynamicArray.length; i++) {
        for (int j = 0; j < dynamicArray[i].length; j++) {
            System.out.print(dynamicArray[i][j] + " ");
        }
        System.out.println();
    }
}
```



## 面向对象编程的概念

- 什么是对象
  - 万物皆对象。

- 什么是面向对象
  - 面向对象就是指以特征(属性)和行为的观点去分析现实世界中事物的方式。

- 什么是面向对象编程？
  - 面向对象编程就是指先使用面向对象的方式进行分析，再使用任意一门面向对象的编
    程语言进行翻译的过程。

- 如何学好面向对象编程？
  - 深刻理解面向对象编程的三大特征:封装、继承、多态。

## 类、对象以及引用

- 对象和类的概念

  - 对象是客观存在的实体，在Java语言体现为内存空间的一块区域。
  - 类就是分类的概念，是对具有相同特征和行为的多个对象共性的抽象描述，在Java语言中包含描述特征的成员变量和描述行为的成员方法，是创建对象的模板。

- 类的定义

  - 类定义的语法格式

  - class 类名{

    ​	类体；

    }

- 成员变量定义的语法格式

  - class 类名{

    ​	数据类型 成员变量 = 初始值；

    }

  - 注意类名要大写，当类名是多单词时，每个单词首字母大写；

  - 当成员变量名有多个单词组成时，要求从第二个单词起首字母大写。

  - 扩展:
    局部变量-主要指在方法体中声明的变量，作用范围从声明开始到方法体结束

    成员变量-主要指在方法体外类体内声明的变量，作用范围从声明到类体结束

- 对象的创建

  - 语法

    new 类名（）；

  - 注意事项

    a.当一个类定义完毕后，使用new关键字创建/构造对象的过程叫做 类的实例化;

    b.创建对象的本质就是在内存中的堆区申请存储空间，来存放该对象独有的特征信息

- 引用

  - 基本概念

    在Java语言中使用引用数据类型声明的变量叫做引用型变量，简称为"引用”引用变量主要用于记录对象在堆区中的内存地址信息，便于下次访问。

  - 语法格式

​		类名 引用变量名；

```java
public class Singer {
    String name;
    String gender;

    public static void main(String[] args) {
        //创建对象
        Singer chengChuShen = new Singer();
        Singer yiChunShan =new Singer();
        //打印对象
        System.out.println("我是"+chengChuShen.name+"我是一个"+chengChuShen.gender+"歌手");
        //属性赋值
        chengChuShen.name="陈楚生";
        chengChuShen.gender="男";
        //打印对象
        System.out.println("我是"+chengChuShen.name+"我是一个"+chengChuShen.gender+"歌手");
    }
}
```

## 成员方法

- 语法格式

  - ```java
    public class Singer {
        String name;
        String gender;
        
        public void singASong(){
            System.out.println("我正在唱一首歌");
        }
    }
    ```

- 格式详解

  - 返回值类型

    像上面的void就是返回类型，void说明没有返回值，不需要return。

    返回值类型主要指返回值的数据类型，可以是基本数据类型，也可以是引用数据类型。

    当返回的数据内容是66时，则返回值类型写int即可;

    当返回的数据内容是3.14时，则返回值类型写double即可;

    当返回的数据内容是"hello"时，则返回值类型写String即可;

  - 形参列表

    形式参数主要用于将方法体外的数据传入到方法体的内部，格式:数据类型形参；

  - 成员方法体

    成员方法体主要编写描述该方法功能的语句。

- 方法的调用

  - 语法格式

    引用变量名.成员方法名；

- 直接看代码

```java
public class Calculator {

    // 成员方法：add，用于计算两个整数的和
    public int add(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        // 创建Calculator类的实例
        Calculator calculator = new Calculator();

        // 调用add方法，并传递两个参数
        int result = calculator.add(5, 3);

        // 输出结果
        System.out.println("The sum is: " + result);
    }
}
```

## 构造方法及方法重载

- 构造方法

  - class 类名{

    ​	类名（形参列表）{

    ​		构造方法体；

    ​	}

    }

  - 注意事项

    - 就是一个方法名和类名完全相同的方法，没有返回值，void也不能给；
    - 它可以有参也可以无参。

  - 默认构造方法

    - 当一个类中没有自定义任何形式的构造方法时，编译器会自动添加一个无参的空构造方法，叫做默认/缺省构造方法；
    - 若类中出现自定义构造方法，则编译器不再提供任何形式的构造方法。

```java
public class Person {
    // 成员变量
    private String name;
    private int age;

    // 无参构造函数
    public Person() {
        this.name = "未知";
        this.age = 0;
    }

    // 有参构造函数
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // 获取成员变量的值
    public String getName() {
        return name;
    }

    public int getAge() {
        return age;
    }

    // 打印信息
    public void displayInfo() {
        System.out.println("姓名: " + name);
        System.out.println("年龄: " + age);
    }

    public static void main(String[] args) {
        // 调用无参构造函数
        Person person1 = new Person();
        System.out.println("无参构造函数初始化的对象:");
        person1.displayInfo(); // 输出默认值

        // 调用有参构造函数
        Person person2 = new Person("张三", 25);
        System.out.println("\n有参构造函数初始化的对象:");
        person2.displayInfo(); // 输出传入的参数值
    }
}
```

- 方法的重载

  - 概念
    - 在Java语言中若方法的名称相同但参数列表不同，这样的方法之间构成重载关系。

  - 形式
    - 参数的个数不同、参数的类型不同、参数的顺序不同，与形方法重载的主要形式有:但建议返回值类型最好相同。参变量名和返回值类型无关；
    - 判断方法是否重载的核心:调用能否区分。	

```java
public class demo1 {

    // 两个整数相加
    public int add(int a, int b) {
        return a + b;
    }

    // 三个整数相加
    public int add(int a, int b, int c) {
        return a + b + c;
    }

    // 两个双精度浮点数相加
    public double add(double a, double b) {
        return a + b;
    }

    // 两个字符串拼接
    public String add(String a, String b) {
        return a + b;
    }

    public static void main(String[] args) {
        demo1 demo = new demo1();

        System.out.println(demo.add(1, 2));
        System.out.println("三个整数相加: " + demo.add(5, 10, 20));         // 输出：35
        System.out.println("两个浮点数相加: " + demo.add(2.5, 3.5));       // 输出：6.0
        System.out.println("两个字符串拼接: " + demo.add("Hello", "World")); // 输出：HelloWorld
    }
}
```

## this关键字

- 基本概念
  - 在构造方法中，this关键字代表当前正在构造的对象；
  - 在成员方法中代表当前正在调用的对象。

```java
public class demo2 {
    // 成员变量
    private String name;
    private int age;

    // 无参构造
    public demo2() {
        this("未知", 0); // 调用有参构造函数
    }

    // 有参构造
    public demo2(String name, int age) {
        this.name = name; // this.name 表示当前对象的成员变量
        this.age = age;
    }

    // 设置名字的方法
    public void setName(String name) {
        this.name = name; // 区分参数 name 和成员变量 name
    }

    // 获取信息并打印
    public void displayInfo() {
        System.out.println("姓名: " + this.name); // 使用 this 明确访问成员变量
        System.out.println("年龄: " + this.age);
    }

    public static void main(String[] args) {
        demo2 d1 = new demo2(); // 调用无参构造
        System.out.println("默认初始化:");
        d1.displayInfo();

        demo2 d2 = new demo2("张三", 25); // 调用有参构造
        System.out.println("\n带参数初始化:");
        d2.displayInfo();
    }
}
```

- 使用方式

  - 当形参变量和成员变量同名时，在构造方法或成员方法中通常优先使用形参变量,若希望使用成员变量就需要在变量名的前面加上this.进行说明；

  - 在构造方法的第一行使用this(实参)的方式可以调用本类中的其它构造方法。

## 方法的传参和递归调用

- 方法的传参过程
  - main方法是程序的入口，为main方法中的局部变量开辟内存空间并初始化;
  - 调用max方法时为max方法的形参变量开辟内存空间;
  - 使用实参变量给形参变量进行赋值操作，执行max方法的方法体;
  - 当max方法结束后释放形参变量的内存空间；
  - 已main方法中的res得到max方法的返回值然后继续向下执行;
  - 当main方法结束后释放局部变量的内存空间;

- 递归调用
  - 在一个方法体中调用自己

## 封装

- 概念
  - 通常情况下测试类可以对封装类中的成员变量进行赋值，若赋值的数据合法但不合理时无论时编译阶段还是运行阶段都不会报错或者给出提示，此时与现实生活不符；
  - 为了避免上述错误的发生，就需要对成员变量进行密封包装处理，该机制就叫做封装换句话说，封装就是一种保证成员变量值合理性的机制。

- 实现
  - 将属性私有化，使用private修饰；
  - 提供更公共的get和set方法，在方法体中进行合理值的判断；
  - 在构造方法中调用set方法进行合理值的判断。

```java
public class Person {
    // 私有成员变量，对外不可见
    private String name;
    private int age;

    // 获取姓名
    public String getName() {
        return name;
    }

    // 设置姓名，加入空值判断
    public void setName(String name) {
        if (name == null || name.trim().isEmpty()) {
            throw new IllegalArgumentException("姓名不能为空");
        }
        this.name = name;
    }

    // 获取年龄
    public int getAge() {
        return age;
    }

    // 设置年龄，加入合法范围判断
    public void setAge(int age) {
        if (age < 0 || age > 150) {
            throw new IllegalArgumentException("年龄必须在 0 到 150 之间");
        }
        this.age = age;
    }

    // 显示信息
    public void displayInfo() {
        System.out.println("姓名: " + this.name);
        System.out.println("年龄: " + this.age);
    }

    public static void main(String[] args) {
        Person person = new Person();

        // 设置合法值
        person.setName("张三");
        person.setAge(25);
        person.displayInfo();

        // 尝试设置非法值，会抛出异常
        try {
            person.setAge(-5);
        } catch (IllegalArgumentException e) {
            System.out.println("捕获异常: " + e.getMessage());
        }
    }
}
```

## static关键字

- 通常情况下成员变量隶属于对象层级，每创建一个对象就需要申请独立的内存空间来存放该对象独立的成员变量信息，若所有对象的某个成员变量数值完全一样却又单独存放会造成内存空间的浪费。

- 为了解决上述问题，则使用static关键字修饰成员变量表达静态的含义，此时该成员梦量由对象层级提升为类层级被所有对象共享，该成员变量随着类的加载准备就绪，与是否创建对象无关。

- static关键字也可以修饰成员方法，推荐使用 类名. 的方式访问。

- 使用方式

  - 在非静态的成员方法中既能访问非静态的成员也能访问静态的成员;

    (成员:成员变量+成员方法，静态成员被所有对象共享)

  - 在静态的成员方法中只能访问静态的成员不能访问非静态的成员；

    (成员:成员变量+成员方法，调用静态方法时可能还没有创建对象)

  - 只有隶属于类层级被所有对象共享的内容才可以使用static修饰;

    (不能滥用static关键字)

- 单例设计模式

  - 基本概念
    - 在某些特殊场合中一个类对外提供且只提供一个对象，这样的类叫做单例类。
      而设计单例类的思想和模式叫做单例设计模式，主要用于固定的场合。

  - 实现流程
    - 私有化构造方法，使用private关键字修饰；
    - 声明本类类型的引用指向本类类型的对象，使用privatestatic共同修饰；
    - 提供公有的get方法负责将成员变量的数值返回出去，使用static关键字修饰;

  - 实现方法
    - 单例设计模式的实现方式有两种:饿汉式和懒汉式，在以后的开发中推荐饿汉式。

```java
public class SingletonInnerClass {
    private SingletonInnerClass() {}

    // 静态内部类，在外部类加载时不立即加载
    private static class SingletonHolder {
        private static final SingletonInnerClass INSTANCE = new SingletonInnerClass();
    }

    public static SingletonInnerClass getInstance() {
        return SingletonHolder.INSTANCE;
    }

    public void showMessage() {
        System.out.println("Hello from Singleton (Inner Class)");
    }

    public static void main(String[] args) {
        SingletonInnerClass s1 = SingletonInnerClass.getInstance();
        SingletonInnerClass s2 = SingletonInnerClass.getInstance();

        System.out.println(s1 == s2); // 输出 true，说明是同一个实例
        s1.showMessage();
    }
}
```

## 继承

- 基本概念
  - 当多个类之间有相同的特征和行为时，可以将相同的内容提取出来组成一个公共类让多个类吸收公共类中已有特征和行为而在多个类的内部编写自己独有特征和行为的方式，叫做继承。
  - 使用继承可以提高代码的复用性和扩展性以及可维护性。
  - 在Java语言中使用extends(扩展)关键字来表达继承关系。
  - public class Worker extends Person其中Person类叫做基类、父类、超类其中Worker类叫做派生类、子类、孩子类
    表示Worker类继承自Person类

- 注意事项
  - 子类可以继承父类的成员变量和成员方法，其中私有成员变量可以继承但不可以直接使用，子类不可以继承父类的构造方法和私有方法。
  - 无论使用何种方式构造子类对象时，都会自动调用父类中的无参构造方法来初始化从父类中继承下来的成员变量，相当于在子类构造方法第一行增加代码:super()的效果。
  - 使用继承必须满足 子类isa父类的逻辑关系，也就是不能滥用继承。
  - Java语言中只支持单继承不支持多继承，也就是一个子类只能有一个父类，但一个父类可以有多个子类。

- 方法的重写

  - 基本概念
    - 若从父类中继承下来的方法不满足子类的需求时，就需要在子类中重新写一个与父类中一样的方法来覆盖从父类中继承的版本，这种方式就叫做重写。

  - 原则
    - 要求方法名相同、参数列表相同、返回值类型相同，从jdk1.5开始允许返回子类类型。
    - 要求方法的访问权限不能变小，可以相同或者变大。
    - 要求不能抛出更大的异常(异常机制)。

## 访问控制

- 常用的访问控制符

  ![image-20250702153659394](C:\Users\Water3\AppData\Roaming\Typora\typora-user-images\image-20250702153659394.png)

  - public修饰的内容可以在任意位置使用；
  - private修饰的内容只能在本类中使用；
  - 通常情况下，成员变量都使用private修饰，成员方法都使用public修饰；

- 包的定义

  - package 包名
    package 包名1.包名2...包名n;-便于管理，避免命名冲突的问题

- final关键字

  - 基本概念
    - final本意为"最终的，不可更改的”，该关键字可以修饰类、成员方法、成员变量等。

  - 使用方式
    - final关键字修饰类表示该类不能被继承。
    - final关键字修饰成员方法表示该方法不能被重写但可以被继承。
    - final关键字修饰成员变量表示该成员变量必须初始化而且不能更改。

## 多态

- 基本概念

  - 多态主要指同一种事物表现出来的多种形态。

- 语法

  - 父类类型 引用变量名= new 子类类型()； 

- 效果

  - 当父类的引用指向子类的对象时，父类的引用可以直接调用父类独有的方法；
  - 当父类的引用指向子类的对象时，父类的引用不可以直接调用子类独有的方法；
  - 对于父子类都有的非静态成员方法来说，编译阶段调用父类版本，运行阶段调用子类重写以后的版本；
  - 对于父子类都有的静态方法来说，编译和运行阶段调用父类版本，隶属于类层级，因此与对象无关;

- 引用数据类型之间的转换

  - 引用数据类型之间的转换分为:自动类型转换和强制类型转换。

    其中自动类型转换主要指从小范围到大范围之间的转换，也就是子类到父类的转换

    其中强制类型转换主要指从大范围到小范围之间的转换，也就是父类到子类的转换

  - 引用数据类型之间的转换必须发生在父子类之间，否则编译报错。

- 多态的意义

  - 多态的实际意义在于可以屏蔽不同子类的差异性实现通用的编程，但可以调用不同的方法带来不同的结果。

```java
public class Animal {
    // 普通成员方法
    public void makeSound() {
        System.out.println("动物发出声音");
    }
}
public class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("汪汪汪...");
    }
}
public class Cat extends Animal {
    @Override
    public void makeSound() {
        System.out.println("喵喵喵...");
    }
}
public class Main {
    public static void main(String[] args) {
        // 父类引用指向子类对象 - 多态体现
        Animal animal1 = new Dog();
        Animal animal2 = new Cat();

        // 调用方法，根据对象实际类型执行重写后的方法
        animal1.makeSound(); // 输出：汪汪汪...
        animal2.makeSound(); // 输出：喵喵喵...

        // 可以扩展为方法参数传递，也体现多态
        callSound(new Dog());
        callSound(new Cat());
    }

    // 接收 Animal 类型，但可传入其子类对象
    public static void callSound(Animal animal) {
        animal.makeSound();
    }
}
```

## 抽象类

- 抽象方法的概念
  - 抽象方法就是指不能具体实现的方法，也就是没有方法体并使用abstract关键字修饰

- 抽象类的概念
  - 抽象类就是指不能具体实例化的类，也就是不能创建对象并使用abstract关键字修饰

- 注意事项
  - 抽象类中可以有成员变量、构造方法以及成员方法;
  - 抽象类中可以有抽象方法也可以没有抽象方法;
  - 拥有抽象方法的类必须是抽象类，因此严格来说，具有抽象方法并且使用abstract关键字修饰的类才算真正意义上的抽象类。

- 实际意义
  - 抽象类的意义不在于自身创建对象而在于被继承，当一个类继承抽象类后必须重写抽象类中的抽象方法，否则该类也变成抽象类。
  - 也就是说抽象类对子类具有强制性和规范性，因此叫做模板设计模式。

```java
public abstract class Animal {

    // 具体方法：有实现
    public void breathe() {
        System.out.println("动物在呼吸");
    }

    // 抽象方法：只有声明，没有实现
    public abstract void makeSound();
}
public class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("汪汪汪...");
    }
}
// Cat 类继承 Animal 并实现 makeSound 方法
public class Cat extends Animal {
    @Override
    public void makeSound() {
        System.out.println("喵喵喵...");
    }
}
public class Main {
    public static void main(String[] args) {
        // 不能 new Animal()，因为它是抽象类
        // Animal animal = new Animal(); // 编译错误！

        // 向上转型，多态使用
        Animal dog = new Dog();
        Animal cat = new Cat();

        dog.breathe();      // 调用具体方法
        dog.makeSound();    // 调用重写的抽象方法

        cat.breathe();
        cat.makeSound();
    }
}
```

## 接口

- 基本概念
  - 接口就是一种比抽象类还抽象的类，体现为所有成员方法都是抽象方法。
  - 定义类的关键字是class，而定义接口的关键字是interface。
  - 继承类的关键字是extends，而实现接口的关键字是implements。

- 类和接口之间的关系
  - 类和类之间的关系	使用extends关键字表达继承的关系	支持单继承
  - 类和接口之间的关系	使用implemets关键字表达实现的关系  支持多实现
  - 接口和接口之间的关系	使用extends关键字表达继承的关系	支持多继承

- 抽象类和接口之间的区别
  - 定义抽象类的关键字是abstract class，而定义接口的关键字是interface。
    继承抽象类的关键字是extends，而实现接口的关键字是implements。
    继承抽象类支持单继承，而实现接口可以多实现。
    抽象类中可以有构造方法，而接口中不可以有构造方法。
    抽象类中可以有成员变量，而接口中只可以有常量。
    抽象类中可以有成员方法，而接口中只可以有抽象方法。
    抽象类中增加方法可以不影响子类，而接口中增加方法通常都影响子类。
    从jdk1.8开始允许接口中出现非抽象方法，但需要使用default关键字修饰。

## 匿名内部类

- 语法

  - class 外部类名{

    ​	class 内部类名{

    ​		内部类的类体；

    ​	}

    }

- 实际作用

  - 当一个类存在的价值仅仅是为某一个类单独服务时，那么就可以将这个类定义为所服务类中的内部类，这样可以隐藏该类的实现细节并且可以方便的访问外部类的私有成员而不再需要提供公有的get和set方法。

- 分类

  - 普通内部类	直接将一个类的定义放在另外一个类的类体中。
  - 静态内部类	使用static关键字修饰的内部类，隶属于类层级。

## Object类

- 常用的包
  - java.lang包-该包是Java语言中的核心包，该包中的内容由Java虚拟机自动导入
    如：String类、System类等
  - java.util包-该包是Java语言中的工具包，里面包含了大量的工具类和集合类等
    如：Scanner类、Random类等
  - java. io包
    -该包是Java语言中的输入输出包，里面包含了大量读写文件的类等
    如:FileOutputStream类、FileInputStream类等
  - java.net包一该包是Java语言中的网络包，里面包含了大量网络编程的类等
    如：ServerSocket类、Socket类等

- 常见的方法
  - Object(-使用无参方式构造对象。
    boolean equals(Objectobj) 一 用于判断调用对象是否与参数对象相等。
    该方法默认比较两个对象的地址，与 == 运算符结果相同。

```java
class Person {
    private String name;

    public Person(String name) {
        this.name = name;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (!(obj instanceof Person)) return false;

        Person other = (Person) obj;
        return name != null ? name.equals(other.name) : other.name == null;
    }

    public static void main(String[] args) {
        Person p1 = new Person("Alice");
        Person p2 = new Person("Alice");

        System.out.println(p1.equals(p2)); // true
    }
}
```

## 包装类和教学处理类

- Personp=newPersonO；	-声明Person类型的引用指向Person类型的对象
  int num = 10;			   －声明一个int类型的变量num初始值为10

  Java语言是一门纯面向对象的编程语言

- 包装类的概念

  - 由于Java语言是一门纯面向对象编程语言，而8种基本数据类型声明的变量并不是对象为了满足Java语言的特性就需要对这些变量进行对象化处理，而实现该功能的相关类就叫做包装类。

- 包装类的分类

  - int => java. lang. Integer类
    char => java. lang. Character类
    其它类型对应的包装类就是将首字母变成大写

- Integer类

  - 基本概念
    - java.lang.Integer类是int类型的包装类，里面包含了一个int类型的成员变量。
      该类由final关键字修饰表示不能被继承。

  - 常用方法
    - Integer(intvalue)-根据参数指定的整数构造对象
      Integer(Strings)-根据参数指定的字符串构造对象
      该类重写了equalsO、hashCodeO、toStringO方法
      intintValue() - 用于获取调用对象中的整数数据并返回。
      static Integer valueOf(int i) - 根据参数指定的整数返回对应的Integer对象。
      static int parseInt(String s) - 用于将String类型转换为int类型并返回。

- BigDecimal类

  - 基础概念
    - 由于float类型和double类型的运算可能会有误差，为了实现精确运算则需要借助
      java.math.BigDecimal类型加以描述。

  - 常用方法
    - BigDecimal(Stringval)根据参数指定的字符串构造对象。
      BigDecimal add (BigDecimal augend)
      一用于计算调用对象和参数对象的和并返回
      BigDecimal subtract (BigDecimal subtrahend)
      一用于计算调用对象和参数对象的差并返回。
      BigDecimal multiply(BigDecimal multiplicand)
      一用于计算调用对象和参数对象的积并返回。
      BigDecimal divide (BigDecimal divisor)
      一用于计算调用对象和参数对象的商并返回。

## String类

- 基本概念

  - java.lang.String类用于描述字符串，Java应用程序中所有字符串字面值都可以作为
    String类型的对象加以描述，如：”abc”等。
    该类描述的字符串内容是个常量，一旦创建完毕后则不能更改，因此可以被共享。
    如：
    String strl = "abc”;
    str1=”123”；-改变str1的指向而不是指向的内容

- 常量池

  ```java
  import java.util.HashMap;
  import java.util.Map;
  
  public class StringPool {
      // 模拟String常量池
      private static final Map<String, String> pool = new HashMap<>();
  
      // 获取或创建String对象
      public static String intern(String str) {
          if (str == null) {
              return null;
          }
  
          // 如果字符串已经在池中，返回已存在的引用
          if (pool.containsKey(str)) {
              return pool.get(str);
          }
  
          // 否则将字符串加入池中，并返回其引用
          pool.put(str, str);
          return str;
      }
  
      public static void main(String[] args) {
          // 测试代码
          String str1 = StringPool.intern("Hello");
          String str2 = StringPool.intern("Hello");
  
          System.out.println(str1 == str2);  // 输出 true，表示两个引用指向同一个对象
      }
  }
  ```

- String类的操作

  ```java
  public class SimpleString {
      private final char[] value;
  
      // 构造函数
      public SimpleString(char[] value) {
          this.value = value;
      }
  
      // 返回字符串长度
      public int length() {
          return value.length;
      }
  
      // 获取指定索引处的字符
      public char charAt(int index) {
          if (index < 0 || index >= value.length) {
              throw new IndexOutOfBoundsException("Index out of bounds");
          }
          return value[index];
      }
  
      // 截取子字符串
      public SimpleString substring(int beginIndex, int endIndex) {
          if (beginIndex < 0 || endIndex > value.length || beginIndex > endIndex) {
              throw new IndexOutOfBoundsException("Invalid indices");
          }
          char[] subValue = new char[endIndex - beginIndex];
          System.arraycopy(value, beginIndex, subValue, 0, subValue.length);
          return new SimpleString(subValue);
      }
  
      // 判断两个SimpleString对象是否相等
      @Override
      public boolean equals(Object obj) {
          if (this == obj) return true;
          if (!(obj instanceof SimpleString)) return false;
  
          SimpleString other = (SimpleString) obj;
          if (value.length != other.value.length) return false;
  
          for (int i = 0; i < value.length; i++) {
              if (value[i] != other.value[i]) return false;
          }
  
          return true;
      }
  
      // 查找子字符串首次出现的位置
      public int indexOf(SimpleString str) {
          for (int i = 0; i <= value.length - str.length(); i++) {
              boolean match = true;
              for (int j = 0; j < str.length(); j++) {
                  if (value[i + j] != str.charAt(j)) {
                      match = false;
                      break;
                  }
              }
              if (match) return i;
          }
          return -1;
      }
  
      // 拼接字符串
      public SimpleString concat(SimpleString str) {
          char[] newValue = new char[value.length + str.length()];
          System.arraycopy(value, 0, newValue, 0, value.length);
          for (int i = 0; i < str.length(); i++) {
              newValue[value.length + i] = str.charAt(i);
          }
          return new SimpleString(newValue);
      }
  
      // 转换为Java内置String类型（便于输出）
      @Override
      public String toString() {
          return new String(value);
      }
  
      // 测试代码
      public static void main(String[] args) {
          SimpleString str1 = new SimpleString("Hello".toCharArray());
          SimpleString str2 = new SimpleString("World".toCharArray());
  
          System.out.println("Length: " + str1.length()); // 输出 5
          System.out.println("Char at index 1: " + str1.charAt(1)); // 输出 'e'
          SimpleString substr = str1.substring(0, 3);
          System.out.println("Substring: " + substr); // 输出 'Hel'
  
          SimpleString str3 = new SimpleString("Hello".toCharArray());
          System.out.println("Equals: " + str1.equals(str3)); // 输出 true
  
          System.out.println("IndexOf: " + str1.indexOf(str2)); // 输出 -1 (不匹配)
          SimpleString concatStr = str1.concat(str2);
          System.out.println("Concat: " + concatStr); // 输出 'HelloWorld'
      }
  }
  ```

- StringBuilder类和StringBuffer类

  - 基本概念
    - 由于String类型描述的字符串内容是个常量不可更改，当程序中出现大量类似的字符串时需要单独存放从而浪费内存空间，若希望使用一块内存空间进行存储并且可以修改字符串内容，则应该使用StringBuilder类和StringBuffer类。
      其中StringBuffer类从jdk1.0开始存在，该类支持线程安全，因此访问的效率比较低
      其中StringBuilder类从jdk1.5开始存在，该类不支持线程安全，访问的效率比较高

```java
public class SimpleString {
    public static void main(String[] args) {
        long startTime;

        // String 拼接
        startTime = System.nanoTime();
        String str = "";
        for (int i = 0; i < 10000; i++) {
            str += "test";
        }
        System.out.println("String 拼接耗时: " + (System.nanoTime() - startTime) / 1_000_000 + "ms");

        // StringBuilder
        startTime = System.nanoTime();
        StringBuilder sb = new StringBuilder(10000 * 4); // 避免多次扩容
        for (int i = 0; i < 10000; i++) {
            sb.append("test");
        }
        System.out.println("StringBuilder 耗时: " + (System.nanoTime() - startTime) / 1_000_000 + "ms");

        // StringBuffer
        startTime = System.nanoTime();
        StringBuffer sbf = new StringBuffer(10000 * 4);
        for (int i = 0; i < 10000; i++) {
            sbf.append("test");
        }
        System.out.println("StringBuffer 耗时: " + (System.nanoTime() - startTime) / 1_000_000 + "ms");
    }
}
```

- 日期相关的类

  - Date类
    - 基本概念
      - java.util.Date类用于描述特定的瞬间，可以精确到毫秒。

  - SimpleDateFormat类
    - 基本概念
      - java.text. SimpleDateFormat类主要用于实现日期和文本之间的相关转换。

## 集合

- 集合框架
  - 在Java语言中集合框架的顶层是：java.util.Collection集合和java.util.Map集合
    其中Collection集合中操作元素的基本单位是：单个元素。
    其中Map集合中操作元素的基本单位是：单对元素。

- 集合由来
  - 当需要在程序中记录单个数据内容时，则声明一个变量即可；
    当需要在程序中记录多个类型相同的数据内容时，则声明一个一维数组即可；
    当需要在程序中记录多个类型不同的数据内容时，则构造一个对象即可；
    当需要在程序中记录多个类型相同的对象时，则声明一个对象数组即可；
    当需要在程序中记录多个类型不同的对象时，则声明一个集合即可；

## Collection集合

- 基本概念
  - java.utl.Collection集合是集合框架的根接口，其它接口是该接口的子接口。

## List集合

- 基本概念
  - java.util.List集合是Collection集合的子集合，该集合中元素有先后次序且允许重复
    该集合的主要实现类有：ArrayList类、LinkedList类、Stack类、Vector类等
    其中ArrayList类的底层是采用动态数组进行数据管理，访问方便，增删不方便。
    其中LinkedList类的底层是采用链表进行数据管理，增删方便，访问不方便。

```java
import java.util.ArrayList;
import java.util.List;

public class ListCRUDDemo {
    public static void main(String[] args) {
        // 创建一个 List 集合
        List<String> list = new ArrayList<>();

        // 1️⃣ Create - 添加元素
        System.out.println("=== 1. 添加元素 ===");
        list.add("Apple");     // 添加到末尾
        list.add("Banana");
        list.add(2, "Cherry"); // 插入到指定位置
        System.out.println("添加后: " + list);

        // 2️⃣ Read - 读取元素
        System.out.println("\n=== 2. 读取元素 ===");
        System.out.println("第一个元素: " + list.get(0)); // Apple
        System.out.println("是否包含 Banana: " + list.contains("Banana"));

        // 3️⃣ Update - 更新元素
        System.out.println("\n=== 3. 更新元素 ===");
        list.set(1, "Blueberry"); // 将索引为1的元素替换为 Blueberry
        System.out.println("更新后: " + list);

        // 4️⃣ Delete - 删除元素
        System.out.println("\n=== 4. 删除元素 ===");
        list.remove("Cherry"); // 根据对象删除
        list.remove(0);        // 根据索引删除
        System.out.println("删除后: " + list);

        // 清空集合
        list.clear();
        System.out.println("清空后: " + list);
    }
}
```

## 泛型

- 基本概念
  - 通常情况下集合中可以存放不同类型的对象，本质上是将这些对象全部看做Object类型放入的，因此从集合中取出元素时也是Object类型，为了表达元素最真实的数据类型就需要强制类型转换，而强制类型转换可能发生类型转换异常。
  - 为了避免上述错误的发生，从jdk1.5开始提出泛型机制，也就是在集合名称的右侧使
    用<数据类型>的方式明确要求该集合可以存放的元素类型，若放入其它类型则编译报错
    如：
    List lt1 = new LinkedList()；-  可以放入任意类型对象，取出麻烦
    List<String>lt1=new LinkedList<String>O; - 只能放入String类型,取出方便
- 原理
  - 泛型的本质就是参数化类型，也就是让数据类型作为参数传递，集合定义中的E相当于形式参数负责占位，而使用集合时<>中的数据类型相当于实际参数负责给形式参数初始化，当初始化完毕后所有E被替换为实际参数表示的类型进行使用。

## Queue集合

- 基本概念
  - java.utli.Queue集合是Collection集合的子集合，与List集合是平级关系。
  - 该集合的主要实现类是：LinkedList类，因为该类在增删方面有一定的优势。
  - 该集合用于描述具有先进先出特征的数据结构，叫做队列（first in first out）。

```java
public static void main(String[] args) {
    // 创建一个队列
    Queue<String> queue = new LinkedList<>();

    //  1入队 (Enqueue)
    System.out.println("=== 1. 入队操作 ===");
    queue.offer("Apple");     // 添加到队尾
    queue.offer("Banana");
    queue.offer("Cherry");
    System.out.println("入队后: " + queue);

    // 2出队 (Dequeue)
    System.out.println("\n=== 2. 出队操作 ===");
    String removedElement = queue.poll(); // 移除并返回队首元素
    System.out.println("出队元素: " + removedElement);
    System.out.println("出队后: " + queue);

    // 3查看队首元素 (Peek)
    System.out.println("\n=== 3. 查看队首元素 ===");
    String frontElement = queue.peek(); // 查看但不移除队首元素
    System.out.println("当前队首元素: " + frontElement);
    System.out.println("队列状态: " + queue);

    // 4️ 判断队列是否为空
    System.out.println("\n=== 4. 判断队列是否为空 ===");
    boolean isEmpty = queue.isEmpty();
    System.out.println("队列是否为空: " + isEmpty);

    // 5️ 清空队列
    queue.clear();
    System.out.println("清空后: " + queue);
}
```

## Set集合

- 基本概念

  - java.util.Set集合是Collection集合的子集合，与List集合以及Queue集合平级关系
  - 该集合与List集合的主要区别在于：元素没有先后次序并且不允许重复的元素。
  - 该集合的主要实现类有：HashSet类和TreeSet类。
  - 其中HashSet类的底层采用哈希表进行数据管理的。
  - 其中TreeSet类的底层采用二叉树进行数据管理的。

- 常见的方法

  ```java
  public static void main(String[] args) {
      // 创建一个 Set 集合
      Set<String> set = new HashSet<>();
  
      // 1️⃣ Create - 添加元素
      System.out.println("=== 1. 添加元素 ===");
      set.add("Apple");
      set.add("Banana");
      set.add("Cherry");
      set.add("Apple"); // 重复元素不会被添加
      System.out.println("添加后: " + set);
  
      // 2️⃣ Read - 读取元素（Set 不支持通过索引读取）
      System.out.println("\n=== 2. 读取元素 ===");
      System.out.println("是否包含 Banana: " + set.contains("Banana"));
  
      // 3️⃣ Update - 更新元素（Set 本身没有直接更新方法，需先删除再添加）
      System.out.println("\n=== 3. 更新元素 ===");
      set.remove("Banana");
      set.add("Blueberry"); // 模拟更新 Banana -> Blueberry
      System.out.println("更新后: " + set);
  
      // 4️⃣ Delete - 删除元素
      System.out.println("\n=== 4. 删除元素 ===");
      set.remove("Cherry");
      System.out.println("删除后: " + set);
  
      // 清空集合
      set.clear();
      System.out.println("清空后: " + set);
  }
  ```

## Map集合

- 基本概念
  - java.util.Map<K，V>集合中操作元素的基本单位是：单对元素，其中类型参数如下：
  - K-此映射所维护的键(key)的类型
  - V-映射值(value)的类型
  - 该集合中不允许出现重复的键，每个键最多只能映射到一个值。
  - 该集合的主要实现类有：HashMap类和TreeMap类。
  - 其中HashMap类的底层是采用哈希表进行数据管理的。

```java
public static void main(String[] args) {
    // 创建一个 Map 集合（键值对形式）
    Map<String, Integer> map = new HashMap<>();

    // 1️⃣ Create - 添加元素
    System.out.println("=== 1. 添加元素 ===");
    map.put("Apple", 10);
    map.put("Banana", 20);
    map.put("Cherry", 30);
    System.out.println("添加后: " + map);

    // 2️⃣ Read - 读取元素
    System.out.println("\n=== 2. 读取元素 ===");
    System.out.println("获取 Apple 的值: " + map.get("Apple")); // 获取指定 key 的 value
    System.out.println("是否包含 key 'Banana': " + map.containsKey("Banana"));

    // 3️⃣ Update - 更新元素
    System.out.println("\n=== 3. 更新元素 ===");
    map.put("Banana", 25); // 更新已有的键值对
    System.out.println("更新后 Banana: " + map.get("Banana"));
    System.out.println("当前 Map: " + map);

    // 4️⃣ Delete - 删除元素
    System.out.println("\n=== 4. 删除元素 ===");
    map.remove("Cherry"); // 根据 key 删除键值对
    System.out.println("删除 Cherry 后: " + map);

    // 清空集合
    map.clear();
    System.out.println("清空后: " + map);
}
```

## 异常机制

- 基本概念 

  - 异常就是”不正常”的含义，在Java语言中用于表示运行阶段发生的错误。
  - java.lang.Throwable类是Java语言中所有错误(Error)和异常(Exception)的超类。
  - 其中Error类主要用于描述比较严重无法编码解决的问题，如：JVM挂了。
  - 其中Exception类主要用于描述比较轻微可以编码解决的问题，如：0作为除数。

- 基本分类

  - java.lang.Exception类是所有异常类的超类，主要分为以下两大类：

  - RuntimeException一运行时异常，也叫作非检测性异常

  - IOException和其它异常一其它异常，也叫作检测性异常

    ​	——所谓检测性异常就是在编译阶段能够被编译器检测出来的异常

  - 其中RuntimeException类的主要子类：
    ArithmeticException-算术异常
    ArrayIndexOutOfBoundsException一数组下标越界异常
    NullPointerException-空指针异常
    ClassCastException-类型转换异常
    NumberFormatException-数字格式异常

- 异常的避免

  - 在开发中尽量使用if条件判断来避免异常的发生。

- 异常的捕获

  - 语法

    try{
    编写可能发生异常的语句；

    }catch(异常类型变量名）{
    编写针对该类异常的处理语句；
    finally{
    编写无论是否发生异常都应该执行的语句；

​		}

## I/O流

- FileOutputStream类

  - 基本概念
    - java.io.FileOutputStream类主要用于将图像数据之类的原始字节流写入输出流中。

  - 常用方法

```java
public static void main(String[] args) {
    // 定义要写入文件的内容（字节数组）
    String data = "Hello, this is a demo of FileOutputStream!";
    byte[] byteArray = data.getBytes();  // 将字符串转换为字节

    // 使用 try-with-resources 自动关闭资源
    try (FileOutputStream fos = new FileOutputStream("output.txt")) {
        fos.write(byteArray);  // 写入字节到文件
        System.out.println("Data written successfully to the file.");
    } catch (IOException e) {
        e.printStackTrace();  // 捕获并处理 IO 异常
    }
}
```

- FileInputStream类

  - 基本概念
    - java.io.FileInputStream类主要用于从输入流中读取图像数据之类的原始字节流。

  - 常用

```java
public static void main(String[] args) {
    // 使用 try-with-resources 自动关闭资源
    try (FileInputStream fis = new FileInputStream("output.txt")) {
        int content;
        // 逐个字节读取文件内容
        while ((content = fis.read()) != -1) {
            System.out.print((char) content);  // 将字节转换为字符并输出
        }
    } catch (IOException e) {
        e.printStackTrace();  // 捕获并处理 IO 异常
    }
}
```

- 文件拷贝

```java
public static void main(String[] args) {
    String sourceFilePath = "output.txt";          // 源文件路径
    String destinationFilePath = "output_copy.txt"; // 目标文件路径

    // 设置缓冲区大小，通常为 1024 字节（1KB）或其倍数
    byte[] buffer = new byte[1024];

    try (FileInputStream fis = new FileInputStream(sourceFilePath);
         FileOutputStream fos = new FileOutputStream(destinationFilePath)) {

        int bytesRead;
        // 每次读取一个缓冲区内容
        while ((bytesRead = fis.read(buffer)) != -1) {
            // 将缓冲区中实际读取到的数据写入输出流
            fos.write(buffer, 0, bytesRead);
        }

        System.out.println("使用缓冲区的文件拷贝完成！");
    } catch (IOException e) {
        e.printStackTrace();
    }
}
```

- BufferedWriter类

  - 基本概念
    - java.io.BufferedWriter类主要中写入单个字符、字符数组以及字符串

  - 常用

```java
public static void main(String[] args) {
    // 定义要写入的文件路径
    String filePath = "buffered_output.txt";

    // 使用 try-with-resources 自动关闭资源
    try (BufferedWriter writer = new BufferedWriter(new FileWriter(filePath))) {
        // 写入多行字符串
        writer.write("欢迎使用 BufferedWriter 写入文本！");
        writer.newLine(); // 换行
        writer.write("这是第二行文本。");
        writer.newLine();
        writer.write("你可以高效地写入大量文本内容。");

        System.out.println("文本内容已成功写入文件！");
    } catch (IOException e) {
        e.printStackTrace();
    }
}
```

- BufferedReader类

  - 基本概念
    - java.io.BufferedReader类主要用于从输入流中读取单个字符、字符数组以及一行字符串内容。

  - 用法

```java
public static void main(String[] args) {
    // 定义要读取的文件路径
    String filePath = "buffered_output.txt";

    // 使用 try-with-resources 自动关闭资源
    try (BufferedReader reader = new BufferedReader(new FileReader(filePath))) {
        String line;
        // 逐行读取文件内容
        while ((line = reader.readLine()) != null) {
            System.out.println(line);  // 打印每一行内容
        }
    } catch (IOException e) {
        e.printStackTrace();
    }
}
```

- PrintStream类

  - 基本概念
    - java.io.PrintStream类主要用于方便地打印各种数据内容并且自动刷新。

  - 常用

```java
public static void main(String[] args) {
    // 定义输出文件路径
    String filePath = "printstream_output.txt";

    // 使用 try-with-resources 自动关闭资源
    try (PrintStream ps = new PrintStream(filePath)) {
        // 输出字符串
        ps.println("这是通过 PrintStream 写入的第一行文本。");

        // 格式化输出
        ps.printf("这是一个整数：%d，一个浮点数：%.2f%n", 100, 3.1415);

        // 输出布尔值
        ps.print(true);
        ps.println(" 这是紧接着的一段文字。");

        System.out.println("数据已成功写入到文件：" + filePath);
    } catch (FileNotFoundException e) {
        e.printStackTrace();
    }
}
```

- ObjectOutputStream类
  - 基本概念
    - java.io.ObjectOutputStream类主要用于将Java语言中的对象整体写入输出流中。
      只能将支持java.io. Serializable接口的对象写入流中。
      类通过实现java.io.Serializable接口以启用其序列化功能。
      所谓序列化就是指将一个对象相关的所有信息有效组织成字节序列的转化过程。

- ObjectInputStream类
  - 基本概念
    - java.io.ObjectInputStream类主要用于从输入流中一次性将一个对象的内容读取出来实现了从字节序列到对象的转化过程，叫做反序列化。

```java
public class Person implements Serializable {
    private static final long serialVersionUID = 1L;

    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return "Person{name='" + name + "', age=" + age + "}";
    }

    public static void main(String[] args) {
        String filePath = "person.ser";

        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(filePath))) {
            // 创建一个对象
            Person person = new Person("Alice", 25);

            // 序列化对象写入文件
            oos.writeObject(person);

            System.out.println("对象已写入文件：" + filePath);
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

## 线程

- 基本概念

  - 程序主要指存放在硬盘上的可执行文件。
  - 运行在内存中的程序称之为进程。

  - 目前主流的操作系统都支持多进程，为了使得操作系统能够同时执行多个任务，但进程是重量级的，新建进程对系统的资源消耗比较大，因此进程的数量比较局限。

  - 线程是进程内部的程序流，也就是操作系统中支持多进程，而每个进程的内部又可以支持多线程，线程是轻量级的，新建线程会共享所在进程的系统资源，因此以后的开发中都采用多线程技术。

  - 多线程技术采用时间片轮转法实现并发执行，所谓并发就是指宏观并行微观串行。

- 线程的创建

  - 创建和启动方法
    - java.lang.Thread类用于描述线程，Java虚拟机允许应用程序并发地运行多个执行线程，而线程的创建和启动方如下：
    - 自定义类继承Thread类并重写run方法，创建该类的实例调用start方法。
    - 自定义类实现Runnable接口并重写run方法，创建该类的实例作为实参来构造Thread类型的对象，然后使用Thread类型的对象调用start方法。

  - 相关方法的解析

    - Thread-使用无参方式构造对象。

    - Thread(Stringname)-根据参数指定的名称来构造对象。

    - Thread(Runnabletarget)-根据参数指定的接口引用来构造对象。

    - Thread(Runnable target, String name)

    - 根据参数指定的引用和名称构造对象。

      

    - voidrun()   -   若使用Runnable类型的引用构造出来的对象调用该方法，则最终调用引用所指向对象的run方法，否则调用该方法啥也不做。

    - voidstart()   -   用于启动线程，Java虚拟机会自动调用该线程的run方法。

```java
class MyThread extends Thread {
    // 重写 run 方法
    @Override
    public void run() {
        for (int i = 0; i < 5; i++) {
            System.out.println("线程运行: " + i);
            try {
                Thread.sleep(500); // 模拟耗时操作
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
    public static void main(String[] args) {
        // 创建线程实例
        MyThread myThread = new MyThread();

        // 调用 start 方法启动线程
        myThread.start();
    }
}
```

- 原理分析
  - a.执行main方法的线程叫做主线程，执行run方法的线程叫做子线程。
  - b.main方法是程序的入口，最开始只有主线程来依次执行main方法中的代码，当start方法调用成功后，线程的个数瞬间由1个变成了2个，其中子线程去执行run方法，主线程继续执行main方法的代码，两个线程各自独立运行互不影响。
  - c.当run方法执行完毕后子线程结束，当main方法执行完毕后主线程结束，但两个线程谁先执行没有明确的规定，取决于操作系统的调度算法。

```java
class MyRunnable implements Runnable {
    @Override
    public void run() {
        for (int i = 0; i < 5; i++) {
            System.out.println("当前线程运行: " + i);
            try {
                Thread.sleep(500); // 模拟耗时操作
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }

    public static void main(String[] args) {
        // 创建 Runnable 实例
        MyRunnable myRunnable = new MyRunnable();

        // 创建多个线程并启动
        Thread thread1 = new Thread(myRunnable, "线程A");
        Thread thread2 = new Thread(myRunnable, "线程B");

        thread1.start();
        thread2.start();
    }
}
```

- 线程创建两种方法
  - 创建一个具体线程，需要继承于Thread类。
    覆盖run方法(就是更新运行过程)，实现用户指定任务的过程。
    创建线程实例（一个线程)。
    使用线程实例调思start方法启动线程，该线程会尽快的去并发执行run方法。
  - 创建一个类实现Runnable接口并重写run方法。
    创建实现Runnable接口类的实例对象作为参数创建Thread对象。
    使用Thread类对象调start方法启动线程，该线程会尽快并发执行run方法
- 匿名类的方法

```java
public class AnonymousThreadDemo {
    public static void main(String[] args) {
        // 使用匿名内部类方式创建线程1
        Thread thread1 = new Thread(new Runnable() {
            @Override
            public void run() {
                for (int i = 0; i < 5; i++) {
                    System.out.println("线程1: " + i);
                    try {
                        Thread.sleep(500); // 模拟耗时操作
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }, "线程A");

        // 使用匿名内部类方式创建线程2
        Thread thread2 = new Thread(new Runnable() {
            @Override
            public void run() {
                for (int i = 0; i < 5; i++) {
                    System.out.println("线程2: " + i);
                    try {
                        Thread.sleep(500); // 模拟耗时操作
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }, "线程B");

        // 启动线程
        thread1.start();
        thread2.start();
    }
}
```

- 线程的编号和名称

```java
public class AnonymousThreadDemo {
    public static void main(String[] args) {
        // 使用匿名内部类方式创建线程1
        Thread thread1 = new Thread(new Runnable() {
            @Override
            public void run() {
                long id = Thread.currentThread().getId();     // 获取当前线程编号
                String name = Thread.currentThread().getName(); // 获取当前线程名称
                for (int i = 0; i < 5; i++) {
                    System.out.println("线程名称: " + name + ", 编号: " + id + ", 执行i=" + i);
                    try {
                        Thread.sleep(500); // 模拟耗时操作
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }, "线程A");

        // 使用匿名内部类方式创建线程2
        Thread thread2 = new Thread(new Runnable() {
            @Override
            public void run() {
                long id = Thread.currentThread().getId();     // 获取当前线程编号
                String name = Thread.currentThread().getName(); // 获取当前线程名称
                for (int i = 0; i < 5; i++) {
                    System.out.println("线程名称: " + name + ", 编号: " + id + ", 执行i=" + i);
                    try {
                        Thread.sleep(500); // 模拟耗时操作
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }, "线程B");

        // 启动线程
        thread1.start();
        thread2.start();
    }
}
```

- 线程优先级与等待

```java
public class AnonymousThreadDemo {
    public static void main(String[] args) {
        // 使用匿名内部类方式创建线程1
        Thread thread1 = new Thread(new Runnable() {
            @Override
            public void run() {
                long id = Thread.currentThread().getId();
                String name = Thread.currentThread().getName();
                for (int i = 0; i < 5; i++) {
                    System.out.println("线程名称: " + name + ", 编号: " + id + ", 执行i=" + i);
                    try {
                        Thread.sleep(500); // 模拟耗时操作
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }, "线程A");

        // 使用匿名内部类方式创建线程2
        Thread thread2 = new Thread(new Runnable() {
            @Override
            public void run() {
                long id = Thread.currentThread().getId();
                String name = Thread.currentThread().getName();
                for (int i = 0; i < 5; i++) {
                    System.out.println("线程名称: " + name + ", 编号: " + id + ", 执行i=" + i);
                    try {
                        Thread.sleep(500); // 模拟耗时操作
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
                }
            }
        }, "线程B");

        // 设置线程优先级：线程A优先级更高
        thread1.setPriority(Thread.MAX_PRIORITY); // 设置为最高优先级
        thread2.setPriority(Thread.MIN_PRIORITY); // 设置为最低优先级

        // 启动线程
        thread1.start();
        thread2.start();

        // 主线程等待 thread1 和 thread2 执行完成
        try {
            System.out.println("主线程开始等待...");
            thread1.join(); // 等待线程A结束
            thread2.join(); // 等待线程B结束
            System.out.println("所有线程执行完毕，主线程继续执行");
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
}
```