# Java编程基础与程序设计

[toc]

## 1 Java程序开发入门

### 1.1 计算机的基本概念

- 计算机俗称电脑，主要有**软件**和**硬件**两部分组成
- 硬件是客观存在的各种设备，如CPU、硬盘、显卡等，软件是用于控制各种硬件设备完成各种功能

### 1.2 常见硬件的介绍

- CPU（中央处理器）的概念和作用
  - 是计算机的核心部件，负责执行指令、处理数据以及协调其他硬件的工作。
  - 它是计算机的“大脑”，决定了设备的计算性能。

- 内存的概念和作用
  - 是计算机存储数据的地方，用于临时CPU访问的数据。
  - CPU直接访问且效率高
  - 容量小，一但断电会造成数据的丢失

- 硬盘（Hard Disk Drive，HDD）的概念和作用
  - 是计算机存储数据的重要设备。
  - CPU无法直接访问，效率低
  - 容量大，但断电不会丢失数据

### 1.3 计算机的体系结构

- 计算机的体系结构是计算机系统的核心框架，它定义了计算机硬件、软件、数据和网络等各个组成部分之间的相互关系、功能和性能，如下图所示：

  ![image-20250628155811838](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628155811838.png)

  

  

### 1.4 java语言的发展史

- 如下图所示：

![image-20250628161811376](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628161811376.png)



### 1.5 编写第一个java程序的流程

1. 新建文本文档，将文件名有xxx.txt修改为xxx.java；
2. 编写Java代码保存
3. 启动dos窗口，切换到文件所在路径
4. 使用javac xxx.java 进行编译，生成xxx.class的字节码文件；
5. 使用java xxx 进行解释执行，打印最终结果

### 1.6 开发java程序常用的快捷键

```diff
ctrl+c 复制		ctrl+v 粘贴		ctrl+z 撤销		ctrl+s 保存

ctrl+x 剪切		ctrl+f 查找		ctrl+a 全选 
```

### 1.7 环境变量的配置

- 环境变量的基本概念

  通常情况下可执行文件只能在该文件所在路径中访问，若希望该文件可以在全路径下访问，则需要将该文件配置在环境变量Path中

- 右键此电脑选择属性

  ![image-20250628162105721](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628162105721.png)

- 进入系统页面，点击高级系统设置

  ![image-20250628162146830](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628162146830.png)

- 进入下面界面，点击环境变量

  ![image-20250628162207352](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628162207352.png)

- 在用户变量下选择新建

  ![image-20250628162243697](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628162243697.png)

- 点击新建，变量名为Java_Home,变量值为jdk所在路径

  ![image-20250628162354468](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628162354468.png)

- 选择Path，点击编辑

  ![image-20250628162415883](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628162415883.png)

- 新建两个变量

  1.  %JAVA_HOME%\bin
  2.  %JAVA_HOME%\jre\bin 

  ![image-20250628162619973](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628162619973.png)

  到这里就搞定了。

  

### 1.8 跨平台的原理和总结

**Java通过将程序编译为字节码，由不同平台上的Java虚拟机（JVM）将其转换为本地机器代码，实现跨平台运行。**

## 2 Java语言的基本语法格式

### 2.1 变量的基本概念和使用

- 变量的基本概念

  **变量相当于在计算机内存中开辟的一个存储空间，这个空间有一个名字（即变量名）**

- 变量的声明和使用

  ``` java
  public class Main {
      public static void main(String[] args) {
          //1. 声明了一个初始值为18的int类型的变量
          int age = 18;
          //2. 打印变量的数值
          System.out.println("age = "+age);//age = 18 
      }
  }
  ```

  

### 2.2 标识符及其命名规则

1. 由26个英文字母大小写，0-9，_或 $ 组成
2. 数字不可以开头。int 5abc = 1；//错误
3. 不可以使用关键字和保留字。
4. Java中严格区分大小写，长度无限制
5. 标识符不能包含空格。int a b = 99;//错误

### 2.3 变量的输入输出



```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //提示用户输入年龄和姓名
        System.out.println("请输入年龄：");
        Scanner sc = new Scanner(System.in);
        int age = sc.nextInt();
        System.out.println("请输入姓名：");
        String name = sc.next();
        //输出年龄
        System.out.println(" age = "+age);
        //输出姓名
        System.out.println(" name = "+name);
    }
}
```



