# 三.JavaSE核心类库

## 1.Java的各种数据类型对象库的处理应用

### 1.1 Object类

**1.1.1 常用的包**

​	java.lang包 - 该包时java语言中的核心包，该包中的内容由Java虚拟机自动导。

​	java.util包 - 该包是Java语言中的工具包，里面包含了大量的工具类和集合类等。

​	java.io包 - 该包是Java语言中的输入输出包，里面包含了大量读写文件的类等。

​	java.net包 - 该包是Java语言中的网络包，里面包含了大量网络编程的类等。

**1.1.2 Object类**

（1）基本概念

​	java.lang.Object类是所有类层次结构的根类，任何类都是该类的直接或间接子类。

（2）常用的方法

​	Object（） - 使用无参方式构造对象。

​	boolean eqals（Object obj) - 用于判断调用对象是否与参数对象相等。

​		- 该方法默认比较两个对象的地址，与==运算符结果相同。

​		- 为了使得该方法比较两个对象的内容，则需要重写该方法。

​		- 若该方法重写后，则应该重写hashCode方法来维护hashCode方法的常规协定。

```java
@Override
public boolean equals(Object obj) {
    // 1. 检查是否同一个对象
    if (this == obj) {
        return true;
    }
    
    // 2. 检查是否为null
    // 3. 检查是否是相同类型（使用getClass()或instanceof）
    if (obj == null || getClass() != obj.getClass()) {
        return false;
    }
    
    // 4. 类型转换
    MyClass other = (MyClass) obj;
    
    // 5. 比较各个关键字段
    return Objects.equals(this.field1, other.field1)
        && Objects.equals(this.field2, other.field2)
        && this.field3 == other.field3;
}
```

​	int hashCode（） - 用于获取调用对象的哈希码值(内存地址的编号)。

​		- 若调用equals方法的结果相等，则各自调用hashCode方法的结果相同。

​		- 若调用equals方法的结果不相等，则各自调用hashCode方法的结果不相同。

​		- 为了维护上述的常规协定与equals方法结果保持一致，就需要重写该方法。

```java
public class Person {
    private String name;
    private int age;
    private String passportNumber;
    
    // 构造方法和其他代码...

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;
        Person person = (Person) o;
        return age == person.age &&
               Objects.equals(name, person.name) &&
               Objects.equals(passportNumber, person.passportNumber);
    }

    @Override
    public int hashCode() {
        return Objects.hash(name, age, passportNumber);
    }
}
```

​	String toString（）- 用于获取对象的字符串形式。

​		- 该方法默认返回的字符串为:包名.类名@哈希码值的十六进制形式。

​		- 为了返回夷有意义的数据内容则需要重写该方法。

​		- 当字符串内容与引用进行连接时，自动调用toString方法。

​		- 当使用print或println方法打印引用时，会自动调用toString方法。

```java
public class Student {
    private String id;
    private String name;
    private int grade;
    private List<String> courses;
    
    // 构造方法和其他代码...

    @Override
    public String toString() {
        return "Student{" +
               "id='" + id + '\'' +
               ", name='" + name + '\'' +
               ", grade=" + grade +
               ", courses=" + courses +
               '}';
    }
}
```

### 1.2 包装类和数学处理类

**1.2.1 包装类的概念**

​	由于Java语言是一门纯面向对象编程语言，而8种基本数据类型声明的变量并不是对象为了满足Java语言的特性就需要对这些变量进行对象化处理，而实现该功能的相关类就叫做包装类。

**1.2.2 包装类的分类**

​	int → java.lang.Integer类

​	char → java.lang.Character类

​	其它类型对应的包装类就是将首字母变成大写。

**1.2.3 Integer类**

（1）基本概念

​	java.lang.Integer类是int类型的包装类，里面包含了一个int类型的成员变量。

​	该类由final关键字修饰表示不能被继承。

（2）常用方法

​	Integer（int value）- 根据参数指定的整数构造对象

​	Integer（String s）- 根据参数指定的字符串构造对象

​	该类重写了equals()、hashCode()、toString()方法。

​	int intValue() - 用于获取调用对象中的整数数据并返回。

​	static Integer valueOf（int i）- 根据参数指定的整数返回对应的Integer对象。

​	static int parseInt（String s）- 用于将String类型转换为int类型并返回。

**1.2.4 BigDecimal类**

（1）基本概念

​	由于float类型和double类型的运算可能会有误差，为了实现精确运算则需要借助java.math.BigDecimal类型加以描述。

（2）常用方法

​	BigDecimal（String val）- 根据参数指定的字符串构造对象。

​	BigDecimal add（BigDecimal augend）- 用于计算调用对象和参数对象的和并返回。

​	BigDecimal subtract（BigDecimal subtrahend）- 用于计算调用对象和参数对象的差并返回。

​	BigDecimal multiply（BigDecimal multiplicand）- 用于计算调用对象和参数对象的积并返回。

