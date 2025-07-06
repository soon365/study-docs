# Java面向对象编程思想

## 1. 理解面向对象思想和概念

[toc]

### 1.1 对象和面向对象

1. 什么是对象？

   **万物皆对象**

2. 什么是面向对象？

   **面向对象就是指以特征(属性)和行为的观点去分析现实世界中事物的方式。**

3. 什么是面向对象编程？

   **面向对象编程就是指先使用面向对象的方式进行分析，再使用任意一门面向对象的编
   程语言进行翻译的过程。**

4. 面向对象三大特性

   **封装、继承、多态**

### 1.2  对象、类及其引用

1. 对象和类的概念

   - **对象是客观存在的实体，在Java语言体现为内存空间的一块区域。**

   - **类就是分类的概念，是对具有相同特征和行为的多个对象共性的抽象描述，在Java语言中包含描述特征的成员变量和描述行为的成员方法，是创建对象的板。**

2. 类定义的语法

   - 示例

     ```java
     class 类名 {
         数据类型 成员变量名1;
         数据类型 成员变量明2;
         返回值类型 成员方法名 (形参列表) {
             成员方法体;
         }
         //返回值主要指从方法体内向方法体外返回的数据内容。
         //形式参数主要用于将方法体外的数据传入到方法体的内部
     }
     class Person {
         String name;
         int age;
         String student (int age, String name){
             return "姓名："+name+" 年龄："+age;
         }
     }
     ```

   - 注意事项：

     1. 当类名由多个单词组成时，要求每个单词的首字母都要**大写**
     2. 当成员变量名由多个单词组成时，要求从**第二个单词起每个单词首字母大写**
     3. 返回值类型主要指返回值的数据类型，可以是基本数据类型，也可以是引用数据类型

   - 扩展：

     1. 局部变量和成员变量的区别

        局部变量：主要指在方法体中声明的变量，作用范围从声明开始到方法体结束

        成员变量：主要指在方法体外类体内声明的变量，作用范围从声明到类体结束

3. 对象创建的格式

   1. 对象创建的语法格式

      ```java
      类名 对象名 = new 类名();
      Person zhangsan = new Person();
      ```

4. 对象的引用

   根据**对象名.成员变量名**，可以引用对象的成员变量

   示例：

   ```java
   public class Person {
       private String name;
       private int age;
   
       public static void main(String[] args) {
           Person p = new Person();
           p.name = "张三";
           p.age = 18;
           System.out.println("姓名："+p.name + " 年龄：" + p.age);
       }
   }
   ```

   输出结果为：

   姓名：张三 年龄：18

5. 成员方法的调用

   成员方法语法格式：

   ```java
   public class Person {
       private String name;
       private int age;
       void student (int age, String name){
           System.out.println("姓名："+name+" 年龄："+age);
       }
   
       public static void main(String[] args) {
           Person p = new Person();
           p.name = "张三";
           p.age = 18;
           
           //变量名.成员方法名(实参列表)
           p.student(18,"张三");
       }
   }
   ```

   输出结果：

   姓名：张三 年龄：18

   

   注意事项：

   1. 实际参数的个数、类型、顺序等都必须与形参列表保持一致;
   2. 实参可以传递常量、变量、表达式以及方法的调用等;

6. person类中修改姓名和年龄

   示例：

   ```java
   public class Person {
       private String name;
       private int age;
       void student (){
           System.out.println("姓名："+name+" 年龄："+age);
       }
   	// 自定义set方法修改成员变量name的值
       public void setName(String n) {
           name = n;
       }
   	// 自定义set方法修改成员变量name的值
       public void setAge(int a) {
           age = a;
       }
       public static void main(String[] args) {
           Person p = new Person();
           p.name = "张三";
           p.age = 18;
           //修改
           p.setName("李四");
           p.setAge(28);
           //打印name和age
           p.student();
       }
   }
   ```

   输出结果：

   姓名：李四 年龄：28

7. person类中获取姓名和年龄

   示例：

   ```java
   public class Person {
       private String name;
       private int age;
       void student (){
           System.out.println("姓名："+name+" 年龄："+age);
       }
       // 自定义get方法获取成员变量name的值，并返回
       public String getName() {
           return name;
       }
       // 自定义get方法获取成员变量age的值，并返回
       public int getAge() {
           return age;
       }
       public static void main(String[] args) {
           Person p = new Person();
           p.name = "张三";
           p.age = 18;
   
           // 使用get方法获取成员变量的值
           System.out.println("姓名："+p.getName()+" 年龄："+p.getAge());
       }
   }
   ```

   输出结果：

   姓名：张三 年龄：18