### 2.4 注释的概念和注意事项

- // 表示单行注释，以`//`开头，从`//`开始到该行末尾的所有内容都被视为注释。

- 示例：

  ```java
  // 这是单行注释
  int a = 10; // 这也是单行注释
  ```

  

- 以`/*`开头，以`*/`结尾，中间的所有内容都被视为注释，可以跨越多行。

- 示例：

  ```java
  /*
   * 这是多行注释
   * 可以跨越多行
   */
  int b = 20;
  ```

- 注意：**多行注释不允许嵌套使用！！！**

### 2.5 数据类型的分类和常用进制

- 数据类型，在Java语言中分为两大类：

  - 基本数据类型

    **byte、short、int、long、float、double、char、boolean**

  - 引用数据类型

    **类、接口、注解、数组和枚举**

- 常用进制

  - 在日常生活中采用十进制进行数据的描述，权重：10^0、10^1、10^2、...
  - 在计算机底层采用二进制进行数据的描述，权重：2^0、2^1、2^2、...

### 2.6  十进制转换为二进制的方式

- 正十进制转换为二进制的方式

  十进制转二进制的转换原理：除以2，反向取余数，直到商为0终止，将所有得到的余数最终正序输出

  ![image-20250628170947880](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628170947880.png)

  得到二进制为1001

- 负十进制转换为二进制的方式

  负十进制转二进制的转换原理：除以2，反向取余数，直到商为0终止，将所有得到的余数最终逆序输出

  ![image-20250628171802821](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628171802821.png)

  得到二进制为101010

### 2.7 二进制转换为十进制的方式

- 正二进制转换为十进制的方式

  ![image-20250628172418458](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628172418458.png)

  

- 负二进制转换为十进制的方式

  

![image-20250628172302726](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250628172302726.png)



## 3 运算符与表达式



### 3.1 算术运算符的概念和使用

- 算术运算符是用于执行基本数学运算的符号。

  ```
  + 表示加法运算符		- 表示减法运算符		* 表示乘法运算符
  / 表示除法运算符		% 表示取模/取余运算符
  ```

- 示例：

  ``` java
  public class Main {
      public static void main(String[] args) {
          int a = 5;
          int b = 2;
          System.out.println(a + b);//7
          System.out.println(a - b);//3
          System.out.println(a * b);//10
          System.out.println(a / b);//2
          System.out.println(a % b);//1，这是5除以2的余数
      }
  }
  ```

  

- 注意事项

  ```java
  public class Main {
      public static void main(String[] args) {
          int a = 5;
          int b = 2;
          System.out.println(a / b);//2
          //将其中一个变量转化为double类型，就可以保留小数
          System.out.println((double) a / b);//2.5
      }
  }
  ```

  注意这里a / b 不等于2.5，也没有四舍五入等于3，而是取的2.5前面的整数，也就是2.

- 数字0作为除数的注意事项

  ``` java
  public class Main {
      public static void main(String[] args) {
          int a = 5;
          int b = 0;
          System.out.println(a/b);
      }
  }
  ```

  

  - 编译ok，但是运行发生**ArithmeticException**异常

  ![image-20250629094445766](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250629094445766.png)

- 算术运算符实现秒数的拆分

  ``` java
  import java.util.Scanner;
  
  public class Main {
      public static void main(String[] args) {
          Scanner sc = new Scanner(System.in);
          System.out.println("请输入一个整数类型的秒数");
          int number = sc.nextInt();
          // 将秒数转换为时分秒
          int hour = number / 3600; //拆分小时数,3666/3600=1
          int minute = (number % 3600) / 60; //拆分分钟数,3666%3600=66,66/60=1
          int second = number % 60; //拆分秒数,3666%60=6
          // 输出结果
          System.out.println(number + "秒转换为:" + hour + "时" + minute + "分" + second + "秒");
      }
  }
  ```

- 算术运算符和字符串连接符的区分

  **+** 既可以作为算术运算符也可以作为字符串连接符，区分方式如下：

  ``` java
  public class Main {
      public static void main(String[] args) {
          int a = 1;
          int b = 1;
          int c = 6;
          System.out.println(""+a + b + c);//116,
          System.out.println(a + "" + b + c);//166
          System.out.println(a + b + "" + c);//26
          System.out.println(a + b + c + "");//8
          System.out.println(a + (b + c ) + "");//8
          System.out.println(a + b + (c + ""));//26
      }
  }
  ```

  注意：**只要+两端的操作数有一个是字符串类型，则按照字符串连接符对待**

