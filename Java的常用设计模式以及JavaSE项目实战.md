# Java的常用设计模式以及JavaSE项目实战

[toc]

## 1. Java常用的设计模式



### 1.1 常用的设计原型

- 开闭原则

  对扩展开放对修改关团：为了使程序的扩展性好，易于维护和开级。

- 里氏代换原则

  任何基类可以出现的地方，子类一定可以出现，多使用多态的方式。

- 依赖倒转原则

  尽量多依赖于抽象类或接口而不是具体实现类，对子类具有强制性和规范性

- 接口隔离原则

  尽量依赖于小接口而不是大接口，避免接口的污染

- 迪米特法则

  一个实体应当尽量少与其他实体之间发生相互作用，使系统功能块相对独立

- 合成复用原则

  尽量多使用合成/聚合的方式，而不是继承的方式。

### 1.2 常用的设计模式

#### 基本概念

- 设计模式就是一种用于固定场合的固定套路，是多年编程经验的总结

#### 常用的设计模式

- 单例设计模式、模板设计模式、工厂方法模式、抽象工厂模式。

- 示例普通工厂方法的实现

  ![image-20250705111114110](C:\Users\as202\AppData\Roaming\Typora\typora-user-images\image-20250705111114110.png)

  ```java
  public interface Sender {
      //定义发送方法
      public abstract void send();
  }
  ```

  ```java
  public class MailSender implements Sender{
      @Override
      public void send() {
          System.out.println("发送邮件");
      }
  }
  ```

  ```java
  public class SmsSender implements Sender{
  
      @Override
      public void send() {
          System.out.println("发送短信");
      }
  }
  ```

  ```java
  public class SenderFactory {
      // 自定义创建函数，根据传入参数，创建不同的发送器
      public Sender produce(String type){
          if("mail".equals(type)){
              return new MailSender();
          }else if("sms".equals(type)){
              return new SmsSender();
          }else{
              System.out.println("请输入正确的类型!");
              return null;
          }
      }
  }
  ```

  ```java
  public class SenderFactoryTest {
      public static void main(String[] args) {
          SenderFactory factory = new SenderFactory();
          Sender sender = factory.produce("mail");
          sender.send();
      }
  }
  ```

  输出结果：

  发送邮件



### 1.3 常用的算法

#### 线性/顺序查找算法

- 使用目标元素与样本数列中的第一个元素起依次比较

- 若找到与目标元素相等的元素，则表示查找成功

- 若目标元素与所有样本元素比较完毕也不相等，则表示查找失败


- 示例：

  ```java
  public class Main {
      public static int find(int[] arr,int num){
          for (int i = 0; i < arr.length; i++){
              if (arr[i] == num){//找到相等的
                  return i;
              }
          }
          return -1;//未找到
      }
      public static void main(String[] args) {
          int[] arr = {1,2,3,4,5,6,7,8,9,10};
          int num = 5;
          int res = Main.find(arr,num);
          if (res == -1){
              System.out.println("未找到");
          }else {
              System.out.println("找到，下标为：" + res);
          }
      }
  }
  ```

  输出结果：

  找到，下标为：4

#### 二分/折半查找算法

- 假定样本数列中的元素是从小到大依次排序的

- 使用目标元素与样本数列中的中间元素进行比较

- 若目标元素与中间元素相等，则表示查找成功

- 若目标元素小于中间元素，则去中间元素的左边进行查找

- 若目标元素大于中间元素，则去中间元素的右边进行查找

- 直到目标元素与所有该比较的元素比较完毕后也不相等，则表示查找失败;


- 示例：

  ```java
  public class Test {
      public static int find(int[] arr,int left,int right,int num) {
          //1.判断数组是否为空,否则返回-1
          //因为每次递归会缩短数组的范围，所以需要判断数组至少需要一个元素
          if (left <= right) {
              //        1.计算中间运算的下标，找到中间元素
              int cen = (left + right) / 2;
  //        2.使用目标元素与中间元素比较是否相等，若相等则直接返回下标
              if (arr[cen] == num) {
                  return cen;
              }
  //        3.若目标元素小于中间元素，则去中间元素的左边查找，使用递归的思想
              if (arr[cen] > num) {
                  return find(arr, left, cen - 1, num);
              }
  //        4.若目标元素大于中间元素，则去中间元素的右边查找，使用递归的思想
              return find(arr, cen + 1, right, num);
          }
          return -1;
      }
      public static void main(String[] args) {
          int arr[] = {1,2,3,4,5,6,7,8,9,10};
          int num = 71;
          int res = find(arr,0,arr.length - 1,num);
          if (res == -1){
              System.out.println("未找到");
          }else {
              System.out.println(res);
          }
  
      }
  }
  ```

  输出结果：

  6