### 1.3 内存结构

- 方法区

  '方法区'用于存放类的信息，**在方法区保存类的各种信息**

- 堆区

  '堆'空间用于存储使用new关键字创建的**对象**。

- 栈区

  '栈'用于存放程序运行过程当中所有的**局部变量**

## 2. 构造方法及方法重载

### 2.1 构造方法的概念和使用

- 语法结构

  ```java
  public class Person {
      //类名(){ 
      //}
      Person() {
      }
  }
  ```

- 注意事项：

  1. 构造方法的名称与类名**完全相同**，没有返回值类型连void都不许有
  2. 当使用new关键字构造对象时会自动调用构造方法进行成员变量的初始化工作

- 默认构造方法

  1. 当一个类中没有自定义任何形式的构造方法时，编译器会**自动添加**一个**无参的空构造方法**，叫做默认/缺省构造方法，如:Person(){)
  2. 若类中出现自定义构造方法，则编译器不再自动提供构造方法。

  

- 无参构造方法和有参构造方法

  ```java
  public class Person {
      private String name;
      private int age;
      void show() {
          System.out.println("姓名：" + name + "，年龄：" + age);
      }
      Person() {
      }
      Person(String n, int a) {
          name = n;
          age = a;
      }
      public static void main(String[] args) {
          Person p = new Person();
          p.show();
  
          Person p1 = new Person("张三", 18);
          p1.show();
  
      }
  }
  ```

  输出结果：

  姓名：null，年龄：0
  姓名：张三，年龄：18

### 2.2 方法重载的概念和体现形式

- 方法重载的基本概念

  在Java语言中若**方法的名称相同但参数列表不同**，这样的方法之间构成重载关系。

- 示例：

  ```java
  public class Test {
      void show(){
          System.out.println("show()");
      }
      void show(int a){//方法名相同，参数列表不同
          System.out.println("show()"+a);
      }
  
      public static void main(String[] args) {
          Test t = new Test();
          t.show();
          t.show(10);
      }
  }
  ```

  输出结果：

  show()
  show()10

- 体系形式

  参数的个数不同、参数的类型不同、参数的顺序不同，与形访法重载的主要形式有:参变量名和返回值类型无关，但建议返回值类型最好相同。

- 重载的意义

  在方法的调用者看来，似乎只有一个show方法，而它可以处理不同的数据。这样的设计方式，称为重载设计，即设计多个同名但不同参数的方法。适当的使用重载，可以使类的设计变得优雅。

### 2.3 this关键字的基本概念

- this的基本概念

  在构造方法中this关键字代表当前正在构造的对象

  在成员方法中this关键字代表当前正在调用的对象

- 示例：

  ```java
  public class Person {
      public Person() {
          System.out.println("在构造方法中：this="+ this);
      }
      public void show(){
          System.out.println("在成员方法方法中：this="+ this);
      }
      public static void main(String[] args) {
          Person p = new Person();
          p.show();
          System.out.println("在main方法中：p="+ p);
      }
  }
  ```

- 原理分析：

  当成员方法中访问成员变量时默认会加上this.(相当于汉语中"我的")，当不同的引用调用同一个成员方法时会导致成员方法中的this不同，那么this.访问的结果随之不同。

- this关键字的作用

  1. 所有的成员变量不能重名，在同一区域的局部变量不能重名，但成员变量和局部变量可以重名。在局部变量的作用区域之外，变量名代表成员变量，在局部变量的作用区域之内，代表局部变量，如果想使用成员变量，需要this.的方式访问。

     示例：

     ```java
     public class Person {
         String name;
         public void setName(String name) {
             //this.name=成员变量name
             //name=形参name
             this.name = name;
         }
         public void show(){
             System.out.println("姓名："+name);
         }
         public static void main(String[] args) {
             Person person = new Person();
             person.setName("张三");
             person.show();
         }
     }
     ```

     输出结果：

     姓名：张三

  2. 在构造方法的第一行使用this(实参)的方式可以调用本类中的其它构造方法

     示例：

     ```java
     public class Person {
         String name;
         public Person() {
             // 调用有参构造方法
             this( "张三");
             System.out.println("无参构造方法");
         }
         public Person(String name) {
             this.name = name;
             System.out.println("有参构造方法");
         }
         public static void main(String[] args) {
             Person p = new Person();
         }
     }
     ```

     输出结果：

     有参构造方法
     无参构造方法

### 2.4 方法的传参

