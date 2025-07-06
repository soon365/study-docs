# JavaSE核心类库

[toc]

## 1. Java的各种数据类型对象库的处理应用



### 1.1 java语言中的常用包

- 常用的包

```java
java.lang包 ————该包是Java语言中的核心包，该包中的内容由Java虚拟机自动导入
			   如:String类、System类等该包是Java语言中的工具包
                   
java.util包 ————里面包含了大量的工具类和集合类等
			   如:Scanner类、Random类等
                   
java.io包   ————该包是Java语言中的输入输出包，里面包含了大量读写文件的类等
			   如:File0utputStream类、FileInputStream类等
                   
java.net包  ————该包是Java语言中的网络包，里面包含了大量网络编程的类等
			   如:ServerSocket类、Socket类等
······
```

### 1.2 Object类

#### object类的概念

- java.lang.0bject类是所有类层次结构的根类，**任何类都是该类的直接或间接子类**

#### object类中的equals()方法

- equals()方法的功能

  用于判断**调用对象**是否与**参数对象相等**`boolean equals(0bject obj)`该方法默认**比较两个对象的地址**，与==运算符结果相同。

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          Person p = new Person();
          Person p1 = new Person();
  
          System.out.println(p.equals(p));// true
  
          System.out.println(p1.equals(p));// false
      }
  }
  ```

  输出结果：

  true
  false

- equals方法的重写和使用

- 示例：

  ```java
  @Override
  public boolean equals(Object obj) {
      // 1. 判断对象是否为同一个对象
      if (this == obj){
          return true;
      }
      // 2. 判断对象是否为空
      if (obj == null) {
          return false;
      }
      // 3. 判断对象是否为同一个类
      if (obj instanceof Person){
          return this.id == ((Person) obj).id;
      }
      return false;
  }
  ```

  ```java
  public class Main {
      public static void main(String[] args) {
          Person p = new Person(1);
          Person p1 = new Person(1);
  
          System.out.println(p1.equals(p));// true,比较内容
  
          System.out.println(p == p1);// false,比较地址
      }
  }
  ```

  输出结果：

  true
  false

- 注意事项：

  若该方法重写后，则应该重写 hashCode 方法来维护 hashCode 方法的常规协定

  

#### object类中的hashCode方法

- hashCode方法的功能

  用于获取调用对象的哈希码值(内存地址的编号)

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          Person p = new Person(1001);
          Person p1 = new Person(1001);
          System.out.println("p的哈希码值为："+p.hashCode());
          System.out.println("p1的哈希码值为："+p1.hashCode());
      }
  }
  ```

  输出结果：

  p的哈希码值为：990368553
  p1的哈希码值为：1828972342

  

#### object类中的toSring方法

- toSring方法的功能

  用于获取对象的字符串形式。

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          Person p = new Person(1001);
          Person p1 = new Person(1001);
  
          System.out.println(p.toString());//Person@3b07d329
      }
  }
  ```

  输出结果：

  Person@3b07d329

- toSring方法的重写和使用

  ```java
  @Override
  public String toString() {
      return "Person{id=" + id+"}";
  }
  ```

  ```java
  public class Main {
      public static void main(String[] args) {
          Person p = new Person(1001);
  
          System.out.println(p.toString());//Person{id=1001}
      }
  }
  ```

  输出结果：

  Person{id=1001}

### 1.3 包装类的概念和分类

#### 包装类的概念

- 在Java中，包装类是将基本数据类型封装成对象的类。Java为每种基本数据类型都提供了对应的包装类，使得基本数据类型也可以像对象一样使用。

#### 包装类的分类

![image-20250701165707920](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250701165707920.png)

### 1.4 Integer类

#### Integer类的基本概念

- java. lang.Integer类是 int 类型的包装类，里面包含了一个int类型的成员变量。

#### 常用方法

1. Integer(int value)	根据参数指定的整数构造对象
2. Integer(String 否)       根据参数指定的字符串构造对象

示例：

```java
public class Main {
    public static void main(String[] args) {
        Integer i = new Integer(10);
        Integer j = new Integer("20");

        System.out.println(i);//10 
        System.out.println(j);//20 String类型的20
    }
}
```

输出结果：

10
20

3. int intValue()                             用于获取调用对象中的整数数据并返回。

4. static Integer value0f(inti)        根据参数指定的整数返回对应的Integer对象

5. static int parseInt(String s)       用于将String类型转换为int类型并返回。

   示例：

   ```java
   public class Main {
       public static void main(String[] args) {
           Integer i = new Integer(10);
           Integer j = new Integer("20");
   
           System.out.println(j.intValue());//20
   
           Integer res = Integer.valueOf(i);
           System.out.println(res);//10
   
           res=Integer.parseInt("123456");
           System.out.println(res);//123456
       }
   }
   ```

   输出结果：

   20
   10
   123456

### 1.5 自动装箱和自动拆箱

- 自动装箱是指Java编译器在需要的时候，将基本数据类型自动转换为对应的包装类对象的过程。

- 自动拆箱是自动装箱的相反过程。它是Java编译器将包装类对象自动转换为对应的基本数据类型的过程

- 示例：

  ```java
  Integer i = 10;// 自动装箱
  int res = i;// 自动拆箱
  ```





### 1.6 BigDecimal类

#### 基本概念

- 由于float类型和double类型的运算可能会有误差，为了实现精确运算则需要借助**java.math.BigDecimal**类型加以描述。

#### 常用方法

1. BigDecimal(String val)——根据参数指定的字符串构造对象
2. BigDecimal add(BigDecimal augend)——用于计算调用对象和参数对象的和并返回
3. BigDecimal subtract(BigDecimal subtrahend)——用于计算调用对象和参数对象的差并返回
4. BigDecimal multiply(BigDecimal multiplicand)——用于计算调用对象和参数对象的积并返回
5. BigDecimal divide(BigDecimal divisor)——用于计算调用对象和参数对象的商并返回

- 示例：

  ```java
  import java.math.BigDecimal;//导入对应的包
  
  public class Main {
      public static void main(String[] args) {
          BigDecimal a = new BigDecimal("10.2");
          BigDecimal b = new BigDecimal("5.1");
  
          System.out.println("a+b="+a.add(b));
          System.out.println("a-b="+a.subtract(b));
          System.out.println("a*b="+a.multiply(b));
          System.out.println("a/b="+a.divide(b));
  
          //若商无法精确表示，则返回最接近的表示结果
          BigDecimal c = new BigDecimal("1.0");
          BigDecimal d = new BigDecimal("0.3");
          System.out.println("c/d="+c.divide(d,BigDecimal.ROUND_HALF_UP));//BigDecimal.ROUND_HALF_UP表示四舍五入
      }
  }
  ```

  输出结果：

  a+b=15.3
  a-b=5.1
  a*b=52.02
  a/b=2
  c/d=3.3

### 1.7 String类

#### 基本概念

- String类是Java中用于表示字符串的类。它是由字符序列组成的不可变对象。

#### 常量池

- 由于Sting类型描述的字符串内容是个常量不可改变，因此Java虚拟机提供了一个常量池，当Java程序中出现字符串内容时就放入常量池中，若后续出现重复的字符串内容则直接使用池中已有的对象而不需再次创建，从而提高了性能。

#### 常用构造方法

```java
import java.math.BigDecimal;//导入对应的包