### 3.2 关系运算符的概念和使用

- 关系运算符用于比较两个操作数的大小关系，其运算结果是一个布尔值，即“真”（true）或“假”（false）。

  ```
  > 表示是否大于运算符		>= 表示是否大于等于运算符
  < 表示是否小于运算符		<= 表示是否小于等于运算符
  == 运算符表示是否相等	!= 运算符表示是否不相等
  ```

- 示例：

  ``` java
  public class Main {
      public static void main(String[] args) {
          int a = 3;
          int b = 2;
          System.out.println(a >  b);// true
          System.out.println(a >= b);// true
          System.out.println(a <  b);// false
          System.out.println(a <= b);// false
          System.out.println(a == b);// false
          System.out.println(a != b);// true
      }
  }
  ```

  

- 注意：所有以关系运算符作为最终运输的表达式结果一定是boolean类型

### 3.3 自增减运算符的概念和使用

- ++ 表示自增运算符，主要用于使得变量自身的数值加1

- **--**   表示自减运算符，主要用于使得变量自身的数值减1

- 示例

  ```java
  public class Main {
      public static void main(String[] args) {
          int a = 3;
          int b = 2;
          ++a;
          --b;
          System.out.println(a);//4
          System.out.println(b);//1
      }
  }
  ```

- 注意事项：a++表示先让a的数值作为表达式的结果，然后再自增，++a则反之

  ```java
  public class Main {
      public static void main(String[] args) {
          int a = 3;
          System.out.println(++a);//4
          System.out.println(a++);//4
          System.out.println(a);//5
      }
  }
  ```

  

### 3.4 逻辑运算符的概念和使用

- 逻辑运算符是用于对逻辑值（布尔值）进行操作的运算符

  ```
  &&(逻辑与)		当且仅当两个操作数都为“真”时，结果才为“真”，否则为“假”
  ||(逻辑或)		当且仅当两个操作数都为“假”时，结果才为“假”，否则为“真”
  !(逻辑非)		对操作数的逻辑值进行取反操作。如果操作数为“真”，结果为“假”；如果操作数为“假”，结果为“真”
  ```

  ![image-20250629103102316](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250629103102316.png)

- 逻辑运算符的短路特性

  ```java
  public class Main {
      public static void main(String[] args) {
          int a = 3;
          int b = 2;
          boolean bl = (++a == 3) && (++b == 2);
          // 当++a == 3时为false，右边就不会执行了
          System.out.println(bl);//false
          System.out.println(a);//4
          System.out.println(b);//2
          boolean b4 = (++a == 5) || (++b == 2);
          // 当++a == 5时为true，右边就不会执行了
          System.out.println(b4);//false
          System.out.println(a);//5
          System.out.println(b);//2
      }
  }
  ```

  

### 3.5 三元运算符的概念和使用

- 三元运算符是一种特殊的运算符，用于根据一个条件表达式的真假来选择两个值中的一个

- 三元运算符的语法通常为：

  **条件表达式 ? 表达式1 : 表达式2**,如果为true则执行表达式1，反之执行表达式2

  ``` java
  import java.util.Scanner;
  public class Main {
      public static void main(String[] args) {
          Scanner sc = new Scanner(System.in);
          System.out.print("请输入一个整数：");
          int n = sc.nextInt();
          System.out.println(n < 0 ? "负数":"非负数");
      }
  }
  ```

### 3.6 赋值运算符的概念和使用

- 赋值运算符是用于将一个值赋给一个变量的运算符

  如：a = 2，将2赋值给a，覆盖原来的值

- 符合赋值

  ```java
  int a = 2;
  a = a + 3;	从结果上等价于	 a += 3
  ```

### 3.7 运算符的优先级

![image-20250629105522953](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250629105522953.png)\

### 3.8 位移运算符的概念和基本使用

