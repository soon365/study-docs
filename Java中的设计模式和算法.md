# 四.Java中的设计模式和算法

## 1.Java常用的设计模式

### 1.1 常用的设计原则

**1.1.1 软件的开发流程**

​	需求分析文档 → 概要设计文档 → 详细设计文档 → 编码和测试 → 安装和调试 → 维护和升级

**1.1.2 常用设计原则**

​	开闭原则 - 对扩展开放，对修改关闭。

​			- 提高了代码的扩展性和维护性。

​	里氏代换原则 - 任何父类可以出现的地方，子类一定可以出现。

​				- 子类 is a 父类。

​				- 在以后的开发中多使用继承和多态的理念。

​	依赖倒转原则 - 尽量多依赖于抽象类和接口，而不是具体实现类。

​				- 在以后的开发中多使用抽象类和接口，对子类具有强制性和规范性。

​	接口隔离原则 - 尽量依赖于小接口而不是大接口，避免接口的污染。

​				- 可以降低耦合度。

​				- 耦合主要指一个模块与其它模块之间的关联度。

​	迪米特法则(最少知道原则) - 一个实体应当尽量少于其它实体之间发生相互作用。

​				- 低耦合，高内聚。

​				- 高内聚就是指将一个实体应当将该实体应该拥有的功能尽量聚集在该实体内部。

​	合成复用原则 - 尽量多使用合成的方式，而不是继承的方式。

### 1.2 常用的设计模式

**1.2.1 基本概念**

​	设计模式就是一种用于固定场合的固定套路，是多年编程经验的总结。

**1.2.2 常用的设计模式**

​	单例设计模式、模板设计模式、工厂方法模式、抽象工厂式。

**1.2.3 普通工厂方法模式**

（1）主要组成部分

1. 抽象产品 (Product): 定义产品的接口。

2. 具体产品 (ConcreteProduct): 实现抽象产品接口的具体类。

3. 抽象创建者 (Creator): 声明工厂方法，返回一个产品对象。

4. 具体创建者 (ConcreteCreator): 重写工厂方法以返回具体产品实例。

```java
// 抽象产品
interface Product {
   void operation();
}

// 具体产品A
class ConcreteProductA implements Product {
   @Override
   public void operation() {
       System.out.println("ConcreteProductA operation");
   }
}

// 具体产品B
class ConcreteProductB implements Product {
   @Override
   public void operation() {
       System.out.println("ConcreteProductB operation");
   }
}

// 抽象创建者
abstract class Creator {
   // 工厂方法
   public abstract Product factoryMethod();

   public void someOperation() {
       Product product = factoryMethod();
       product.operation();
   }
}

// 具体创建者A
class ConcreteCreatorA extends Creator {
   @Override
   public Product factoryMethod() {
       return new ConcreteProductA();
   }
}

// 具体创建者B
class ConcreteCreatorB extends Creator {
   @Override
   public Product factoryMethod() {
       return new ConcreteProductB();
   }
}

// 客户端代码
public class FactoryMethodDemo {
   public static void main(String[] args) {
       Creator creatorA = new ConcreteCreatorA();
       creatorA.someOperation();  // 输出: ConcreteProductA operation

       Creator creatorB = new ConcreteCreatorB();
       creatorB.someOperation();  // 输出: ConcreteProductB operation
   }
}
```

```
┌───────────────────┐       ┌───────────────────┐
│     <<interface>> │       │    <<abstract>>   │
│      Product      │       │      Creator      │
├───────────────────┤       ├───────────────────┤
│ +operation(): void│       │ +factoryMethod(): │
└─────────┬─────────┘       │       Product     │
          ▲                 │ +someOperation(): │
          │                 │       void        │
          │                 └─────────┬─────────┘
┌─────────┴─────────┐                 ▲
│  ConcreteProductA │                 │
├───────────────────┤       ┌─────────┴─────────┐
│ +operation(): void│       │  ConcreteCreatorA │
└───────────────────┘       ├───────────────────┤
                            │ +factoryMethod(): │
┌───────────────────┐       │     Product       │
│  ConcreteProductB │       └───────────────────┘
├───────────────────┤
│ +operation(): void│       ┌───────────────────┐
└───────────────────┘       │  ConcreteCreatorB │
                            ├───────────────────┤
                            │ +factoryMethod(): │
                            │     Product       │
                            └───────────────────┘
```

优点：

1. 解耦: 将客户端代码与具体产品类解耦。
2. 可扩展性: 添加新产品时只需添加新的创建者类，无需修改现有代码。
3. 单一职责原则: 将产品创建代码集中在一个位置，便于维护。
4. 开闭原则: 对扩展开放，对修改关闭。