public class Main {
    public static void main(String[] args) {
        String str1 = new String();
        System.out.println(str1);//空的

        byte[] b = {65,66,67,68};
        String str2 = new String(b,1,3);//把字节数组转换成字符串
        System.out.println(str2);// BCD

        String str3 = new String(b);
        System.out.println(str3);// ABC

        char[] c = {'h','e','l','l','o'};
        String str4 = new String(c);
        System.out.println(str4);// hello

        String str5 = new String("hello");
        System.out.println(str5);
    }
}
```

输出结果：

BCD
ABCD
hollo
hello

#### String类的常用方法

- 示例：

  ```java
  import java.math.BigDecimal;//导入对应的包
  
  public class Main {
      public static void main(String[] args) {
          String str1 = "Hello";
          System.out.println("str1的长度是："+str1.length());
          System.out.println("str1的第二个字符是："+str1.charAt(1));
          System.out.println("str1转大写："+str1.toUpperCase());
          System.out.println("str1转小写："+str1.toLowerCase());
          System.out.println("str1是否以H开头："+str1.startsWith("H"));
          System.out.println("str1是否以o结尾："+str1.endsWith("o"));
          System.out.println("str1是否包含ell："+str1.contains("ell"));
          System.out.println("str1是否为空："+str1.isEmpty());
  
          String str2 = " hello world ";
          System.out.println("去掉两端空格后："+str2.trim());
          System.out.println("str1和str2是否相等："+str1.equals(str2));
  
          //从下标0开始查找，找到返回索引，找不到返回-1
          int index = str1.indexOf("ell");
          System.out.println("str1中第一个ell的索引："+index);
  
          //从下标3开始取到9,包含3但不包含9
          System.out.println("从下标3取到9："+str2.substring(3,9));
      }
  }
  ```

  输出结果：

  str1的长度是：5
  str1的第二个字符是：e
  str1转大写：HELLO
  str1转小写：hello
  str1是否以H开头：true
  str1是否以o结尾：true
  str1是否包含ell：true
  str1是否为空：false
  去掉两端空格后：hello world
  str1和str2是否相等：false
  str1中第一个ell的索引：1
  从下标3取到9：llo wo

### 1.8 StringBuilder类

#### 基本概念

- StringBuilder类是Java中用于可变字符串操作的类。与String类不同，StringBuilder对象的内容是可以被修改的。

#### 常用方法

- 示例：

  ```java
  import java.math.BigDecimal;//导入对应的包
  
  public class Main {
      public static void main(String[] args) {
          StringBuilder sb1 = new StringBuilder("Hello");
          System.out.println(sb1);
          System.out.println("容量："+sb1.capacity());//16+字符串的长度
          System.out.println("长度："+sb1.length());
  
          sb1.insert(0,"World");//插入
          System.out.println(sb1);
  
          sb1.append("!");//在最后面添加
          System.out.println(sb1);
  
          sb1.delete(0,5);//删除
          System.out.println(sb1);
  
          sb1.reverse();//反转
          System.out.println(sb1);
  
          sb1.replace(0,5,"World");//替换
          System.out.println(sb1);
          
      }
  }
  ```

  输出结果：

  Hello
  容量：21
  长度：5
  WorldHello
  WorldHello!
  Hello!
  !olleH
  WorldH

### 1.9 Date类

#### 基本概念

- Date类是Java中用于表示日期和时间的类。它位于java.util包中。Date对象包含了一个特定的瞬间，精确到毫秒。

#### 常用方法

```java
import java.util.Date;