- 位移运算符是用于对整数的二进制表示进行左移或右移操作的运算符。

  **<<** 表示左移运算符，用于将数据的二进制位向左移动，右边使用0补充

  **>> **表示右移运算符，用于将数据的二进制位向右移动，左边使用符号位补充

  **>>> **表示逻辑右移运算符，用于将数据的二进制位向右移动，左边使用0补充

  

  ```java
  public class Main {
      public static void main(String[] args) {
          int a = 10; // 二进制表示为 0000 1010
          int b = a >> 1; // 将二进制位向右移动1位，二进制表示为 0000 0101，结果 b = 5
          System.out.println(b);//5
      }
  }
  ```

  

### 3.9 位运算符的概念和基本使用

- 位运算符是用于直接对整数的二进制位进行操作的运算符

  ```
  按位与（&）		对两个操作数的每一位进行逻辑与操作。只有当两个操作数的对应位都为1时，结果位才为1，否则为0。
  按位或（|）		对两个操作数的每一位进行逻辑或操作。只要两个操作数的对应位中有一个为1，结果位就为1，否则为0。
  按位异或（^）	    对两个操作数的每一位进行逻辑异或操作。只有当两个操作数的对应位不同时，结果位才为1，否则为0。
  按位取反（~）	    对操作数的每一位进行逻辑取反操作。将1变为0，将0变为1。
  ```

- 示例：

  ``` java
  public class Main {
      public static void main(String[] args) {
          int b1 = 11;// 00001011
          int b2 = 13;// 00001101
          System.out.println(b1 & b2);// 00001001 => 9
          System.out.println(b1 | b2);// 00001111 => 15
          System.out.println(b1 ^ b2);// 00000110 => 6
          System.out.println(~b1);//00001011 => 11110100 => 11110011 => 00001100 => -12
      }
  }
  ```

  

## 4 运算符与表达式



### 4.1 分支结构if语句的概念和使用

- #### if分支结构

  **分支结构是一种程序控制结构，它根据条件的真假来选择不同的执行路径。**

  ```java
  public class Main {
      public static void main(String[] args) {
          int score = 85;
          if (score >= 60) {//成立
              System.out.println("及格");//执行
          }
      }
  }
  ```

  输出结果为及格

  ``` java
  public class Main {
      public static void main(String[] args) {
          int score = 55;
          if (score >= 60) {//不成立
              System.out.println("及格");//不执行
          }else {//成立
              System.out.println("不及格");//执行
          }
      }
  }
  ```

  输出结果为不及格

- #### if_elseif_else分支结构

  **分支结构是一种程序控制结构，允许程序根据不同的条件执行不同的代码块，从而实现复杂的逻辑控制。**

  ```java
  public class Main {
      public static void main(String[] args) {
          int score = 75;
          if (score >= 90) {//不成立
              System.out.println("优秀！\n");//不执行
          } else if (score >= 80) {//不成立
              System.out.println("良好！\n");//不执行
          } else if (score >= 70) {//成立
              System.out.println("中等！\n");//执行
          } else if (score >= 60) {
              System.out.println("及格！\n");
          } else {
              System.out.println("不及格！\n");
          }
      }
  }
  ```

  输出结果为中等！

  

### 4.2 for循环的概念和使用

- **for循环是一种常用的循环结构，它允许程序重复执行一段代码，直到满足某个条件为止**

- **for循环的基本语法结构如下：**

  ```java
  for (初始化表达式; 条件表达式; 更新表达式) {
      // 循环体
  }
  初始化表达式：在循环开始前执行一次，通常用于初始化循环变量。
  条件表达式：在每次循环开始时进行判断。如果条件为true，则执行循环体；如果条件为false，则退出循环。
  更新表达式：在每次循环体执行完毕后执行，通常用于更新循环变量的值。
  循环体：在条件为true时执行的代码块。
  ```

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          for (int i = 0; i < 5; i++) {
              System.out.println("i = "+ i);
          }
      }
  }
  ```

  输出结果为：

  i = 0
  i = 1
  i = 2

- 使用for循环打印奇数

  ```java
  public class Main {
      public static void main(String[] args) {
          for (int i = 1; i < 100; i ++){
              if (i % 2 == 1){
                  System.out.println(i);
              }
          }
      }
  }
  ```

  输出结果为：

  1

  3

  ···

  99

- for循环实现累加

  ```java
  public class Main {
      public static void main(String[] args) {
          //累加的结果
          int sum = 0;
          for (int i = 1; i <= 100; i++) {
              sum += i;
          }
          System.out.println(sum);//5050
      }
  }
  ```

  输出结果为：5050

- break和continue关键字的使用

  ```
  break 		关键字用于立即终止当前所在的循环
  continue 	关键字用于跳过当前循环体内的剩余代码，并直接进入下一次循环迭代。
  ```

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          for (int i = 0; i < 10; i++){
              if (0 == i % 2){
                  continue;
              }
              if (i == 7){
                  break;
              }
              System.out.println(i);
          }
      }
  }
  ```

  输出结果为：

  1
  3
  5