**1.2.3 多个工厂方法模式**

​	多个工厂方法模式是工厂方法模式的扩展，它在一个创建者类中提供多个工厂方法，用于创建不同类型的产品。

特点：

1. 一个创建者类中包含多个工厂方法。
2. 每个工厂方法负责创建不同类型的产品。
3. 仍然保持工厂方法模式的灵活性，但提供了更集中的创建点。

```java
// 抽象产品
interface Product {
    void operation();
}

// 具体产品A
class ConcreteProductA implements Product {
    @Override
    public void operation() {
        System.out.println("ConcreteProductA operation");
    }
}

// 具体产品B
class ConcreteProductB implements Product {
    @Override
    public void operation() {
        System.out.println("ConcreteProductB operation");
    }
}

// 抽象创建者（包含多个工厂方法）
abstract class Creator {
    // 工厂方法A
    public abstract Product createProductA();
    
    // 工厂方法B
    public abstract Product createProductB();
    
    public void operationA() {
        Product product = createProductA();
        product.operation();
    }
    
    public void operationB() {
        Product product = createProductB();
        product.operation();
    }
}

// 具体创建者
class ConcreteCreator extends Creator {
    @Override
    public Product createProductA() {
        return new ConcreteProductA();
    }

    @Override
    public Product createProductB() {
        return new ConcreteProductB();
    }
}

// 客户端代码
public class MultipleFactoryMethodDemo {
    public static void main(String[] args) {
        Creator creator = new ConcreteCreator();
        
        creator.operationA();  // 输出: ConcreteProductA operation
        creator.operationB();  // 输出: ConcreteProductB operation
        
        // 也可以直接使用工厂方法
        Product productA = creator.createProductA();
        productA.operation();  // 输出: ConcreteProductA operation
        
        Product productB = creator.createProductB();
        productB.operation();  // 输出: ConcreteProductB operation
    }
}
```

```
┌───────────────────┐       ┌───────────────────┐
│     <<interface>> │       │    <<abstract>>   │
│      Product      │       │      Creator      │
├───────────────────┤       ├───────────────────┤
│ +operation(): void│       │ +createProductA():│
└─────────┬─────────┘       │       Product     │
          ▲                 │ +createProductB():│
          │                 │       Product     │
          │                 └─────────┬─────────┘
┌─────────┴─────────┐                 ▲
│  ConcreteProductA │                 │
├───────────────────┤       ┌─────────┴─────────┐
│ +operation(): void│       │    ConcreteCreator │
└───────────────────┘       ├───────────────────┤
                            │ +createProductA():│
┌───────────────────┐       │       Product     │
│  ConcreteProductB │       │ +createProductB():│
├───────────────────┤       │       Product     │
│ +operation(): void│       └───────────────────┘
└───────────────────┘
```

优点：

1. 集中管理：多个相关产品的创建逻辑集中在一个类中。
2. 灵活性：仍然保持了工厂方法模式的灵活性。
3. 可扩展性：添加新产品类型时，只需在创建者中添加新的工厂方法。
4. 一致性：相关产品的创建逻辑保持一致性。

**1.2.4 静态工厂方法模式**

​	静态工厂方法模式是一种不使用传统工厂类，而是通过类的静态方法来创建对象的变体。这是工厂方法模式的一种简化形式。

特点：

1. 使用静态方法作为工厂方法。
2. 不需要创建工厂类的实例。
3. 方法通常命名为有意义的名称（而非必须使用"create"或"new"）。
4. 可以隐藏具体实现类。

```java
// 产品接口
interface Product {
    void operation();
    
    // 静态工厂方法
    static Product createProduct(String type) {
        switch (type.toLowerCase()) {
            case "a":
                return new ConcreteProductA();
            case "b":
                return new ConcreteProductB();
            default:
                throw new IllegalArgumentException("Unknown product type");
        }
    }
    
    // 另一种常见的静态工厂方法 - 有意义的名称
    static Product createDefaultProduct() {
        return new ConcreteProductA();
    }
}

// 具体产品A
class ConcreteProductA implements Product {
    @Override
    public void operation() {
        System.out.println("ConcreteProductA operation");
    }
}

// 具体产品B
class ConcreteProductB implements Product {
    @Override
    public void operation() {
        System.out.println("ConcreteProductB operation");
    }
}

// 客户端代码
public class StaticFactoryMethodDemo {
    public static void main(String[] args) {
        // 使用静态工厂方法创建产品
        Product productA = Product.createProduct("a");
        productA.operation();  // 输出: ConcreteProductA operation
        
        Product productB = Product.createProduct("b");
        productB.operation();  // 输出: ConcreteProductB operation
        
        Product defaultProduct = Product.createDefaultProduct();
        defaultProduct.operation();  // 输出: ConcreteProductA operation
    }
}
```