public class Main {
    public static void main(String[] args) {
        Date date1 = new Date();
        System.out.println(date1);
        
        Date date2 = new Date(1000);
        System.out.println(date2);

        // 获取调用对象表示的时间
        System.out.println("当前系统时间距离2020年1月1日0时0分0秒："+date1.getTime()+"毫秒");

        // 设置调用对象表示的时间为距离标准时间2秒的时间点
        date1.setDate(2000);
        System.out.println(date1);
    }
}
```

输出结果：

Tue Jul 01 20:45:37 CST 2025
Thu Jan 01 08:00:01 CST 1970
当前系统时间距离2020年1月1日0时0分0秒：1751373937390毫秒
Sat Dec 21 20:45:37 CST 2030

### 1.10 SimpleDateFormat类

#### 基本概念

- java.text.SimpleDateFormat类主要用于实现日期和文本之间的相关转换

#### 常用方法

- 示例：

  ```java
  import java.text.SimpleDateFormat;
  import java.util.Date;
  
  public class Main {
      public static void main(String[] args) throws Exception {
          Date date1 = new Date();
          SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");//创建SimpleDateFormat对象
          String date = sdf.format(date1);//格式化时间
          System.out.println(date);
  
          Date date2 = sdf.parse(date);//解析时间
          System.out.println(date2);
      }
  }
  ```

  输出结果：

  2025-07-01 20:51:43
  Tue Jul 01 20:51:43 CST 2025



### 1.11 Calendar类

#### 基本概念

- java.uti1.Calendar类用于取代Date类来描述年月日时分秒的特定瞬间。

#### 常用方法

- 示例：

  ```java
  import java.text.SimpleDateFormat;
  import java.util.Calendar;
  import java.util.Date;
  
  public class Main {
      public static void main(String[] args) throws Exception {
          Date date1 = new Date(2008-1900,8-1,8,20,8,8);
          SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
          System.out.println(sdf.format(date1));
  
          Calendar calendar = Calendar.getInstance();
          calendar.set(2008,8-1,8,20,8,8);//0代表一月
          Date date2 = calendar.getTime();
          System.out.println(sdf.format(date2));
      }
  }
  ```

  输出结果：

  2008-08-08 20:08:08
  2008-08-08 20:08:08



## 2. 包装类、集合、数据结构



### 2.1 集合的框架

- Java提供了容器一集合框架，集合框架中包含一系列不同数据结构的实现类。

![image-20250702093649001](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250702093649001.png)

#### 变量和数组以及集合的比较

1. 当需要在程序中记录单个数据内容时，则声明一个变量即可;
2. 当需要在程序中记录多个类型相同的数据内容时，则声明一个一维数组即可:
3. 当需要在程序中记录多个类型不同的数据内容时，则构造一个对象即可;
4. 当需要在程序中记录多个类型相同的对象时，则声明一个对象数组即可;
5. 当需要在程序中记录多个类型不同的对象时，则声明一个集合即可;

### 2.2 Collection集合

#### Collection集合的概念

- java.util.Collection集合是集合框架的根接口，其它接口是该接口的子接口。

#### Collection集合的增删改查

- 示例：

  ```java
  import java.util.ArrayList;
  import java.util.Collection;
  public class Main {
      public static void main(String[] args) throws Exception {
          Collection c = new ArrayList();
  
          c.add("one");
          c.add("two");
          System.out.println("集合的内容："+c);
  
          System.out.println("集合中是否包含one: "+c.contains("one"));
  
          c.remove("one");
          System.out.println("集合的内容："+c);
  
          c.clear();
          System.out.println("集合的内容："+c);
  
          System.out.println("集合中元素的个数："+c.size());
  
          System.out.println("集合中是否为空："+c.isEmpty());
      }
  }
  ```

  输出结果：

  集合的内容：[one, two]
  集合中是否包含one: true
  集合的内容：[two]
  集合的内容：[]
  集合中元素的个数：0
  集合中是否为空：true

### 2.3 List集合

#### 基本概念

- java.util.List集合是Collection集合的子集合，该集合中**元素有先后次序且允许重复**

- 该集合的主要实现类有:ArrayList类、LinkedList类、Stack类、Vector类等

#### ArrayList集合的增删改查

- 示例：

  ```java
  import java.util.ArrayList;
  import java.util.Collection;
  import java.util.List;
  
  public class Main {
      public static void main(String[] args) throws Exception {
          List list = new ArrayList<>();
          list.add(0,new Person(1));//添加元素
          list.add(1,7);//添加元素
          list.add(2,"30");//添加元素
          list.add(3,"40");
          System.out.println("原始的集合："+list);//输出集合
  
          // 遍历集合
          for(int i = 0; i < list.size(); i++){
              System.out.println(list.get(i));
          }
  
          list.set(1,20);//修改集合下标为1的元素
          System.out.println("修改后的集合："+list);
  
          list.remove(1);//删除集合下标为1的元素
          System.out.println("删除后的集合："+list);
  
          List subList = list.subList(0, 2);
          System.out.println("获取到的集合："+subList);
  
          // 修改subList,会导致list集合也发生改变，因为subList和list共用同一块内存
          subList.set(1, "20");
          System.out.println("修改subList后的集合："+list);
      }
  }
  ```

  输出结果：

  原始的集合：[Person{id=1}, 7, 30, 40]
  Person{id=1}
  7
  30
  40
  修改后的集合：[Person{id=1}, 20, 30, 40]
  删除后的集合：[Person{id=1}, 30, 40]
  获取到的集合：[Person{id=1}, 30]
  [Person{id=1}, 20, 40]

### 2.4 Queue集合

#### 基本概念

- java.util.Queue集合是Collection集合的子集合，与List集合是平级关系
- 该集合的主要实现类是**:LinkedList类**，因为该类在增删方面有一定的优势
- 该集合用于描述具有**先进先出特征**的数据结构，叫做队列。

#### Queue集合的方法

- 示例：

  ```java
  import java.util.LinkedList;
  import java.util.Queue;
  
  public class Main {
      public static void main(String[] args) throws Exception {
          Queue<Integer> queue = new LinkedList<>();
          for (int i = 0; i < 7; i++){
              queue.offer(i);//将一个对象添加至队尾
          }
          System.out.println("原来的队列：" +queue);
  
          System.out.println("队首的元素：" +queue.peek());//获取队首的元素
  
          System.out.println("出队的元素：" +queue.poll());//删除队首的元素
  
          System.out.println("新的队列：" +queue);
      }
  }
  ```

  输出结果：

  原来的队列：[0, 1, 2, 3, 4, 5, 6]
  队首的元素：0
  出队的元素：0
  新的队列：[1, 2, 3, 4, 5, 6]

### 2.5 Set集合

#### 基本概念

- java.util.Set集合是Collection集合的子集合，与List集合以及Queue集合平级关系
- 该集合与List集合的主要区别在于:元素**没有先后次序并且不允许重复的元素**。
- 该集合的主要实现类有:HashSet类 和 TreeSet类
- 其中HashSet类的底层采用哈希表进行数据管理的
- 其中TreeSet类的底层采用二又树进行数据管理的

#### HashSet集合放入过程

1. 先调用元素的hashCode()方法得到哈希码，通过算法计算在哈希表中的位置
2. 如果该位置没有元素，直接放入即可
3. 如果该位置有元素，调用元素的equals()方法比较是不是相等
4. 如果相等，则保留旧元素丢弃新元素
5. 如果不相等，则放入该位置的链表中下一个元素

#### set集合的方法

- 示例：

  ```java
  import java.util.HashSet;
  import java.util.Iterator;
  import java.util.Set;
  
  public class Main {
      public static void main(String[] args) throws Exception {
          Set<String> set = new HashSet<>();
          set.add("1");
          set.add("2");
          set.add("0");
          System.out.println(set.add("1"));// false
          System.out.println( set);//[0, 1, 2],没有先后顺序，和不允许重复
  
          //使用迭代器遍历集合
          Iterator<String> it = set.iterator();//创建迭代器
          while (it.hasNext()) {//判断集合中是否有下一个元素
              System.out.println(it.next());//获取集合中的下一个元素,并输出
          }
  
          set.remove("1");//删除集合中的元素
          System.out.println("删除后的集合"+set);
  
          //使用for-each遍历集合
          for(String s:set){
              System.out.println(s);
          }
      }
  }
  ```

  输出结果：

  false
  [0, 1, 2]
  0
  1
  2
  删除后的集合[0, 2]
  0
  2

### 2.6 Map集合

#### 基本概念

- java.util.Map<K,V>集合是Java中的一种数据结构，它存储键值对映射关系其中类型参数如下
- K——此映射所维护的键(key)的类型
- V——映射值(value)的类型

#### Map集合的方法

- 示例：

  ```java
  import java.util.*;
  
  public class Main {
      public static void main(String[] args) throws Exception {
          Map<Integer, String> map = new HashMap<>();
  
          String str1 =map.put(1, "one");//若集合中已经包含该Key，则替换该Key所对应的Value，返回值为该Key原来所对应的Value，若没有则返回null
          System.out.println(str1);//输出null
          String str2 =map.put(1, "two");
          System.out.println(str2);//输出one
  
          //get(key)获取集合中指定Key所对应的Value
          System.out.println("获取Key=1的Value："+map.get(1));//输出two
  
          //containsKey(key)判断集合中是否包含指定Key
          System.out.println("是否包含Key=1的："+map.containsKey(1));
  
          //containsValue(value)判断集合中是否包含指定Value
          System.out.println("是否包含Value=two的："+map.containsValue("two"));
  
          //remove(key)删除集合中指定Key所对应的Value
          System.out.println("删除的Value："+map.remove(1));
  
          map.put(1, "one");
          map.put(2, "two");
          map.put(3, "three");
          System.out.println(map);
  
          //遍历map集合
          for (Integer key:map.keySet()) {
              System.out.println(key+"--->"+map.get(key));
          }
      }
  }
  ```

  







### 2.7 泛型的概念和基本使用

#### 基本概念

- 泛型是一种允许在定义类、接口和方法时使用类型参数的技术。通过使用泛型，可以在编译时检查类型安全，避免运行时的类型转换错误。

#### 基本使用

- 示例：

  ![image-20250702103046799](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250702103046799.png)







## 3.Java的异常处理机制和文件流



### 3.1 异常机制

#### 基本概念

- 异常是指程序运行过程中出现的不正常情况。它可能是因为程序逻辑错误、外部环境因素或者用户操作不当等原因引起的

#### 基本分类

- 其中Error类主要用于描述比较严重无法编码解决的问题，如:JVM挂了

- 其中Exception类主要用于描述比较轻微可以编码解决的问题，如:0作为除数。

- java.lang.Exception类是所有异常类的超类，主要分为以下两大类:

  - RuntimeException——运行时异常，也叫作非检测性异常
  - IOException和其它异常——其它异常，也叫作检测性异常

  ![image-20250702144543415](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250702144543415.png)

  

### 3.2 异常捕获

  #### 语法格式

- 示例：

  ```java
  try{
  	编写可能发生异常的语句;
  }catch(异常类型 变量名){
      编写针对该类异常的处理语句;
  }    
  ···
  finally{
      编写无论是否发生异常都应该执行的语句;
  } 
  ```

  ```java
  import java.util.*;
  public class Main {
      public static void main(String[] args) throws Exception {
          try {
              int a = 10;
              int b = 0;
              System.out.println(a / b);
          }catch (Exception e){
              System.out.println("除数不能为0");
          }finally {
              System.out.println("程序结束");
          }
      }
  }
  ```

  输出结果：

  除数不能为0
  程序结束

- 注意事项：

  当需要编写多个catch分支时，切记小类型的异常应该放在大类型异常的上面。

  

### 3.3 异常抛出

#### 基本概念

- 在某些特殊情况下产生的异常无法处理或者不便于处理时，就可以**将该异常转移给该方法的调用者**，这种方式就叫做异常的抛出。

#### 语法格式

- 使用**throws**关键词来声明这个方法将会抛出异常。

- 示例：

  ```java
  import java.io.File;
  import java.io.FileInputStream;
  public class Main {
      public static void main(String[] args) throws Exception{// throws Exception
          FileInputStream fileInputStream = new FileInputStream(new File("c:/a.txt"));
      }
  }
  ```

  

### 3.4 自定义异常

#### 基本概念

- 自定义异常是程序员根据特定的业务需求或程序逻辑，自己定义的异常类型

#### 实现流程

- 自定义xxxxException**继承**自Exception类或者其子类:

- 提供两个版本的构造方法**:无参构造方法**和字符串作为参数的构造方法;

- 示例：

  ```java
  public void setAge(int age) throws AgeException {
      if (age < 0){
          throw new AgeException("年龄不能小于0");
      }else {
          this.age = age;
      }
  }
  ```

  ```java
  public class Main {
      public static void main(String[] args) throws AgeException {
          Person person = new Person();
          person.setName("张三");
          person.setAge(-18);
      }
  }
  ```

  输出结果：

  ![image-20250702153442325](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250702153442325.png)

  

### 3.5 file类

#### 基本概念

- java.io.File类主要用于描述文件和目录的路径信息，可以获取名称、大小等属性信息

#### 对文件的操作

- 示例：

  ```java
  import java.io.File;
  import java.io.IOException;
  import java.text.SimpleDateFormat;
  import java.util.Date;
  public class Main {
      public static void main(String[] args) throws IOException {
          File file = new File("D:/a.txt");//创建File对象
  
          if (file.exists()){//file.exists()表示文件是否存在
              System.out.println("文件名:"+file.getName());//file.getName()表示文件名
              System.out.println("文件大小:"+file.length());//file.length()表示文件大小
              Date date = new Date(file.lastModified());//file.lastModified()表示文件最后修改时间,单位毫秒
              SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
              System.out.println("最后修改时间:"+sdf.format(date));
              System.out.println("文件的绝对路径:"+file.getAbsolutePath());//file.getAbsolutePath()表示文件的绝对路径
          }else {
              System.out.println(file.createNewFile()?"创建成功":"创建失败");//file.createNewFile()表示创建文件
          }
      }
  }
  ```

  输出结果：

  文件名:a.txt
  文件大小:58
  最后修改时间:2025-07-02 15:39:38
  文件的绝对路径:D:\a.txt

#### 对文件夹的操作

- 示例：

  ```java
  import java.io.File;
  import java.io.IOException;
  public class Main {
      public static void main(String[] args) throws IOException {
          File file1 = new File("D:/Elysia");
          if (file1.exists()){
              System.out.println(file1.delete()?"删除目录成功":"删除目录失败");
          }else {
              System.out.println(file1.mkdir()?"创建目录成功":"创建目录失败");
          }
          
          File file2 = new File("D:/Elysia/Elysi/Ely");
          if (file2.exists()){
              System.out.println(file2.delete()?"删除目录成功":"删除目录失败");
          }else {
              System.out.println(file2.mkdirs()?"创建目录成功":"创建目录失败");//mkdirs()创建多级目录
          }
      }
  }
  ```

#### 获取内容

- 示例：

  ```java
  import java.io.File;
  import java.io.FileFilter;
  import java.io.IOException;
  public class Main {
      public static void main(String[] args) throws IOException {
          File file = new File("D:/Elysia/Elysia");
  
          FileFilter fileFilter = new FileFilter() {// 创建文件过滤器
              @Override
              public boolean accept(File pathname) {
                  return pathname.getName().endsWith(".txt");// 判断文件名是否以.txt结尾
              }
          };
          File[] files1 = file.listFiles();
          for (File f : files1) {
              System.out.println(f.getName());// 打印文件名
          }
          System.out.println("------------------------------------------");
          File[] files2 = file.listFiles(fileFilter);
          for (File f : files2) {
              System.out.println(f.getName());// 打印文件名
          }
      }
  }
  ```

  输出结果：

  a.txt
  Elysia
  l.txt
  x.txt

  y.txt
  ------------------------------------------

  a.txt
  l.txt
  x.txt
  y.txt

  

## 4. Java的IO流处理



### 4.1 IO流

#### 基本概念

- IO流（输入/输出流）是编程中用于处理数据输入和输出的一种机制。

#### 基本分类

- 按照数据读写的基本单位不同分为字节流和字符流。

- 其中**字节流**主要指以字节为单位进行读写的流，可以处理任意类型的文件

- 其中**字符流**主要指以字符(2个字节)为单位进行读写的流，只能处理文本文件，(主要用于处理汉字)

  

- 按照数据流动的方向不同分为:输入流和 输出流(站在程序的角度)

- 其中输入流主要指从文件中读取数据内容**输入到程序中**，也就是读文件

- 其中输出流主要指将程序中的数据内容**输出到文件中**，也就是写文件;

![image-20250702164141154](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250702164141154.png)



### 4.2 FileOutputStream类

#### 基本概念

- java.io.FileOutputStream类主要用于将图像数据之类的原始**字节**流写入输出流中

#### 常用方法

- 示例

  ```java
    import java.io.*;
    public class Main {
        public static void main(String[] args) {
            try {
                FileOutputStream fos = new FileOutputStream("D:/a.txt");
                // 写入数据,当文件不存在时，会自动创建
                // 当文件存在时，会覆盖文件
                fos.write(97);// 写入一个字节97 —— a
                fos.write('9');// 写入9
                fos.write('7');// 写入7
                String s = "hello";
                byte[] b = s.getBytes();// 将字符串转换成字节数组
                fos.write(b);
                fos.close();// 关闭流
            } catch (Exception e) {
                e.printStackTrace();
            }
        }
    }
  ```

  输出结果：

![image-20250702165739122](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250702165739122.png)

- 注意事项：

  FileOutputStream(Stfing name）只会覆盖原有的不能追加

  FileOutputStream(Stfing name,ture),才能追加

  ```java
  import java.io.*;
  public class Main {
      public static void main(String[] args) {
          try {
              FileOutputStream fos = new FileOutputStream("D:/a.txt", true);
              fos.write(97);
              fos.write('9');
              fos.write('7');
              String s = "hello";
              byte[] b = s.getBytes();// 将字符串转换成字节数组
              fos.write(b);
              fos.close();// 关闭流
          } catch (Exception e) {
              e.printStackTrace();
          }
      }
  }
  ```

  输出结果：

  ![image-20250702170318744](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250702170318744.png)


### 4.3 FileInputStream类

#### 基本概念

- java.io.FileInputStream类主要用于从输入流中读取图像数据之类的原始字节流

#### 常用方法

- 示例：

  ```java
  import java.io.*;
  public class Main {
      public static void main(String[] args){
          try {
              FileInputStream fis = new FileInputStream("D:/a.txt");
              byte[] b = new byte[20];//创建字节数组
              int res = fis.read(b);//读取数据,存储到字节数组b中，返回读取的字节个数
              String str = new String(b,0,res);//字节数组转换成字符串
              System.out.println(str);//输出字符串
              fis.close();
          } catch (Exception e) {
              e.printStackTrace();
          }
      }
  }
  ```

  输出结果：

  a97helloa97a97helloa

### 4.4 实现文件的拷贝

- 示例：

  ```java
  import java.io.*;
  public class Main {
      public static void main(String[] args){
  //          准备一个适当的缓冲区，每次将缓冲区读满就写入输出流中
          //1.构造FileInputStream类型的对象与c:/a.txt文件关联
          try {
              System.out.println("开始拷贝...");
              FileInputStream fis = new FileInputStream("d:/a.txt");
          //2.构造FileOutputStream类型的对象与c:/b.txt文件关联
              FileOutputStream fos = new FileOutputStream("d:/b.txt");
          //3.不断地从输入流中读取一个字节写入到输出流中
              byte[] b = new byte[1024*8];//创建一个缓冲区
              int len = fis.read(b);//读取
              while (len != -1){
                  fos.write(b,0,len);//将缓冲区中的数据写入输出流中
                  len = fis.read(b);//继续读取
              }
              System.out.println("拷贝完毕！");
          //4.关闭流对象并释放有关的资源
              fis.close();
              fos.close();
          } catch (Exception e) {
              e.printStackTrace();
          }
      }
  }
  ```

### 4.5 BufferedWriter类

#### 基本概念

- java.io.BufferedWriter类主要用于写入单个**字符**、字符数组以及字符串到输出流中

#### 常用方法

```java
import java.io.*;
public class Main {
    public static void main(String[] args){
        try {
            BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(new FileOutputStream("d:/a.txt")));
            char[] chars = new char[]{'h','e','l','l','o'};

            bw.write(chars);// 写入整个字符数组
            bw.write("world");// 写入字符串
            bw.newLine();// 换行符
            bw.close();// 关闭流
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```



### 4.6 BufferedReader类

#### 基本概念

- java.io.BufferedReader类用于从输入流中读取单个字符、字符数组以及字符串。

#### 常用方法

```java
import java.io.*;
public class Main {
    public static void main(String[] args){
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(new FileInputStream("d:/a.txt")));
            //准备一个字符数组，实现读满字符数组的一部分以及整个字符数组
            char[] chs = new char[20];
            // 从输入流中读取字符存放到字符数组中
            int read = br.read(chs, 2, 15);
            System.out.println("内容："+new String(chs,2,read)+"读取的字符数："+read);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

输出结果：

内容：helloworld
读取的字符数：12



### 4.7 PrintStream类

#### 基本概念

- java.io.PrintStream类主要用于方便地打印各种数据内容并且自动刷新

#### 常用方法

```java
import java.io.*;
public class Main {
    public static void main(String[] args){
        try {
            PrintStream ps = new PrintStream(new FileOutputStream("d:/a.txt"));
            ps.println("hello world1");//写入数据
            System.out.println("写入完毕");
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```



### 4.8 ObjectOutputStream类

#### 基本概念

- java.io.ObjectOutputStream类主要用于将Java语言中的对象整体写入输出流中

#### 常用方法

```java
import java.io.*;
public class Main {
    public static void main(String[] args){
        try {
            ObjectOutputStream out = new ObjectOutputStream(new FileOutputStream("d:/a.txt"));
            User user = new User("admin","123456");
            out.writeObject(user);//写入对象
            System.out.println("写入成功");
            out.close();
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```



### 4.9 ObjectInputStream类

#### 基本概念

- java.io.ObjectInputStream类主要用于从输入流中一次性将一个对象的内容读取出来实现了从字节序列到对象的转化过程，叫做反序列化。

#### 常用方法

```java
import java.io.*;
public class Main {
    public static void main(String[] args){
        try {
            ObjectInputStream in = new ObjectInputStream(new FileInputStream("d:/a.txt"));
            Object obj = in.readObject();// 读取对象
            System.out.println("读取到的对象是："+ obj);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

输出结果：

读取到的对象是：User{name='admin', password='123456'}



### 4.10 transien关键字

#### 基本概念

- transient是Javá语言的关键字，用来表示一个域不是该对象串行化的一部分

#### 使用

```java
private transient String password;

import java.io.*;
public class Main {
    public static void main(String[] args){
        try {
            ObjectOutputStream out = new ObjectOutputStream(new FileOutputStream("d:/a.txt"));
            User user = new User("admin","123456");
            out.writeObject(user);//写入对象
            System.out.println("写入成功");
            out.close();
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
//这时候被transient关键字标记的password字段不会被写入进去
```





## 5. Java的多线程处理和网络编程



### 5.1 线程

#### 基本概念

- 线程是进程内部的程序流，也就是操作系统中支持多进程，而每个进程的内部又可以支持多线程
- 程序 ——数据结构 +算法，主要指存放在硬盘上的可执行文件
- 进程——主要指运行在内存中的程序

#### 线程的创建

1. 自定义类继承Thread类并重写run方法，创建该类的实例调用start方法。
2. 自定义类实现Runnable接口并重写run方法，创建该类的实例作为实参来构造Thread类型的对象，然后使用Thread类型的对象调用start方法

- 示例：

  

#### run方法的重写和调用以及start方法的调用

- 示例一：

  ```java
  public class SubThreadRunTest extends  Thread{
      @Override
      public void run() {
          System.out.println("子线程开始运行");
          for (int i = 0; i < 7; i++){
              System.out.println("run运行,i="+i);
          }
      }
      public static void main(String[] args) {
          Thread t1 = new SubThreadRunTest();
          t1.run();//调用run方法没有交错的效果
          t1.start();//调用start方法后两个方法的输出语句会发生交错打印，每次交错的效果可能不一样
          for (int i = 0; i < 7; i++){
              System.out.println("主线程运行,i="+i);
          }
      }
  }
  ```

- 示例二：

  ```java
  public class SubRunnaleTest implements Runnable{
      @Override
      public void run() {
          for (int i = 0; i < 7; i++){
              System.out.println("run运行,i="+i);
          }
      }
  
      public static void main(String[] args) {
          SubRunnaleTest sub = new SubRunnaleTest();
          Thread t1 = new Thread(sub);
          t1.start();
          for (int i = 0; i < 7; i++){
              System.out.println("main方法中,i="+i);
          }
      }
  }
  ```

  #### 使用继承和匿名内部类的方式创建和启动线程

- 示例

  ```java
  public class Main {
      public static void main(String[] args){
          //1.使用继承和匿名内部类的方式创建和启动线程
           new Thread(){
              @Override
              public void run(){
                  System.out.println("你！好！");
              }
           }.start();//启动线程
           //2.使用接口和匿名内部类的方式创建和启动线程
          Runnable r = new Runnable(){
              @Override
              public void run(){
                  System.out.println("你！好！");
              }
          };
          Thread t2 = new Thread(r);
          t2.start();//启动线程
      }
  }
  ```

  输出结果：

  你！好！
  你！好！

### 5.2 线程的编号和名称

- 示例：

  ```java
  public class SubThreadRunTest extends Thread{
      @Override
      public void run() {
          System.out.println("当前线程的编号是："+getId()+"，当前线程名称是："+getName());
      }
      public static void main(String[] args) {
          Thread t1 = new SubThreadRunTest();
          t1.start();
  
          Thread t2 = Thread.currentThread();
          System.out.println("主线程的编号是："+t2.getId()+"，主线程名称是："+t2.getName());
      }
  }
  ```

  输出结果：

  主线程的编号是：1，主线程名称是：main
  当前线程的编号是：15，当前线程名称是：Thread-0



### 5.3 线程的优先级

- 示例：

  ```java
  public class SubThreadRunTest extends Thread{
      @Override
      public void run() {
          System.out.println("当前线程的优先级："+getPriority());//获取当前线程的优先级
      }
      public static void main(String[] args) {
          Thread t1 = new SubThreadRunTest();
          t1.setPriority(MAX_PRIORITY);//设置子线程优先级
          t1.start();
          System.out.println("主线程的优先级："+Thread.currentThread().getPriority());
      }
  }
  ```

  输出结果：

  主线程的优先级：5
  当前线程的优先级：10

- 注意：

  优先级越高的线程**不一定先执行**，但该线程获取到时间片的机会越多也就是越有可能它先执行完毕



### 5.4 七层网络模型

- ISO(国际标准委员会组织)将数据的传递从逻辑上划分为以下七层:
- 应用层、表示层、会话层、传输层、网络层、数据链路层、物理层
- 当发送数据时，需要对发送的内容按照上述七层模型进行层层加包再发送出去
- 当接收数据时，需要对接受的内容按照上述七层模型相反的次序层层拆包再解析出来

![image-20250704091646530](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250704091646530.png)

### 5.5 IP地址的概念

- 192.168.1.1-是绝大多数路由器的登录地址，进行账号密码的配置以及Mac地址过滤

- IP地址——是互联网中的唯一标识，用于定位到具体某一台设备

- IP地址本质上是由32位二进制组成的整数，叫做IPv4，当然也有128位二进制组成的整数叫做IPv6，目前主流的还是IPv4

### 5.6 端口号的概念

- 端口号就是用来绑定进程ID的，每个端口号代表一个进程。
- 端口号的范围:0-65535。
- 特殊的端口:
  HTTP:80	CFTP:21	Oracle:152]	MySQL: 3306	Tomcat:8080

### 5.7 实现客户端向服务器发送数据内容

- 示例：

  ```java
  import java.io.BufferedReader;
  import java.io.InputStreamReader;
  import java.io.PrintStream;
  import java.net.Socket;
  
  public class Main {
      public static void main(String[] args){
          try {
              Socket s = new Socket("DESKTOP-4E5BLL4",8888);//创建Socket对象
              System.out.println("连接成功");
  
              //创建输出流
              PrintStream ps = new PrintStream(s.getOutputStream());
              ps.println("hello");
              System.out.println("发送成功！");
  
              Thread.sleep(5000);//休眠5秒
              BufferedReader br = new BufferedReader(new InputStreamReader(s.getInputStream()));
              String s1 = br.readLine();
              System.out.println(s1);
  
              s.close();
              ps.close();
              br.close();
          }catch (Exception e){
              e.printStackTrace();
          }
      }
  }
  ```

  输出结果：

  连接成功
  发送成功！

  ```java
  import java.io.BufferedReader;
  import java.io.InputStreamReader;
  import java.net.ServerSocket;
  import java.net.Socket;
  
  public class Test {
      public static void main(String[] args) {
          try {
              ServerSocket ss = new ServerSocket(8888);
              System.out.println("服务端端启动成功");
              Socket s = ss.accept();
              System.out.println("连接成功");
  
              BufferedReader br = new BufferedReader(new InputStreamReader(s.getInputStream()));
              String s1 = br.readLine();
              System.out.println("客户段发来的内容是："+s1);
          }catch (Exception e){
              e.printStackTrace();
          }
      }
  }
  ```

  输出结果：

  服务端端启动成功
  连接成功
  客户段发来的内容是：hello