- 练习：使用双重for循环打印三角形

  ```java
  public class Main {
      public static void main(String[] args) {
          for (int i = 0; i < 5; i++) {
              for (int j = 0; j <= i; j++) {
                  System.out.print("*");
              }
              //用于换行
              System.out.println();
          }
      }
  }
  ```

  输出结果：

  `*`

  `**`

  `***`

  `****`

  `*****`

### 4.3 while循环的概念和使用

- **while循环是一种在给定条件为真（true）时重复执行代码块的控制结构**

  ```java
  while (条件表达式)
  {
      // 循环体;
  }
  ```

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          int sum = 0;
          int i = 1;
          while (i <= 100) {
              sum += i;
              i++;
          }
          System.out.println("1到100的累加和是：" + sum);
      }
  }
  ```

  输出结果：

  1到100的累加和是：5050

- while循环和for循环的比较和总结

  **while循环主要用于明确循环条件但不明确循环次数的场合中**

  **for循环主要用于明确循环次数或范围的场合中**

### 4.4 switch_case分支结构的概念和使用

- **switch-case 是一种多分支选择结构，它可以根据变量的值来选择执行不同的代码块**

  `表达式的值将与`case`后面的值进行比较。如果找到匹配的值，就执行该`case`后面的代码块，直到遇到`break`语句或`switch`结构结束。`

  ```java
  switch (表达式) {
      case 字面值1:
          // 代码块1
          break;
      case 字面值2:
          // 代码块2
          break;
      ...
      default:
          // 默认代码块
  }
  ```

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          String season = "fall";//输入的季节
          switch (season) {
              case "spring":
                  System.out.println("现在是春天");
                  break;
              case "summer":
                  System.out.println("现在是夏天");
                  break;
              case "fall":
                  System.out.println("现在是秋天");
                  break;
              case "winter":
                  System.out.println("现在是冬天");
                  break;
              default:
                  System.out.println("输入的季节无效");
          }
      }
  }
  ```

  输出结果：

  现在是秋天

- 注意事项：

  如果没有`break`语句，程序会继续执行下一个`case`代码块

  ```java
  public class Main {
      public static void main(String[] args) {
          String season = "fall";//输入的季节
          switch (season) {
              case "spring":
                  System.out.println("现在是春天");
                  break;
              case "summer":
                  System.out.println("现在是夏天");
                  break;
              case "fall":
                  System.out.println("现在是秋天");//没有写break;case穿透
              case "winter":
                  System.out.println("现在是冬天");
                  break;
              default:
                  System.out.println("输入的季节无效");
          }
      }
  }
  ```

  输出结果为：

  现在是秋天
  现在是冬天

  **这是因为case穿透**

- switch()中支持的数据类型有：byte、short、char、int、enum或String

## 5 Java语言的数组声明与应用



### 5.1 数组的基本概念

- **数组**是一种数据结构，用于存储固定大小的**同类型**数据元素

### 5.2 数组的特征

1. **固定大小**：数组的大小在声明时确定，一旦确定，其大小不可改变。
2. **同类型**：数组中的所有元素必须是相同的数据类型。
3. **连续存储**：数组在内存中是连续存储的，这使得通过索引访问元素非常高效。
4. **索引访问**：数组中的每个元素都有一个唯一的索引，从0开始编号，可以通过索引快速访问和修改元素。

### 5.3 数组的声明方式和使用	

- 数组的语法格式

  ```java
  数据类型[] 数组名 = new 数据类型[数组长度];	推荐使用，容易和变量区分开来
  或者
  数据类型 数组名[] = new 数据类型[数组长度];	不推荐使用
  ```