```
┌───────────────────┐
│     Product       │
├───────────────────┤
│ +operation(): void│
└─────────┬─────────┘
          ▲
          │
┌─────────┴─────────┐
│  ConcreteProduct  │
├───────────────────┤
│ -ConcreteProduct()│
│ +operation(): void│
└───────────────────┘

（静态工厂方法通常存在于Product或单独的工厂类中）
```

优点：

1. 简洁性：不需要创建工厂类的实例。
2. 命名灵活性：可以使用有意义的名称而非必须使用"create"或"new"。
3. 控制实例化：可以控制实例的创建（如缓存、返回子类等）。
4. 隐藏实现：客户端代码不需要知道具体实现类。
5. 减少API复杂度：对于简单场景，比完整的工厂模式更轻量。

**1.2.5 抽象工厂方法模式**

​	抽象工厂模式是一种创建型设计模式，它提供了一种方式来创建相关或依赖对象的家族，而无需指定它们的具体类。

特点：

1. 创建多个相关产品族的对象。
2. 高层接口不依赖具体实现。
3. 强调产品之间的兼容性。
4. 比工厂方法模式更高层次的抽象。

```java
// 抽象产品A
interface Button {
    void render();
}

// 抽象产品B
interface Checkbox {
    void check();
}

// 具体产品A1
class WindowsButton implements Button {
    @Override
    public void render() {
        System.out.println("Render a Windows style button");
    }
}

// 具体产品B1
class WindowsCheckbox implements Checkbox {
    @Override
    public void check() {
        System.out.println("Check a Windows style checkbox");
    }
}

// 具体产品A2
class MacOSButton implements Button {
    @Override
    public void render() {
        System.out.println("Render a macOS style button");
    }
}

// 具体产品B2
class MacOSCheckbox implements Checkbox {
    @Override
    public void check() {
        System.out.println("Check a macOS style checkbox");
    }
}

// 抽象工厂
interface GUIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

// 具体工厂1
class WindowsFactory implements GUIFactory {
    @Override
    public Button createButton() {
        return new WindowsButton();
    }

    @Override
    public Checkbox createCheckbox() {
        return new WindowsCheckbox();
    }
}

// 具体工厂2
class MacOSFactory implements GUIFactory {
    @Override
    public Button createButton() {
        return new MacOSButton();
    }

    @Override
    public Checkbox createCheckbox() {
        return new MacOSCheckbox();
    }
}

// 客户端代码
public class Application {
    private Button button;
    private Checkbox checkbox;

    public Application(GUIFactory factory) {
        button = factory.createButton();
        checkbox = factory.createCheckbox();
    }

    public void paint() {
        button.render();
        checkbox.check();
    }

    public static void main(String[] args) {
        // 创建Windows风格的UI
        Application app1 = new Application(new WindowsFactory());
        app1.paint();
        // 输出:
        // Render a Windows style button
        // Check a Windows style checkbox

        // 创建macOS风格的UI
        Application app2 = new Application(new MacOSFactory());
        app2.paint();
        // 输出:
        // Render a macOS style button
        // Check a macOS style checkbox
    }
}
```

```
┌───────────────────┐       ┌───────────────────┐
│   AbstractFactory │       │    AbstractProductA│
├───────────────────┤       ├───────────────────┤
│ +createProductA():│<>----->│ +operationA(): void│
│    AbstractProductA│       └───────────────────┘
│ +createProductB():│               △
│    AbstractProductB│               |
└─────────┬─────────┘       ┌───────┴───────┐
          △                  │ ProductA1      │
          |                  ├───────────────┤
┌─────────┴─────────┐       │ +operationA(): │
│ ConcreteFactory1  │       │     void       │
├───────────────────┤       └───────────────┘
│ +createProductA():│
│    AbstractProductA│       ┌───────────────────┐
│ +createProductB():│       │    AbstractProductB│
│    AbstractProductB│       ├───────────────────┤
└───────────────────┘       │ +operationB(): void│
                            └─────────┬─────────┘
                                      △
                                      |
┌───────────────────┐       ┌───────┴───────┐
│ ConcreteFactory2  │       │ ProductB1      │
├───────────────────┤       ├───────────────┤
│ +createProductA():│       │ +operationB(): │
│    AbstractProductA│       │     void       │
│ +createProductB():│       └───────────────┘
│    AbstractProductB│
└───────────────────┘
```

优点：

1. 产品兼容性：确保创建的产品是兼容的（同一产品族）。
2. 解耦：客户端代码与具体类解耦。
3. 单一职责：产品创建代码集中在一个位置。
4. 开闭原则：引入新产品族时无需修改现有代码。