#### 冒泡排序算法

- 比较相邻位置的两个元素，若第一个素比第二个元素大则交换

- 从开始的策一对元素一直到结尾的最后一对元素，经过这一轮找到了最大值并放在了最后

- 持续对越来越少的元素进行两两比较，直到所有元素不再发生交换为止

- 示例：

  ```java
  public class Test {
      public static void find(int[] arr) {
  //        1.使用外层for循环用于控制比较的轮数
          for (int i = 0; i < arr.length - 1; i++){
              //2.使用内层for循环用于控制当前轮中比较的次数，也就是元素的下标范围
              boolean flag = true;//用于判断是否进行下一轮比较
              for (int j = 0; j < arr.length - 1 - i; j++){
                  //3.若第一个元素比第二个元素大，则交换两个元素的位置
                  if (arr[j] > arr[j+1]){
                      int temp = arr[j];
                      arr[j] = arr[j+1];
                      arr[j+1] = temp;
                      flag = false;//本轮没有进行交换，则说明数组已经有序，可以结束排序
                  }
              }
              if (flag){
                  break;//提前结束排序
              }
          }
      }
  
      public static void main(String[] args) {
          int[] arr = {1, 22, 13, -4, 5};
          find(arr);
          for (int i = 0; i < arr.length; i++){
              System.out.println(arr[i]);
          }
      }
  }
  ```

  输出结果：

  -4
  1
  5
  13
  22



## 1. 在线考试设计及示例



#### 1.1 在线考试系统的实现

```java
import java.util.Scanner;
//用于获取输入,工具类
public class MyScanner {
    private static Scanner sc = new Scanner(System.in);
    public static Scanner getSc() {
        return sc;
    }
    public static void closeSc() {
        sc.close();
    }
}
```

```JAVA
//客户端界面
public class ClientView {
    private ClientViewLogic cvl;

    public ClientView(ClientViewLogic cvl) {
        this.cvl = cvl;
    }

    public void showClientView(){
        while (true){
            System.out.println("===================================");
            System.out.println("1.学员登录");
            System.out.println("2.管理员登录");
            System.out.println("0.退出系统");
            System.out.print("请选择：");
            int choice = MyScanner.getSc().nextInt();
            switch ( choice){
                case 1:
                    System.out.println("学员登录");
                    break;
                case 2:
                    cvl.managerViewLogin();
                    break;
                case 0:
                    System.out.println("退出系统");
                    return;
                default:
                    System.out.println("输入错误");
            }
        }
    }
}
```

```java
import java.io.IOException;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;
import java.net.InetAddress;
import java.net.Socket;
// 客户端初始化关闭
public class ClientInitClose {
    private Socket s;
    private ObjectOutputStream oos;
    private ObjectInputStream ois;
    public ObjectOutputStream getOos() {
        return oos;
    }
    public ObjectInputStream getOis() {
        return ois;
    }
    public Socket getS() {
        return s;
    }
    public void clientInit(){
//    自定义成员方法实现服务器的初始化工作
        try {
            s = new Socket(InetAddress.getLocalHost(), 8888);
            System.out.println("连接服务端成功！");
            oos = new ObjectOutputStream(s.getOutputStream());
            ois = new ObjectInputStream(s.getInputStream());
        } catch (IOException e) {
            throw new RuntimeException(e);
        }

    }
//    自定义成员方法实现服务器的关闭操作
    public void clientClose(){
        try {
            s.close();
        } catch (IOException e) {
            throw new RuntimeException(e);
        }
        System.out.println("客户端已关闭...");
    }
}
```

```java
// 客户端启动类
public class ClientMain {
    public static void main(String[] args) {
        ClientInitClose cic = new ClientInitClose();
        cic.clientInit();

        //声明
        ClientManagerView cmv = new ClientManagerView();
        ClientViewLogic cvl = new ClientViewLogic(cic,cmv);
        ClientView cv = new ClientView(cvl);
        cv.showClientView();
    }
}
```

```java
import java.io.IOException;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;
import java.net.ServerSocket;
import java.net.Socket;
// 服务器初始化关闭类
public class ServerInitClose {
    private ServerSocket ss;
    private Socket s;
    private ObjectInputStream ois;
    private ObjectOutputStream oos;
    public ObjectOutputStream getOos() {
        return oos;
    }
    public ObjectInputStream getOis() {
        return ois;
    }
    public Socket getS() {
        return s;
    }

//    自定义成员方法实现服务器的初始化工作
    public void serverInit(){
        try {
//        1.创建Serversocket类型的对象并提供端口号
            ss = new ServerSocket(8888);
//        2.等待客户端的连接请求，调用accept方法
            System.out.println("等待客户端的连接请求...");
            s = ss.accept();
            ois = new ObjectInputStream(s.getInputStream());
            oos = new ObjectOutputStream(s.getOutputStream());
//        3.使用输入输出流进行通信

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
//
    public  void serverClose(){
        try {
            s.close();
            ss.close();
        } catch (IOException e) {
            throw new RuntimeException(e);
        }
        System.out.println("服务器已关闭...");
    }
}
```

