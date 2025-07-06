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

​	

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

### 4.4 异常机制

**4.4.1 基本概念**

​	异常就是"不正常"的含义，在Java语言中用于表示运行阶段发生的错误。

​	java.lang.Throwable类是Java语言中所有错误(Error)和异常(Exception)的超类。
​	其中Error类主要用于描述比较严重无法编码解决的问题，如:IVM挂了。
​	其中Exception类主要用于描述比较轻微可以编码解决的问题，如:0作为除数。

**4.4.2 基本分类**

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

**4.4.3 异常的避免**

​	在以后的开发中尽量使用if条件判断来避免异常的发生。