​	BigDecimal divide(（BigDecimal divisor）- 用于计算调用对象和参数对象的商并返回。

### 1.3 String类

**1.3.1 基本概念**

​	java.lang.String类用于描述字符串，Java应用程序中所有字符串字面值都可以作为String类型的对象加以描述。

​	该类描述的字符串内容是个常量，一旦创建完毕后则不能更改，因此可以被共享。

**1.3.2 常量池**

​	由于String类型描述的字符串内容是个常量不可改变，因此Java虚拟机提供了一个常量池，当Java程序中出现字符串内容时就放入常量池中，若后续出现重复的字符串内容则直接使用池中已有的对象而不需再次创建，从而提高了性能。

## 2.Java字符串和日期处理

### 2.1 String类的常用方法

**2.1.1 String类的常用方法**

​	String 类是 Java 中最常用的类之一，提供了丰富的方法来操作字符串。

**2.1.2 StringBuilder类和StringBuffer类**

（1）基本概念

​	由于String类型描述的字符串内容是个常量不可更改，当程序中出现大量类似的字符串时需要单独存放从而浪费内存空间，若希望使用一块内存空间进行存储并且可以修改字符串内容，则应该使用StringBuilder类和StringBuffer类。

​	其中StringBuffer类从jdk1.0开始存在，该类支持线程安全，因此访问的效率比较低。

​	其中StringBuilder类从jdk1.5开始存在，该类不支持线程安全，访问的效率比较高。

**2.1.3 常用方法**

StringBuilder类:

```java
// 空构造器（初始容量16）
StringBuilder sb1 = new StringBuilder();  

// 指定初始容量
StringBuilder sb2 = new StringBuilder(100);  

// 从字符串创建
StringBuilder sb3 = new StringBuilder("Hello");  
```

StringBuffer类:

```java
StringBuffer buffer = new StringBuffer();
// 多线程环境下安全
synchronized(buffer) {
    buffer.append("thread-safe");
}
```

### 2.2 日期相关的类

**2.2.1 Date类**

（1）基本概念

​	java.util.Date类用于描述特定的瞬间，可以精确到毫秒。

（2）常用的方法

```java
import java.util.Date;

// 当前日期和时间
Date now = new Date();  

// 指定毫秒数创建（从1970-01-01 00:00:00 GMT开始计算）
Date specificDate = new Date(1625097600000L);  // 2021-06-30 00:00:00 GMT
```

**2.2.2 SimpleDateFormat类**

（1）基本概念

​	java.text.SimpleDateFormat类主要用于实现日期和文本之间的相关转换。

（2）常用的方法

```java
import java.text.SimpleDateFormat;
import java.util.Date;

// 创建默认语言环境的默认格式
SimpleDateFormat sdf1 = new SimpleDateFormat();

// 创建指定模式的格式
SimpleDateFormat sdf2 = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

// 创建指定模式和语言环境的格式
SimpleDateFormat sdf3 = new SimpleDateFormat("yyyy-MM-dd", Locale.CHINA);
```

**2.2.3 Calendar类**

（1）基本概念

​	java.uti1.Calendar类用于取代Date类来描述年月日时分秒的特定瞬间。

（2）常用的方法

```java
int year = calendar.get(Calendar.YEAR);          // 年份
int month = calendar.get(Calendar.MONTH) + 1;    // 月份（0-11，需要+1）
int day = calendar.get(Calendar.DAY_OF_MONTH);   // 日
int hour = calendar.get(Calendar.HOUR_OF_DAY);   // 24小时制小时
int minute = calendar.get(Calendar.MINUTE);      // 分钟
int second = calendar.get(Calendar.SECOND);      // 秒
int millis = calendar.get(Calendar.MILLISECOND); // 毫秒
int dayOfWeek = calendar.get(Calendar.DAY_OF_WEEK); // 星期（1=周日，2=周一...7=周六）
int weekOfYear = calendar.get(Calendar.WEEK_OF_YEAR); // 年中第几周
```

## 3.包装类、集合、数据结构

### 3.1 集合（容器）框架

**3.1.1 集合的由来**

​	当需要在程序中记录单个数据内容时，则声明一个变量即可;

​	当需要在程序中记录多个类型相同的数据内容时，则声明一个一维数组即可:

​	当需要在程序中记录多个类型不同的数据内容时，则构造一个对象即可;

​	当需要在程序中记录多个类型相同的对象时，则声明一个对象数组即可;

​	当需要在程序中记录多个类型不同的对象时，则声明一个集合即可;

**3.1.2 集合框架结构**

​	在Java语言中集合框架的顶层是:java.util.Collection集合 和 java.util.Map集合。

​	其中Co1lection集合中操作元素的基本单位是:单个元素。

​	其中Map集合中操作元素的基本单位是:单对元素。

​	在以后的开发中很少直接使用Collection集合，而是使用该集合的子集合:List集合Queue集合、Set集公等。

### 3.2Collection集合

**3.2.1 基本概念**

​	java.util.Collection集合是集合框架的根接口，其它接口是该接口的子接口。

**3.2.2 常用方法**

```java
// 添加元素
boolean add(E e);                 // 添加单个元素
boolean addAll(Collection<? extends E> c); // 添加集合

// 删除元素
boolean remove(Object o);         // 删除指定元素
boolean removeAll(Collection<?> c); // 删除集合中所有元素
void clear();                    // 清空集合

// 查询
boolean contains(Object o);       // 是否包含元素
boolean containsAll(Collection<?> c); // 是否包含所有元素
boolean isEmpty();               // 是否为空
int size();                      // 元素数量

// 转换
Object[] toArray();              // 转为数组
<T> T[] toArray(T[] a);          // 转为指定类型数组

// 迭代
Iterator<E> iterator();          // 获取迭代器
```

### 3.3 List 集合

**3.3.1 基本概念**

​	java.util.List集合是Collection集合的子集合，该集合中元素有先后次序且允许重复。

​	该集合的主要实现类有:ArrayList类LinkedList类、Stack类、Vector类等。

​	其中ArrayList类的底层是采用动态数组进行数据管理，访问方便，增删不方便。

​	其中LinkedList类的底层是采用链表进行数据管理，增删方便，访问不方便。

​	其中Stack类主要用于描述具有后进先出特征的数据结构，叫做栈，lastin first out该类的底层是采用数组进行数据的管理。

​	其中Vector类的底层采用数组进行数据的管理，与ArrayList类相比属于线程安全的类因此效率比较低，在以后的开发中推荐使用ArrayList类取代之。

**3.3.2 常用方法**

```java
List<String> list = new ArrayList<>();

// 添加元素
list.add("Java");            // 尾部添加
list.add(0, "Python");       // 指定位置插入

// 获取元素
String item = list.get(0);   // 获取第一个元素

// 删除元素
list.remove(1);              // 按索引删除
list.remove("Java");         // 按元素删除

// 修改元素
list.set(0, "C++");          // 替换指定位置元素
```

### 3.4 泛型机制

**3.4.1 基本概念**

​	通常情况下集合中可以存放不同类型的对象，本质上是将这些对象全部看做Object类型放入的，因此从集合中取出元素时也是Object类型，为了表达元素最真实的数据类型就需要强制类型转换，而强制类型转换可能发生类型转换异常。

​	为了避免上述错误的发生，从jdk1.5开始提出泛型机制，也就是在集合名称的右侧使用<数据类型>的方式明确要求该集合可以存放的元素类型，若放入其它类型则编译报。

**3.4.2 原理分析**

​	泛型的本质就是参数化类型，也就是让数据类型作为参数传递，集合定义中的E相当于形式参数负责占位，而使用集合时<>中的数据类型相当于实际参数负责给形式参数初始化当初始化完毕后所有E被替换为实际参数表示的类型进行使用。

```java
// 定义泛型类
public class Box<T> {
    private T content;
    
    public void setContent(T content) {
        this.content = content;
    }
    
    public T getContent() {
        return content;
    }
}

// 使用泛型类
Box<String> stringBox = new Box<>();
stringBox.setContent("Hello");
String value = stringBox.getContent();  // 无需类型转换
```

## 4.Java中的数据结构

### 4.1Queue集合

**4.1.1 基本概念**

​	java.uti1.Queue集合是Collection集合的子集合，与List集合是平级关系。

​	该集合的主要实现类是:LinkedList类，因为该类在增删方面有一定的优势。
​	该集合用于描述具有先进先出特征的数据结构，叫做队列(firstin first out)。

### 4.2 Set集合

**4.2.1 基本概念**

​	java.uti1.Set集合是Co1lection集合的子集合，与List集合以及Queue集合平级关系。

​	该集合与List集合的主要区别在于:元素没有先后次序并且不允许重复的元素。

​	该集合的主要实现类有:HashSet类和TreeSet类其中HashSet类的底层采用哈希表进行数据管理的。

​	其中TreeSet类的底层采用二又树进行数据管理的。

**4.2.2 常用的方法**

```java
Set<String> set = new HashSet<>();

// 添加元素
set.add("Java");        // 成功返回true
set.add("Java");        // 返回false（重复）

// 删除元素
set.remove("Java");     // 成功返回true

// 查询
boolean exists = set.contains("Python");  // 检查存在
int size = set.size();                   // 元素数量
boolean empty = set.isEmpty();           // 是否为空

// 清空
set.clear();
```

注意事项：

​	当使用选代器迭代集合中的所有元素时，若使用集合中的remove方法来删除元素，则会出现ConcurrentModificationException并发修改异常，以后的开发中应该使用迭代器的remove方法来删除元素。

**4.2.3 增强版的for循环（for each）**

（1）语法格式

​	for(元素类型 变量名 : 数组名/集合名){

​		循环体：

​	}

（2）执行流程

​	不断地从数组或集合中取出一个元素并赋值给变量并执行循环体，直到处理完毕所有元素为止。

```java
int[] numbers = {1, 2, 3, 4, 5};

// 传统for循环
for (int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}

// 增强for循环
for (int num : numbers) {
    System.out.println(num);
}
```

总结：

​	遍历Set集合的方式有三种:toString()、for each结构、迭代器方式。

​	遍历List集合的方式有四种:除了上述3种方式外，还有get方法。

### **4.3 Map接口**

**4.3.1 基本概念**

​	java.uti1.Map<K,V>集合中操作元素的基本单位是:单对元素，其中类型参数如下：
​		K-此映射所维护的键(key)的类型
​		V-映射值(value)的类型

​	该集合中不允许出现重复的键，每个键最多只能映射到一个值。

​	该集合的主要实现类有:HashMap类和TreeMap类。

​	其中HashMap类的底层是采用哈希表进行数据管理的。

​	其中TreeMap类的底层是采用二又树进行数据管理的。

**4.3.2 常用方法**

```java
Map<String, Integer> map = new HashMap<>();

// 添加键值对
map.put("Alice", 90);     // {"Alice"=90}

// 键已存在时替换值
map.put("Alice", 95);     // {"Alice"=95}

// 批量添加
map.putAll(Map.of("Bob", 85, "Charlie", 88)); // {"Alice"=95, "Bob"=85, "Charlie"=88}

// 仅当键不存在时添加
map.putIfAbsent("Alice", 100); // {"Alice"=95} (不改变)
map.putIfAbsent("David", 92);  // {"Alice"=95, "Bob"=85, "Charlie"=88, "David"=92}

// 根据键删除
map.remove("Bob");        // 返回被删除的值 85

// 根据键和值匹配删除
map.remove("Alice", 90);  // 返回false（不匹配）
map.remove("Alice", 95);  // 返回true

// 清空Map
map.clear();

// 获取值
Integer score = map.get("Charlie");  // 88
Integer score = map.get("Eve");      // null

// 获取值或默认值
score = map.getOrDefault("Eve", 60); // 60

// 检查键是否存在
boolean hasKey = map.containsKey("Alice");  // true

// 检查值是否存在
boolean hasValue = map.containsValue(100);  // false

// 1. 遍历键
for (String key : map.keySet()) {
    System.out.println(key);
}

// 2. 遍历值
for (Integer value : map.values()) {
    System.out.println(value);
}

// 3. 遍历键值对（推荐）
for (Map.Entry<String, Integer> entry : map.entrySet()) {
    System.out.println(entry.getKey() + ": " + entry.getValue());
}

// 4. forEach方法（Java 8+）
map.forEach((k, v) -> System.out.println(k + "=" + v));
```



## 5.Java的异常处理机制和文件流

### 5.1 异常机制

**5.1.1 基本概念**

​	异常就是"不正常"的含义，在Java语言中用于表示运行阶段发生的错误。

​	java.lang.Throwable类是Java语言中所有错误(Error)和异常(Exception)的超类。
​	其中Error类主要用于描述比较严重无法编码解决的问题，如:IVM挂了。
​	其中Exception类主要用于描述比较轻微可以编码解决的问题，如:0作为除数。

**5.1.2 基本分类**

​	java.lang.Exception类是所有异常类的超类，主要分为以下两大类:

​		RuntimeException-运行时异常，也叫作非检测性异常

​		IOException和其它异常-其它异常，也叫作检测性异常

​			- 所谓检测性异常就是在编译阶段能够被编译器检测出来的异常

​	其中RuntimeException类的主要子类:

​		ArithmeticException-算术异常

​		ArrayIndex0utOfBoundsException-数组下标越界异常

​		NullPointerException-指针异常

​		ClassCastException-类型转换异常

​		NumberFormatException-数字格式异常

注意:
	当程序执行过程中发生异常但没有手动处理时，由Java虚拟机采用默认方式处理，而默认处理方式就是:打印异常名称、异常原因、异常发生的位置并终止程序。

**5.1.3 异常的避免**

​	在以后的开发中尽量使用if条件判断来避免异常的发生。

**5.1.4 异常的捕获**

（1）语法格式

​	try{

​		编写可能发生异常的语句；

​	}catch(异常类型 变量名){

​		编写针对该类异常处理语句；

​	}

​	………

​	finally{

​		编写无论是否发生异常都应该执行的语句；

​	}

> [!NOTE]
>
> 异常是否被捕获的区别在于：是否继续向下执行代码。

（2）注意事项
	a.当需要编写多个catch分支时，切记小类型的异常应该放在大类型异常的上面。

​	b.finally主要用于编写善后处理的语句。

**5.1.5 异常的抛出**

（1）基本概念

​	在某些特殊情况下产生的异常无法处理或不便处理时，就可以将该异常转移给该方法的调用者，这种方式就叫做异常的抛出。

（2）语法格式

​	访问权限 返回值类型 方法名称（形参列表）throws 异常类型1，异常类型2，……{}

**5.1.6 自定义异常**

（1）基本概念

​	虽然Java官方提供了大量的异常类，但一定不会包含所有开发中可能出现的异常，在Java程序中若需要使用表达特定问题的特定异常时，就需要程序员自定义异常来描述。

（2）实现流程

​	a.自定义xxxxxException类或者其子类。

​	b.提供两个版本的构造方法：无参构造方法和字符串作为参数的构造方法；

### 5.2 File类

**5.2.1 基本类型**

​	java.io.File类主要用于描述文件和目录的路径信息，可以获取名称、大小等属性信息

**5.2.2 常用方法**

​	绝对路径 - 主要指以根目录开始的路径信息，如：c:/...、b:/...、.....

​	相对路径 - 主要指以当前目录开始的路径信息，如：./... （在开发中尽量使用相对路径）

​		- . 表示当前目录	.. 表示当前目录的上一级目录

```java
// 通过路径字符串创建
File file1 = new File("C:/test/file.txt");

// 通过父路径和子路径创建
File file2 = new File("C:/test", "file.txt");

// 通过父File对象和子路径创建
File parent = new File("C:/test");
File file3 = new File(parent, "file.txt");

String path = file.getPath();      // 获取路径字符串（构造时传入的）
String absPath = file.getAbsolutePath(); // 获取绝对路径
String canPath = file.getCanonicalPath(); // 获取规范路径（解析..和.）

String name = file.getName();      // 获取文件名/目录名
String parent = file.getParent();  // 获取父目录路径

boolean exists = file.exists();    // 是否存在
boolean isFile = file.isFile();    // 是否是文件
boolean isDir = file.isDirectory(); // 是否是目录
boolean isHidden = file.isHidden(); // 是否隐藏

boolean canRead = file.canRead();  // 是否可读
boolean canWrite = file.canWrite(); // 是否可写
boolean canExec = file.canExecute(); // 是否可执行

boolean created = file.createNewFile(); // 创建新文件（文件不存在时）

boolean deleted = file.delete();   // 删除文件或空目录
```

### 5.3 IO流

**5.3.1 基本概念**

​	I/O就是Input/Output的简写，也就是输入输出的含义。

​	I/O流就是像流水一样不间断地进行输入输出的状态。

**5.3.2 基本分类**

​	按照数据读写的基本单位不同分为 字节流 和 字符流。

​	其中字节流主要指以字节为单位进行读写的流，可以处理任意类型的文件。

​	其中字符流主要指以字符(2个字节)为单位进行读写的流，只能处理文本文件。

​	按照数据流动的方向不同分为：输入流 和 输出流。

​	其中输入流主要指从文件中读取数据内容输入到程序中，也就是读文件。

​	其中输出流主要指将程序中的数据内容输出到文件中，也就是写文件。

**5.3.3 FileOutputStream类**

（1）基本概念

​	java.io.FileOutputStream类主要用于将图像数据之类的原始字节流写入输出流中。

（2）常用方法

```java
// 1. 通过文件路径创建（覆盖模式）
FileOutputStream fos1 = new FileOutputStream("output.txt");

// 2. 通过File对象创建（覆盖模式）
File file = new File("output.txt");
FileOutputStream fos2 = new FileOutputStream(file);

// 3. 追加模式（第二个参数为true表示追加）
FileOutputStream fos3 = new FileOutputStream("output.txt", true);

// 4. 通过文件描述符创建（较少使用）
FileDescriptor fd = new FileDescriptor();
FileOutputStream fos4 = new FileOutputStream(fd);

// 写入单个字节
fos.write(65);  // 写入字符'A'的ASCII码

// 写入字节数组
byte[] data = "Hello".getBytes();
fos.write(data);

// 写入字节数组的一部分
fos.write(data, 1, 3);  // 写入"ell"

// 强制刷新缓冲区（确保数据写入磁盘）
fos.flush();
```

**5.3.4 FileInputStream类**

（1）基本概念

​	java.io.FileInputStream类主要用于从输入流中读取图像数据之类的原始字节流。

（2）常用方法

```java
// 1. 通过文件路径创建
FileInputStream fis1 = new FileInputStream("input.txt");

// 2. 通过File对象创建
File file = new File("input.txt");
FileInputStream fis2 = new FileInputStream(file);

// 3. 通过文件描述符创建（较少使用）
FileDescriptor fd = new FileDescriptor();
FileInputStream fis3 = new FileInputStream(fd);

// 读取单个字节（返回0-255，-1表示结束）
int byteData = fis.read();

// 读取字节到数组（返回实际读取字节数）
byte[] buffer = new byte[1024];
int bytesRead = fis.read(buffer);

// 读取字节到数组指定位置
int bytesRead = fis.read(buffer, 0, buffer.length);

// 跳过指定字节数
long skipped = fis.skip(100);  // 跳过100字节
```

**5.3.5 BufferedWriter类**

（1）基本概念

​	java.io.Bufferedwriter类主要用于向输出流中写入单个字符、字符数组以及字符串

（2）常用方法

```java
// 1. 包装一个Writer，使用默认缓冲区大小（8192字符）
BufferedWriter bw1 = new BufferedWriter(new FileWriter("output.txt"));

// 2. 包装一个Writer，指定缓冲区大小
BufferedWriter bw2 = new BufferedWriter(new FileWriter("output.txt"), 16384);

// 3. 包装一个OutputStream（需配合字符编码）
BufferedWriter bw3 = new BufferedWriter(
    new OutputStreamWriter(
        new FileOutputStream("output.txt"), StandardCharsets.UTF_8));

// 写入单个字符
bw.write('A');

// 写入字符数组
char[] chars = {'H', 'e', 'l', 'l', 'o'};
bw.write(chars);

// 写入字符数组的一部分
bw.write(chars, 1, 3);  // 写入"ell"

// 写入字符串
bw.write("Hello World");

// 写入字符串的一部分
bw.write("Hello World", 6, 5);  // 写入"World"

// 写入换行符（自动适配操作系统）
bw.newLine();
```

**5.3.6 BufferedReader类**

（1）基本概念

​	java.io.BufferedReader类主要用于从输入流中读取单个字符、字符数组以及一行字符串内容。

（2）常用方法

```java
// 1. 包装一个Reader，使用默认缓冲区大小（8192字符）
BufferedReader br1 = new BufferedReader(new FileReader("input.txt"));

// 2. 包装一个Reader，指定缓冲区大小
BufferedReader br2 = new BufferedReader(new FileReader("input.txt"), 16384);

// 3. 包装一个InputStream（需配合字符编码）
BufferedReader br3 = new BufferedReader(
    new InputStreamReader(
        new FileInputStream("input.txt"), StandardCharsets.UTF_8));

// 读取单个字符（返回0-65535，-1表示结束）
int charData = br.read();

// 读取字符到数组（返回实际读取字符数）
char[] buffer = new char[1024];
int charsRead = br.read(buffer);

// 读取字符到数组指定位置
int charsRead = br.read(buffer, 0, buffer.length);

// 读取一行文本（不包含换行符，返回null表示结束）
String line = br.readLine();

// 跳过指定字符数
long skipped = br.skip(100);  // 跳过100字符
```

**5.3.7 PrintStream类**

（1）基本概念

​	java.io.PrintStream类主要用于方便地打印各种数据内容。

（2）常用方法

```java
PrintStream(OutputStream out)
PrintStream(OutputStream out, boolean autoFlush)
PrintStream(OutputStream out, boolean autoFlush, String encoding)
PrintStream(String fileName)
PrintStream(File file)
```

```java
import java.io.*;

public class PrintStreamExample {
    public static void main(String[] args) throws FileNotFoundException {
        // 创建 PrintStream 输出到文件
        PrintStream ps = new PrintStream("output.txt");
        
        // 打印各种数据类型
        ps.print("Hello, ");
        ps.println("World!");
        ps.println(123);
        ps.println(45.67);
        ps.printf("Formatted: %d %.2f %s", 100, 3.14159, "PI");
        
        // 检查错误
        if (ps.checkError()) {
            System.err.println("An error occurred");
        }
        
        // 关闭流
        ps.close();
        
        // 重定向标准输出
        PrintStream console = System.out;
        System.setOut(new PrintStream(new FileOutputStream("console.txt")));
        System.out.println("This goes to console.txt");
        System.setOut(console);
        System.out.println("Back to console");
    }
}
```

**5.3.8 ObjectOutputStream类**

（1）基本概念

​	java.io.0bjectOutputStream类主要用于将Java语言中的对象整体写入输出流中。

​	只能将支持 java.io.Serializable 接口的对象写入流中。

​	类通过实现 java.io.Serializable 接口以启用其序列化功能。

​	所谓序列化就是指将一个对象相关的所有信息有效组织成字节序列的转化过程。

（2）常用方法

```java
void writeObject(Object obj);     // 将指定的对象写入 ObjectOutputStream
void defaultWriteObject();       // 将当前类的非静态和非瞬态字段写入流
void writeFields();              // 将缓冲的字段写入流
```

```java
import java.io.*;

public class ObjectOutputStreamExample {
    public static void main(String[] args) {
        // 要序列化的对象
        Person person = new Person("张三", 25);
        
        try (FileOutputStream fos = new FileOutputStream("person.ser");
             ObjectOutputStream oos = new ObjectOutputStream(fos)) {
            
            // 将对象写入文件
            oos.writeObject(person);
            System.out.println("对象已序列化");
            
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

// 可序列化的类
class Person implements Serializable {
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
}
```

5.3.9 ObjectInputStream类

（1）基本概念

​	java.io.0bjectInputStream类主要用于从输入流中一次性将一个对象的内容读取出来实现了从字节序列到对象的转化过程，叫做反序列化。

（2）常用方法

```java
Object readObject()               // 从 ObjectInputStream 读取对象
void defaultReadObject()          // 从流中读取当前类的非静态和非瞬态字段
void readFields()                 // 读取持久化字段
```

```java
import java.io.*;

public class ObjectInputStreamExample {
    public static void main(String[] args) {
        try (FileInputStream fis = new FileInputStream("person.ser");
             ObjectInputStream ois = new ObjectInputStream(fis)) {
            
            // 从文件读取对象
            Person person = (Person) ois.readObject();
            System.out.println("反序列化对象: " + person);
            
        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}

// 可序列化的类（与ObjectOutputStream示例中的相同）
class Person implements Serializable {
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
}
```

> [!TIP]
>
> ​	当需要写入多个对象到文件中时，建议先将多个对象放入一个集合对象中，然后将集合对象看做一个整体只需要调用一次writeObject方法就可以写入所有内容，此时只需要调用一次readObject方法就可以将所有内容读取出来，这样就避免了通过返回值来判断是否读取到文件的末尾。

**5.3.10 transient关键字**

（1）基本概念

​	transient是Java语言的关键字，用来表示一个域不是该对象串行化的一部分。

​	当一个对象被串行化的时候，transient型变量的值不包括在串行化的表示中然而非transient型的变量是被包括进去的。

（2）常用方法

```java
import java.io.*;

public class TransientExample {
    public static void main(String[] args) {
        User user = new User("admin", "secret123", "192.168.1.1");
        
        // 序列化
        try (ObjectOutputStream oos = new ObjectOutputStream(
                new FileOutputStream("user.ser"))) {
            oos.writeObject(user);
        } catch (IOException e) {
            e.printStackTrace();
        }
        
        // 反序列化
        try (ObjectInputStream ois = new ObjectInputStream(
                new FileInputStream("user.ser"))) {
            User deserializedUser = (User) ois.readObject();
            System.out.println(deserializedUser);
        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}

class User implements Serializable {
    private static final long serialVersionUID = 1L;
    
    private String username;
    private transient String password;  // 不会被序列化
    private transient String lastLoginIp; // 不会被序列化
    
    public User(String username, String password, String lastLoginIp) {
        this.username = username;
        this.password = password;
        this.lastLoginIp = lastLoginIp;
    }
    
    @Override
    public String toString() {
        return "User{" +
                "username='" + username + '\'' +
                ", password='" + password + '\'' +  // 反序列化后为null
                ", lastLoginIp='" + lastLoginIp + '\'' + // 反序列化后为null
                '}';
    }
}
```

## 6.Java的多线程处理

### 6.1 线程

6.1.1 基本概念

​	程序 - 数据结构+算法，主要指存放在硬盘上的可执行文件。

​	进程 - 主要指运行在内存中的程序。

​	目前主流的操作系统都支持多进程，为了使得操作系统能够同时执行多个任务，但进程是重量级的，新建进程对系统的资源消耗比较大，因此进程的数量比较局限。

​	线程是进程内部的程序流，也就是操作系统中支持多进程，而每个进程的内部又可以支持多线程，线程是轻量级的，新建线程会共享所在进程的系统资源，因此以后的开发中都采用多线程技术。

​	多线程技术采用时间片轮转法实现并发执行，所谓并发就是指宏观并行微观串行的技

**6.1.2 线程的创建**

(1)创建和启动的方式

java.lang.Thread类用于描述线程，Java 虚拟机允许应用程序并发地运行多个执行线程而线程的创建和启动方式如下：

​	a.自定义类继承Thread类并重写run方法，创建该类的实例调用start方法。

​	b.自定义类实现Runnable接口并重写run方法，创建该类的实例作为实参来构造Thread类型的对象，然后使用Thread类型的对象调用start方法。

（2）相关方法的解析

​	Thread() - 使用无参方式构造对象。

​	Thread(String name) - 根据参数指定的名称来构造对象。

​	Thread(Runnable target) - 根据参数指定的接口引用来构造对象。

​	Thread(Runnable target，String name) - 根据参数指定的引用和名称构造对象。

​	void run() - 若使用Runnable类型的引用构造出来的对象调用该方法，则最终调用引用所指向对象的run方法，否则调用该方法啥也不做。

​	void start() - 用于启动线程，Java虚拟机会自动调用该线程的run方法。

（3）原理分析

​	a.执行main方法的线程叫做主线程，执行run方法的线程叫做子线程。

​	b.main方法是程序的入口，最开始只有主线程来依次执行main方法中的代码，当start方法调用成功后，线程的个数瞬间由1个变成了2个，其中子线程去执行run方法，主线程继续执行main方法的代码，两个线程各自独立运行互不影响。

​	c.当run方法执行完毕后子线程结束，当main方法执行完毕后主线程结束，但两个程谁先执行没有明确的规定，取决于操作系统的调度算法。

```java
class MyThread extends Thread {
    @Override
    public void run() {
        System.out.println("线程运行中...");
    }
}

// 使用
MyThread thread = new MyThread();
thread.start();
```

```java
class MyRunnable implements Runnable {
    @Override
    public void run() {
        System.out.println("Runnable线程运行中...");
    }
}

// 使用
Thread thread = new Thread(new MyRunnable());
thread.start();
```

```java
class MyCallable implements Callable<String> {
    @Override
    public String call() throws Exception {
        return "Callable返回结果";
    }
}

// 使用
ExecutorService executor = Executors.newSingleThreadExecutor();
Future<String> future = executor.submit(new MyCallable());
System.out.println(future.get());  // 获取返回值
executor.shutdown();
```

> [!CAUTION]
>
> 线程创建和启动的方式一相对来说代码简单，但Java语言中只支持单继承，若该类继承Thread类后则无法继承其它类;而方式二相对来说代码复杂，但不影响该类继其它类以及实现其它接口。

**6.1.3 线程的编号和名称**

（1）基本概念

​	每个Java线程都有一个唯一的标识符，称为线程ID。线程ID是一个正long数，在线程创建时分配，且在线程生命周期内不会改变。

​	每个线程都有一个名称，可用于调试和日志记录。线程名称可以在创建时指定，也可以后期修改。

（2）常用方法

```java
long threadId = Thread.currentThread().getId();
System.out.println("当前线程ID: " + threadId);
```

```java
//方法一：
Thread thread = new Thread("MyThread") {
    @Override
    public void run() {
        System.out.println("线程名称: " + getName());
    }
};
thread.start();

//方法二：
Thread thread = new Thread(() -> {
    System.out.println("线程名称: " + Thread.currentThread().getName());
});
thread.setName("MyLambdaThread");
thread.start();
```

**6.1.4 sleep方法**

（1）基本概念

​	用于暂停当前线程执行的一个静态方法，它可以让当前线程进入定时等待

（2）常用方法

```java
try {
    // 休眠1秒（1000毫秒）
    Thread.sleep(1000);
    
    // 休眠1.5秒（1500毫秒）
    Thread.sleep(1500);
    
    // 精确休眠（1秒+500纳秒）
    Thread.sleep(1000, 500);
} catch (InterruptedException e) {
    // 处理中断异常
    Thread.currentThread().interrupt(); // 重新设置中断标志
}
```

**6.1.5 线程的优先级**

（1）基本概念

​	Java线程优先级是一个整数，用于向线程调度器提示线程执行的重要性程度。理论上，优先级高的线程会比优先级低的线程获得更多的CPU时间。

（2）常用方法

```java
Thread lowPriorityThread = new Thread(() -> {
    System.out.println("低优先级线程运行");
});
lowPriorityThread.setPriority(Thread.MIN_PRIORITY); // 设置为1

Thread highPriorityThread = new Thread(() -> {
    System.out.println("高优先级线程运行");
});
highPriorityThread.setPriority(Thread.MAX_PRIORITY); // 设置为10

lowPriorityThread.start();
highPriorityThread.start();
```

**6.1.6 线程的等待**

（1）基本概念

​	线程等待是指一个线程暂停执行，直到满足特定条件后再继续执行。Java提供了多种线程等待机制，用于协调多线程间的执行顺序和资源共享。

（2）常用方法

```java
Thread workerThread = new Thread(() -> {
    // 执行一些工作
    System.out.println("工作线程正在运行...");
    try {
        Thread.sleep(2000);
    } catch (InterruptedException e) {
        Thread.currentThread().interrupt();
    }
});

workerThread.start();

try {
    workerThread.join();  // 主线程等待workerThread完成
    System.out.println("工作线程已完成");
} catch (InterruptedException e) {
    Thread.currentThread().interrupt();
}
```

**6.1.7 守护线程**

（1）基本概念

​	守护线程是一种特殊的线程类型，它的生命周期依赖于非守护线程（用户线程）。当所有非守护线程结束时，无论守护线程是否执行完毕，JVM都会自动退出并终止所有守护线程。

（2）常用方法

```java
Thread daemonThread = new Thread(() -> {
    while (true) {
        System.out.println("守护线程正在运行...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
            break;
        }
    }
});

// 必须在start()前设置为守护线程
daemonThread.setDaemon(true);  
daemonThread.start();

System.out.println("主线程结束"); 
// 当主线程结束后，守护线程会自动终止
```

## 7.Java网络编程socket

### 7.1线程的同步机制

**7.1.1 基本概念**

​	当多个线程同时访问同一种共享资源时，可能会造成数据的覆盖等不一致性问题，此时就需要进行线程之间的通信和协调，该机制就叫线程的同步机制。

**7.1.2 实现方式**

​	在Java语言中使用svnchronized关键字来实现同步/对象锁机制，来保证线程执行该段代码时的原子性(要么不执行，要么就执行完整)，具体方式如下:

​	（1）使用同步语句块的方式来锁定部分代码；

​		synchronized（任意类型的引用）{

​			编写需要锁定的代码；

​		}

​	（2）使用同步方法的方式来锁定所有代码

​			直接使用synchronized关键字来修饰整个方法：

​				synchronized（this）{整个方法代码}

**7.1.3 原理分析**

​	当多个线程调用start方法后同时去抢占共享资源，由于同步锁的存在导致只有一个线程能够抢到共享资源并进行加锁处理，其它没有抢到共享资源的线程进入阻塞状态，当该线程执行完毕所有锁定的代码后自动释放同步锁，此时阻塞状态的所有线程继续抢占共享资源，抢不到的线程再次回到阻塞状态。

> [!CAUTION]
>
> 1.多个需要同步的线程在访问该同步块时，看到的应该是同一个所对象引用。
>
> 2.在使用同步块时应当尽量减少同步范围以提高并发的执行效率。

**7.1.4 死锁的概念**

（1）基本概念

​	死锁是指两个或多个线程在执行过程中，因争夺资源而造成的一种互相等待的现象，导致这些线程都无法继。

（2）避免死锁

死锁是多线程编程中的常见问题，理解其产生条件和预防策略至关重要：

​	a.预防优于检测：设计时就考虑避免死锁的可能性

​	b.工具辅助：利用JDK提供的并发工具减少手动同步

​	c.代码规范：遵循锁获取的顺序一致性原则

​	d.监控机制：在生产环境中实施死锁检测

### 7.2 网络编程的常识

​	目前主流的网络通讯软件:微信、QQ、陌陌、探探、飞信、阿里旺旺、支付宝、……

**7.2.1 七层网络模型**

​	ISO(国际标准委员会组织)将数据的传递从逻辑上划分为以下七层:应用层、表示层、会话层、传输层、网络层、数据链路层、物理层

​	当发送数据时，需要对发送的内容按照上述七层模型进行层层加包再发送出去。

​	当接收数据时，需要对接受的内容按照上述七层模型相反的次序层层拆包再解析出来。

**7.2.2 IP地址**

​	192.168.1.1- 是绝大多数路由器的登录地址，进行账号密码的配置以及Mac地址过滤

​	IP地址 - 是互联网中的唯一标识，用于定位到具体某一台设备。

​	IP地址本质上是由32位二进制组成的整数，叫做IPv4，当然也有128位二进制组成的整，叫做IPv6。

​	日常生活中采用点分一进制表示法进行IP地址的描述，也就是将每个字节的二进制转换为一个一进制整数，不同的十进制整数之间采用小数点隔开。

**7.2.3 端口号**

​	IP地址-可以定位到具体某一台设备。

​	端口红安 - 可以定位到具体某一个进程。

​	网络编程需要提供:IP地址 +端口号。

​	端口号本质上是由16位二进制组成的整数，表示的范围:1024之65535，其中0间的端口号通常被系统占用，因此开发中从1025开始使用。

### 7.3 基于tcp协议的编程模型

**7.3.1 编程模型**

服务器：

（1）创建ServerSocket类型的对象并提供端口号。

（2）等待客户端的连接请求，调用accept方法。

（3）使用输入输出流进行通信。

（4）关闭Socket。

```java
// 创建ServerSocket
ServerSocket serverSocket = new ServerSocket(8080);

while(true) {
    // 阻塞等待客户端连接
    Socket clientSocket = serverSocket.accept();
    
    // 为每个连接创建新线程处理
    new Thread(() -> {
        try {
            // 获取输入输出流
            InputStream in = clientSocket.getInputStream();
            OutputStream out = clientSocket.getOutputStream();
            
            // 读取请求
            byte[] buffer = new byte[1024];
            int len;
            while((len = in.read(buffer)) != -1) {
                // 处理请求
                String request = new String(buffer, 0, len);
                String response = processRequest(request);
                
                // 发送响应
                out.write(response.getBytes());
            }
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            try {
                clientSocket.close();
            } catch (IOException e) {
                e.printStackTrace();
            }
        }
    }).start();
}
```

客户端：

（1）创建Socket类型的对象并提供服务器的IP地址和端口号。

（2）用输入输出流进行通信。

（3）关闭Socket。

```java
Socket socket = new Socket("localhost", 8080);

// 获取输入输出流
OutputStream out = socket.getOutputStream();
InputStream in = socket.getInputStream();

// 发送请求
String request = "Hello Server";
out.write(request.getBytes());

// 接收响应
byte[] buffer = new byte[1024];
int len = in.read(buffer);
String response = new String(buffer, 0, len);

socket.close();
```