- 数组的使用

  **数组名.length获取数组的长度**

  **使用数组名[索引]获取数组的元素**

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          //声明一个数组
          int[] arr = new int[3];
          arr[0] = 1;//赋值
          arr[1] = 2;
          arr[2] = 3;
          System.out.println("数组的长度为："+arr.length);//使用数组名.length获取数组的长度
          System.out.println("数组的第一个元素为："+arr[0]);//使用数组名[索引]获取数组的元素
          System.out.println("数组的第二个元素为："+arr[1]);
          System.out.println("数组的第三个元素为："+arr[2]);
      }
  }
  ```

- 数组的初始化操作 

  ```java
  int[] numbers = {1, 2, 3, 4, 5};
  //从一开始就赋初始值
  ```

- 注意事项：

  索引从**0**开始，最后一个元素的索引是**数组长度 - 1**，索引**arr[0]**对应的是数组的第一个元素

### 5.4 数组的增删改查

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          //声明一个长度为5元素类型为int类型的一维数组,打印所有元素值;
          int[] arr = new int[5];
          System.out.println("数组中的元素初始值为：");
          for (int i = 0; i < arr.length; i++) {
              System.out.print(arr[i] + " ");
          }
          System.out.println();
  
          //使用10、20、30、40分别给数组中前四个位置元素赋值并打印所有元素，
          for (int i = 0; i < arr.length-1; i++){
              arr[i] = (i+1) * 10;
          }
          System.out.println("数组中的元素为：");
          for (int i = 0; i < arr.length; i++) {
              System.out.print(arr[i] + " ");
          }
          System.out.println();
  
          //将数据50插入到数组中下标为0的位置,原有元素向后移动再次打印，
          for (int i = arr.length-1; i > 0; i--){
              arr[i] = arr[i-1];
          }
          arr[0] = 50;
          System.out.println("数组中的元素为：");
          for (int i = 0; i < arr.length; i++) {
              System.out.print(arr[i] + " ");
          }
          System.out.println();
  
          //将数据50从数组中删除,后续元素向前移动后再次打印所有元素
          for (int i = 0; i < arr.length-1; i++){
              arr[i] = arr[i+1];
          }
          arr[4] = 0;
          System.out.println("数组中的元素为：");
          for (int i = 0; i < arr.length; i++) {
              System.out.print(arr[i] + " ");
          }
          System.out.println();
  
          //查找数组中是否包含元素20，若包含将元素20改为200后再次打印所有
          for (int i = 0; i < arr.length; i++){
              if (arr[i] == 20){
                  arr[i] = 200;
              }
          }
          System.out.println("数组中的元素为：");
          for (int i = 0; i < arr.length; i++) {
              System.out.print(arr[i] + " ");
          }
          System.out.println();
      }
  }
  ```

  

### 5.5 二维数组的基本概念

- **二维数组是一种特殊的数据结构，可以将其想象成一个表格，由行和列组成，每个单元格存储一个元素。它是一种线性数据结构的扩展，用于存储和组织更复杂的数据，二维数组可以看作是数组的数组。**

### 5.6 二维数组的声明

- 二维数组的语法格式及声明

  ```java
  数据类型[][] 数组名称 = new 数据类型[行数][列数];
  int [][] arr = new int [2] [3];
  ```

### 5.7 二维数组的长度分析

- 二维数组的长度分析

  ```java
  brr.length表示二维数组的长度,也就是二维数组中元素的个数，也就是一维数组的个数，也就是行数
  brr[0].ength表示二维数组中的第一个元素的长度，也就是第一行的长度，也就是第一行的列数
  ```

### 5.8 二维数组的初始化

- 二维数组的初始化

  ```java
  int[][] arr = {
      {1, 2, 3, 4},
      {5, 6, 7, 8},
      {9, 10, 11, 12}
  };
  ```



### 5.9 二维数组的赋值和打印

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          int[][] arr = new int[3][4];
          // 初始化数组
          for (int i = 0; i < arr.length; i++) {
              for (int j = 0; j < arr[i].length; j++) {
                  arr[i][j] = i * arr[i].length + j + 1;
              }
          }
          //打印二维数组
          System.out.println("二维数组为：");
          for (int i = 0; i < arr.length; i++) {
              for (int j = 0; j < arr[i].length; j++) {
                  System.out.print(arr[i][j] + "\t");
              }
              System.out.println();
          }
      }
  }
  ```

​	输出结果为：

​	二维数组为：
​	1	2	3	4	
​	5	6	7	8	
​	9	10	11	12	