1. 当基本数据类型的变量作为方法的参数传递时，形参变量的改变不会影响到实参

   示例：

   ```java
   public class Test {
       public void show(int i) {
           i = 200;
           System.out.println("i = "+i);//200
       }
       public static void main(String[] args) {
           Test t = new Test();
           int num = 10;
           t.show(num);
           System.out.println("num = "+num);//10
       }
   }
   ```

   输出结果：

   i = 200
   num = 10

   

2. 当引用数据类型的变量作为方法的参数传递时，形参变量指向的内容发生改变后会影响到实参变量指问的内容

   示例：

   ```java
   public class Test {
       public void show(int[] arr) {
           arr[0] = 200;
           System.out.println("arr[0] = "+arr[0]);//200
       }
       public static void main(String[] args) {
           Test t = new Test();
           int[] arr = new int[]{10,20};
           t.show(arr);
           System.out.println("arr[0] = "+arr[0]);//200
       }
   }
   ```

   输出结果：

   arr[0] = 200
   arr[0] = 200

   

### 2.5 递归调用

- 基本概念

  在一个方法体的内部调用当前方法自身的形式，叫做递归，

  示例：

  ![image-20250630172057585](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250630172057585.png)

  

  ```java
  public class Test {
      public int show(int n) {
          if (n == 1){
              return 1;
          }
          return n*show(n-1);
      }
      public static void main(String[] args) {
          Test t = new Test();
          int num = t.show(5);
          System.out.println(num);
      }
  }
  ```

  输出结果：

  120



## 3. 面向对象三大特性

### 3.1 封装

#### 封装的基本概念

- 封装是指将对象的属性（数据）和行为（方法）组合成一个独立的单元或对象，并尽可能隐藏对象的内部实现细节，**仅通过对象提供的接口（通常是方法）与外部进行交互**

- 示例:

  ![image-20250630174802802](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250630174802802.png)

### 3.2 继承

#### 继承的基本概念

- 继承是一种允许新类（子类）继承现有类（父类）的属性和方法的机制。子类继承了父类的所有非私有属性和方法，并且可以添加新的属性和方法或覆盖父类的方法。

- 示例：

  ```java
  class BaseClass {
      void baseFunction() {
          System.out.println("Base function");
      }
  }
  class DerivedClass extends BaseClass {
      void derivedFunction() {
          System.out.println("Derived function");
      }
  }
  public class Main {
      public static void main(String[] args) {
          DerivedClass obj = new DerivedClass();
          obj.baseFunction(); // 继承自BaseClass
          obj.derivedFunction(); // 自己定义的函数
      }
  }
  ```

  输出结果为：
  Base function
  Derived function

  

- 注意事项  

  1. 子类可以继承父类的成员变量和成员方法，其中私有成员变量可以继承但不可以直接使用，**子类不可以继承父类的构造方法和私有方法**。

  2. 无论使用何种方式构造子类对象时，都会自动调用父类中的无参构造方法

     ```java
     class BaseClass {
         public int a;
         public BaseClass() {
             System.out.println("无参构造方法");
         }
         public BaseClass(int a) {
             System.out.println("有参构造方法");
         }
     }
     class DerivedClass extends BaseClass {
         public DerivedClass() {
             System.out.println("子类的无参构造方法");
         }
     }
     public class Main {
         public static void main(String[] args) {
             DerivedClass obj = new DerivedClass();
         }
     }
     ```

     输出结果：

     无参构造方法
     子类的无参构造方法

  3. 使用继承必须满足子类 is a （是一个）父类的逻辑关系，也就是不能滥用继承，如学生 是一个 人类

  4. Java语言中只支持单继承不支持多继承，也就是一个子类只能有一个父类，但一个父类可以有多个子类

### 3.3 多态

#### 多态的基本概念

- 多态主要指同一种事物表现出来的多种形态

- 语法格式

  ```java
  父类类型 引用变量名 = new 子类类型
  Person p = new Student()
  p.show()
  ```