### 1.3 常用的查找算法

**1.3.1 线性/顺序查找算法**

（1）基本概念

​	线性查找（Linear Search），也称为顺序查找，是最简单直观的查找算法。它逐个检查数据结构中的每个元素，直到找到目标值或遍历完所有元素。

（2）常用方法

​	a.从数据结构的第一个元素开始。

​	b.逐个比较当前元素与目标值。

​	c.如果匹配，返回当前元素的索引。

​	d.如果遍历完所有元素仍未找到，返回特定值（通常为-1）表示未找到。

```java
public class LinearSearch {
    /**
     * 线性查找方法
     * @param arr 要搜索的数组
     * @param target 要查找的目标值
     * @return 目标值在数组中的索引，如果未找到返回-1
     */
    public static int linearSearch(int[] arr, int target) {
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == target) {
                return i;  // 找到目标，返回索引
            }
        }
        return -1;  // 未找到目标
    }

    public static void main(String[] args) {
        int[] data = {24, 18, 12, 9, 16, 66, 32, 4};
        int target = 16;
        
        int result = linearSearch(data, target);
        
        if (result == -1) {
            System.out.println("未找到目标元素 " + target);
        } else {
            System.out.println("元素 " + target + " 的索引位置是: " + result);
        }
    }
}
```

**1.3.2 二分/折半查找算法**

（1）基本概念

​	二分查找（Binary Search）是一种高效的查找算法，适用于已排序的数组或列表。它通过反复将搜索范围减半来快速定位目标元素。

（2）常用方法

​	a.确定数组的中间元素。

​	b.将目标值与中间元素比较：

​		- 如果目标值等于中间元素，查找成功。

​		- 如果目标值小于中间元素，在左半部分继续查找。

​		- 如果目标值大于中间元素，在右半部分继续查找。

​	c.重复上述过程，直到找到目标值或确定目标值不存在。

```java
public class BinarySearch {
    /**
     * 二分查找迭代实现
     * @param arr 已排序的数组
     * @param target 要查找的目标值
     * @return 目标值的索引，未找到返回-1
     */
    public static int binarySearch(int[] arr, int target) {
        int left = 0;
        int right = arr.length - 1;

        while (left <= right) {
            int mid = left + (right - left) / 2; // 防止整数溢出

            if (arr[mid] == target) {
                return mid;
            } else if (arr[mid] < target) {
                left = mid + 1; // 在右半部分查找
            } else {
                right = mid - 1; // 在左半部分查找
            }
        }
        return -1; // 未找到
    }

    public static void main(String[] args) {
        int[] sortedArray = {2, 5, 8, 12, 16, 23, 38, 56, 72, 91};
        int target = 23;
        
        int result = binarySearch(sortedArray, target);
        
        if (result == -1) {
            System.out.println("元素 " + target + " 不存在");
        } else {
            System.out.println("元素 " + target + " 的索引是: " + result);
        }
    }
}
```

**1.3.3 冒泡排序算法**

（1）基本概念

​	冒泡排序（Bubble Sort）是一种简单的排序算法，它通过重复地遍历要排序的列表，比较相邻元素并交换它们的位置来完成排序。

（2）常用方法

​	a.从列表的第一个元素开始，依次比较相邻的两个元素。

​	b.如果前一个元素比后一个元素大（升序排序），则交换它们的位置。

​	c.对每一对相邻元素重复这个过程，直到列表末尾。

​	d.这样一次完整的遍历称为"一轮冒泡"。

​	e.重复上述过程，直到没有任何元素需要交换（列表已排序）。

```java
//基础
public class BubbleSort {
    public static void bubbleSort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {          // 外层循环控制轮数
            for (int j = 0; j < n - i - 1; j++) {  // 内层循环控制每轮的比较次数
                if (arr[j] > arr[j + 1]) {         // 如果前一个元素比后一个大
                    // 交换两个元素的位置
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }

    public static void main(String[] args) {
        int[] arr = {64, 34, 25, 12, 22, 11, 90};
        System.out.println("排序前: " + Arrays.toString(arr));
        
        bubbleSort(arr);
        
        System.out.println("排序后: " + Arrays.toString(arr));
    }
}

//优化
public static void optimizedBubbleSort(int[] arr) {
    int n = arr.length;
    boolean swapped; // 标记是否发生了交换
    
    for (int i = 0; i < n - 1; i++) {
        swapped = false;
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                // 交换元素
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                swapped = true;
            }
        }
        
        // 如果一轮比较中没有发生交换，说明数组已经有序
        if (!swapped) {
            break;
        }
    }
}
```