```java
// 服务器启动类
public class ServerMain {
    public static void main(String[] args) {
//      声明serverInitclose类型的引用指向该类型的对象
        ServerInitClose sic = new ServerInitClose();
//      调用成员方法实现服务器的初始化工作
        sic.serverInit();

        ServerDao sd = new ServerDao();
//        接收客户端发来的数据内容
        ServerLogic sl = new ServerLogic(sic,sd);
        sl.receiveClient();
    }
}
```

```java
//客户端逻辑层
public class ClientViewLogic {
    private ClientInitClose cic;
    private ClientManagerView cmv;

    public ClientViewLogic(ClientInitClose cic,ClientManagerView cmv) {
        this.cic = cic;
        this.cmv = cmv;
    }

    //    自定义成员方法实现管理员登录的业务处理
    public void managerViewLogin(){
        try {
            System.out.println("请输入账号和密码");
            String userName = MyScanner.getSc().next();
            String password = MyScanner.getSc().next();
            System.out.println("用户名："+userName);
            System.out.println("密码："+password);

    //        使用输出流将账户信息和代表功能的类型组成一个对象发送给服务器
            CommunicateMessage cm = new CommunicateMessage("managerCheck", new Manager(userName,password));
            cic.getOos().writeObject(cm);
            System.out.println("客户端发送对象成功！");

//            使用输入流读取服务器回发的处理结果
            CommunicateMessage cm2 = (CommunicateMessage) cic.getOis().readObject();
            if (cm2.getType().equals("success")){
                System.out.println("登录成功！");
            }else {
                System.out.println("登录失败！");
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

```java
//服务器逻辑类
public class ServerLogic {
    private ServerInitClose sic;
    private ServerDao sd;

    public ServerLogic(ServerInitClose sic,ServerDao sd) {
        this.sic = sic;
        this.sd = sd;
    }
    //    自定义成员方法实现对客户端发来的对象进行接收
    public void receiveClient() {
        try {
            CommunicateMessage cm = (CommunicateMessage) sic.getOis().readObject();
            System.out.println("客户端发来的数据为："+cm);
            boolean res = sd.managerCheckDao(cm.getManager());
            if (res){
                cm.setType("success");
            }else {
                cm.setType("failed");
            }
//            使用对象输出流将检验完毕的对象回发给客户端
            sic.getOos().writeObject(cm);
        } catch (Exception e) {
            throw new RuntimeException(e);
        }
//        接收客户端发来的对象并打印出来
    }
}
```

```java
//用于判断账号密码
public class ServerDao {
    public boolean managerCheckDao(Manager mg){
        if (mg.getUserName().equals("admin") && mg.getPassword().equals("123456")){
            return true;
        }
        return false;
    }
}
```

下面两个为传递消息的类

```java
import java.io.Serializable;
// 通信信息
public class CommunicateMessage implements Serializable {
    private static final long serialVersionUID = 1L;// 序列化
    private String type;
    private Manager manager;
    public CommunicateMessage(String type, Manager manager) {
        super();
        this.type = type;
        this.manager = manager;
    }
    public CommunicateMessage() {
        super();
    }
    public String getType() {
        return type;
    }
    public void setType(String type) {
        this.type = type;
    }
    public Manager getManager() {
        return manager;
    }
    public void setManager(Manager manager) {
        this.manager = manager;
    }
    @Override
    public String toString() {
        return "CommunicateMessage{" +
                "type='" + type + '\'' +
                ", manager=" + manager +
                '}';
    }
}
```

```java
import java.io.Serializable;
// 通信信息类，用于传输账户信息
public class Manager implements Serializable {
    private static final long serialVersionUID = 1L;// 序列化
    private String userName;
    private String password;
    public Manager() {
        super();
    }
    public Manager(String userName, String password) {
        super();
        this.userName = userName;
        this.password = password;
    }
    public String getUserName() {
        return userName;
    }
    public void setUserName(String userName) {
        this.userName = userName;
    }
    public String getPassword() {
        return password;
    }
    public void setPassword(String password) {
        this.password = password;
    }
    @Override
    public String toString() {
        return "Manager{" +
                "userName='" + userName + '\'' +
                ", password='" + password + '\'' +
                '}';
    }
}
```