- 示例：

  ```java
  public class Person {
      private String name;
      private int age;
      public String getName() {
          return name;
      }
      public int getAge() {
          return age;
      }
      public Person(String name, int age) {
          this.name = name;
          this.age = age;
      }
      public void show() {
          System.out.println("我是父类");
          System.out.println("姓名：" + name + "，年龄：" + age);
      }
  }
  ```

  ```java
  public class Student extends Person{
      public Student(String name, int age) {
          super(name, age);
      }
      //@Override代表重写父类的方法，(要求方法名相同、参数列表相同、返回值类型相同)
      @Override
      public void show() {
          System.out.println("我是子类");
          System.out.println("Student: " + getName() + " " + getAge());
      }
  }
  ```

  

  ```java
  public class Main {
      public static void main(String[] args) {
          Person person = new Person("张三",30);
          person.show();
  
          Student student = new Student("李四",20);
          student.show();
  
          Person p = new Student("王五",18);
          //当子类没有重写show方法时，下面调用父类的show方法
          //当子类重写show方法后，下面调用子类的show方法
          //在编译阶段调用父类中的show方法，在运行阶段调用子类重写的版本
          p.show();
      }
  }
  ```

  输出结果：

  我是父类
  姓名：张三，年龄：30
  我是子类
  Student: 李四 20
  我是子类
  Student: 王五 18

#### 多态的效果

1. 当父类的引用指向子类的对象时，父类的引用可以直接调用父类独有的方法

2. 当父类的引用指向子类的对象时，父类的引用不可以直接调用子类独有的方法

3. 对于父子类都有的非静态成员方法来说，编译阶段调用父类版本，运行阶段调用子类重写以后的版本

4. 对于父子类都有的静态方法来说，编译和运行阶段都调用父类版本，隶属于类层级，因此与指向的对象无关

   示例：

   ```java
   public class Main {
       public static void main(String[] args) {
           Person person = new Person("张三",30);
   
           Student student = new Student("李四",20);
   
           Person p = new Student("王五",18);
   
           String str1 = p.getName();//调用父类的成员方法
           System.out.println(str1);
   
           p.print();//调用父类的静态方法
           Person.print();//调用父类的静态方法
       }
   }
   ```

   

#### 多态的实际意义

- 多态的实际意义在于可以屏蔽不同子类的差异性实现通用的编程，但可以调用不同的方法带来不同的结果。

#### 多态的使用场合

1. 通过方法的参数传递形成多态

2. 在方法体中直接使用多态的语法格式

   



## 4. 关键字的使用

### 4.1 static关键字的基本概念

- 在类中使用`static`修饰的变量称为静态变量。它属于类本身，而不是类的某个具体对象。
- 在类中使用`static`修饰的方法称为静态方法。它属于类本身，而不是类的某个具体对象。

### 4.2 static的使用方式

1. 在非静态的成员方法中既能访问非静态的成员也能访问静态的成员

   **(成员:成员变量+成员方法，静态成员被所有对象共享)**

2. 在静态的成员方法中只能访问静态的成员不能访问非静态的成员

   **(成员:成员变量+成员方法，调用静态方法时可能还没有创建对象)**

   示例：

   ![image-20250630194424833](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250630194424833.png)

   

3. 只有隶属于类层级被所有对象共享的内容才可以使用static修饰

   **(不能滥用static关键字)**

### 4.3 构造块和静态代码块

```java
public class Person {
    {
        System.out.println("构造块！");
    }
    static {
        System.out.println("静态块！");
    }

    public Person() {
        System.out.println("构造方法体！");
    }
}
```

```java
public class Main {
    public static void main(String[] args) {
        Person person = new Person();
    }
}
```

输出结果为：

静态块！
构造块！
构造方法体！

### 4.4 访问控制

| 访问控制符 | 访问权限 | 本类 | 本包中的类 | 子类 | 其他包中的其他类 |
| ---------- | -------- | ---- | ---------- | ---- | ---------------- |
| public     | 公有的   | ok   | ok         | ok   | ok               |
| protected  | 保护的   | ok   | ok         | ok   | no               |
| 啥也不写   | 默认的   | ok   | ok         | no   | no               |
| private    | 私有的   | ok   | no         | no   | no               |

1. public修饰的内容可以在任意位置使用
1. private修饰的内容只能在本类中使用
1. 通常情况下，成员变量都使用private修饰，成员方法都使用public修饰

### 4.5 final关键字

- 基本概念

  final本意为"**最终的，不可更改的**"，该关键字可以修饰类、成员方法、成员变量等

- 使用方法

  1. final关键字修饰类表示该类不能被继承。

     ![image-20250701100204720](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250701100204720.png)

  2. final关键字修饰成员方法表示该方法不能被重写但可以被继承

     ![image-20250701100302538](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250701100302538.png)

  3. final关键字修饰成员变量表示该成员变量必须初始化而且不能更改。

     ![image-20250701100643973](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250701100643973.png)

     ![image-20250701100659124](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250701100659124.png)

     

  4. 通常使用public static final共同修饰成员变量来表达常量的含义，常量的命名规则是:要求所有字母大写，不同单词之间采用下划线连接

     如：

     ```java
     public final static double PI = 3.14;
     ```

     

### 4.6 抽象类、抽象方法和接口

#### 抽象方法的概念和使用

- 抽象方法就是指不能具体实现的方法，也就是**没有方法体并使用abstract关键字修饰**

- 语法格式

  ```java
  访问控制符 abstract 返回值类型 方法名(形参列表);
  public abstract void cry();
  ```

#### 抽象类的概念和使用

- 抽象类就是指不能具体实例化的类，也就是不能创建对象并使用abstract关键字修饰

```java
public abstract class Person {
    public abstract void cry();
}
```

- 抽象类的注意事项：

  1. 抽象类中可以有成员变量、构造方法以及成员方法
  2. 抽象类中可以有抽象方法也可以没有抽象方法
  3. **拥有抽象方法的类必须是抽象类**，因此严格来说，具有抽象方法并且使用abstract关键字修饰的类才算真正意义上的抽象类

- 实际意义

  抽象类的意义不在于自身创建对象而在于**被继承**，当一个类继承抽象类后**必须重写**抽象类中的抽象方法，否则该类也变成抽象类，也就是说抽象类对子类具有强制性和规范性，因此叫做模板设计模式。

#### 接口的概念和使用

- 接口就是一种比抽象类还抽象的类，体现为所有成员方法都是抽象方法。

- 定义类的关键字是class，而定义接口的关键字是interface。

- 继承类的关键字是extends，而实现接口的关键字是implements

  ```java
  public interface Person {
      public static final int CNT = 18;//接口中只能有常量不能有成员变量
      public String getName();//接口中所有方法都是抽象方法
  }
  ```

  ```java
  public  class Student implements Person{
      @Override
      public String getName() {
          return null;
      }
  }
  ```

- 类和接口之间的关系

  类和类之间的关系		使用extends关键字表达继承的关系		支持单继承
  类和接口之间的关系	     使用implements关键字表达实现的关系	  支持多实现
  接口和接口之间的关系	 使用extends关键字表达继承的关系		支持多继承

#### 抽象类和接口之间的区别

1. 定义抽象类的关键字是abstract class，而定义接口的关键字是interface。
2. 继承抽象类的关键字是extends，而实现接口的关键字是implements。
3. 继承抽象类支持单继承，而实现接口可以多实现。
4. 抽象类中可以有构造方法，而接口中不可以有构造方法。
5. 抽象类中可以有成员变量，而接口中只可以有常量。
6. 抽象类中可以有成员方法，而接口中只可以有抽象方法。
7. 抽象类中增加方法可以不影响子类，而接口中增加方法通常都影响子类
8. 从jdk1.8开始允许接口中出现非抽象方法，但需要使用default关键字修饰。

### 4.7 内部类的概念和使用

#### 匿名内部类

- 如果在一段程序中需要创建一个类的对象(通常这个类需要实现某个接口或者继承某个类)，而且对象创建后这个类的价值也就不存在了，这个类可以不必命名，称之为匿名内部类。

- 语法格式

  ```java
  接口/父类类型 引用变量名= new 接口/父类类型(){方法的重写 };
  ```

- 示例：

  ```java
  public class Main {
      public static void main(String[] args) {
          Person person = new Person(){
              @Override
              public void show() {
                  System.out.println("匿名内部类");
              }
          };
          person.show();
      }
  }
  ```

#### 普通内部类

- 直接将一个类的定义放在另外一个类的类体中

  ```java
  public class Main {
      class Inner{
          void show(){
              System.out.println("内部类");
          }
      }
      public static void main(String[] args) {
          Main m = new Main();
          Inner i = m.new Inner();
          i.show();
      }
  }
  ```

  输出结果：

  内部类

#### 静态内部类

- 使用static关键字修饰的内部类，隶属于类层级

  ```java
  public class Main {
      static class Inner{
          void show(){
              System.out.println("静态内部类");
          }
      }
      public static void main(String[] args) {
          Inner inner = new Inner();
          inner.show();
      }
  }
  ```

  输出结果：

  静态内部类

#### 局部内部类

- 直接将一个类的定义放在方法体的内部时，作用范围是从声明开始一直到方法体结束

  ```java
  public class Main {
      public void show() {
          class Inner{
              void test(){
                  System.out.println("我是局部内部类");
              }
          }
          Inner inner = new Inner();//实例化
          inner.test();//调用
      }
      public static void main(String[] args) {
          Main main = new Main();
          main.show();
      }
  }
  ```

  输出结果：

  我是局部内部类



