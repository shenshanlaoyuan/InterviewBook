# Java面试宝典

## 1.基础篇

### 1.1.面向对象

#### 1.1.1.什么是面向对象

面向对象、面向过程

面向对象的三大基本特征和五大基本原则

#### 1.1.2.平台无关性

Java 如何实现的平台无关

JVM 还支持哪些语言（Kotlin、Groovy、JRuby、Jython、Scala）

#### 1.1.3.值传递

值传递、引用传递

为什么说 Java 中只有值传递

#### 1.1.4.封装、继承、多态

什么是多态、方法重写与重载

Java 的继承与实现

构造函数与默认构造函数

类变量、成员变量和局部变量

成员变量和方法作用域

### 1.2.Java基础知识

#### 1.2.1.基本数据类型

8 种基本数据类型：整型、浮点型、布尔型、字符型

整型中 byte、short、int、long 的取值范围

什么是浮点型？什么是单精度和双精度？为什么不能用浮点型表示金额？

#### 1.2.2. 自动拆装箱

什么是包装类型、什么是基本类型、什么是自动拆装箱

Integer 的缓存机制

#### 1.2.3.String

字符串的不可变性

JDK 6 和 JDK 7 中 substring 的原理及区别、

replaceFirst、replaceAll、replace 区别、

String 对“+”的重载、字符串拼接的几种方式和区别

String.valueOf 和 Integer.toString 的区别、

switch 对 String 的支持

字符串池、常量池（运行时常量池、Class 常量池）、intern

#### 1.2.4.熟悉 Java 中各种关键字

transient、instanceof、final、static、volatile、synchronized、const 原理及用法

#### 1.2.5.集合类

常用集合类的使用、ArrayList 和 LinkedList 和 Vector 的区别 、SynchronizedList 和 Vector 的区别、HashMap、HashTable、ConcurrentHashMap 区别、

Set 和 List 区别？Set 如何保证元素不重复？

Java 8 中 stream 相关用法、apache 集合处理工具类的使用、不同版本的 JDK 中 HashMap 的实现的区别以及原因

Collection 和 Collections 区别

Arrays.asList 获得的 List 使用时需要注意什么

Enumeration 和 Iterator 区别

fail-fast 和 fail-safe

CopyOnWriteArrayList、ConcurrentSkipListMap

#### 1.2.6.枚举

枚举的用法、枚举的实现、枚举与单例、Enum 类

Java 枚举如何比较

switch 对枚举的支持

枚举的序列化如何实现

枚举的线程安全性问题

#### 1.2.7.IO

字符流、字节流、输入流、输出流、

同步、异步、阻塞、非阻塞、Linux 5 种 IO 模型

BIO、NIO 和 AIO 的区别、三种 IO 的用法与原理、netty

#### 1.2.8.反射

反射与工厂模式、反射有什么用

Class 类、java.lang.reflect.*

#### 1.2.9.动态代理

静态代理、动态代理

动态代理和反射的关系

动态代理的几种实现方式

AOP

#### 1.2.10.序列化

什么是序列化与反序列化、为什么序列化、序列化底层原理、序列化与单例模式、protobuf、为什么说序列化并不安全

#### 1.2.11.注解

元注解、自定义注解、Java 中常用注解使用、注解与反射的结合

Spring 常用注解

#### 1.2.12.JMS

什么是 Java 消息服务、JMS 消息传送模型

#### 1.2.13.JMX

java.lang.management.*、 javax.management.*

#### 1.2.14.泛型

泛型与继承、类型擦除、泛型中 KTVE? object 等的含义、泛型各种用法

限定通配符和非限定通配符、上下界限定符 extends 和 super

List<Object> 和原始类型 List 之间的区别? 

List<?> 和 List<Object> 之间的区别是什么?

#### 1.2.15.单元测试

junit、mock、mockito、内存数据库（h2）

#### 1.2.16.正则表达式

java.lang.util.regex.*

#### 1.2.17.常用的 Java 工具库

commons.lang、commons.*...、 guava-libraries、 netty

#### 1.2.18.API & SPI

API、API 和 SPI 的关系和区别

如何定义 SPI、SPI 的实现原理

#### 1.2.19.异常

异常类型、正确处理异常、自定义异常

Error 和 Exception

异常链、try-with-resources

finally 和 return 的执行顺序

#### 1.2.20.时间处理

时区、冬令时和夏令时、时间戳、Java 中时间 API

格林威治时间、CET,UTC,GMT,CST 几种常见时间的含义和关系

SimpleDateFormat 的线程安全性问题

Java 8 中的时间处理

如何在东八区的计算机上获取美国时间

#### 1.2.21.编码方式

Unicode、有了 Unicode 为啥还需要 UTF-8

GBK、GB2312、GB18030 之间的区别

UTF8、UTF16、UTF32 区别

URL 编解码、Big Endian 和 Little Endian

如何解决乱码问题

#### 1.2.22.语法糖

Java 中语法糖原理、解语法糖

语法糖：switch 支持 String 与枚举、泛型、自动装箱与拆箱、方法变长参数、枚举、内部类、条件编译、 断言、数值字面量、for-each、try-with-resource、Lambda 表达式

### 1.3.阅读源代码

String、Integer、Long、Enum、

BigDecimal、ThreadLocal、ClassLoader & URLClassLoader、

ArrayList & LinkedList、 

HashMap & LinkedHashMap & TreeMap & CouncurrentHashMap、HashSet & LinkedHashSet & TreeSet

### 1.4.Java并发编程

#### 1.4.1.并发与并行

什么是并发、什么是并行

并发与并行的区别

#### 1.4.2.什么是线程，与进程的区别

线程的实现、线程的状态、优先级、线程调度、创建线程的多种方式、守护线程

线程与进程的区别

#### 1.4.3.线程池

自己设计线程池、submit() 和 execute()、线程池原理

为什么不允许使用 Executors 创建线程池

#### 1.4.4.线程安全

死锁、死锁如何排查、线程安全和内存模型的关系

#### 1.4.5.锁

CAS、乐观锁与悲观锁、数据库相关锁机制、分布式锁、偏向锁、轻量级锁、重量级锁、monitor、

锁优化、锁消除、锁粗化、自旋锁、可重入锁、阻塞锁、死锁

#### 1.4.6.死锁

什么是死锁

死锁如何解决

#### 1.4.7.synchronized

synchronized 是如何实现的？

synchronized 和 lock 之间关系、不使用 synchronized 如何实现一个线程安全的单例

synchronized 和原子性、可见性和有序性之间的关系

#### 1.4.8.volatile

happens-before、内存屏障、编译器指令重排和 CPU 指令重

volatile 的实现原理

volatile 和原子性、可见性和有序性之间的关系

有了 symchronized 为什么还需要 volatile

#### 1.4.9.sleep 和 wait

#### 1.4.10.wait 和 notify

#### 1.4.11.notify 和 notifyAll

#### 1.4.12.ThreadLocal

#### 1.4.13.写一个死锁的程序

#### 1.4.14.写代码来解决生产者消费者问题

#### 1.4.15.并方包

Thread、Runnable、Callable、ReentrantLock、ReentrantReadWriteLock、Atomic*、Semaphore、CountDownLatch、ConcurrentHashMap、Executors

## 2.底层篇

### 2.1.JVM

#### 2.1.1.JVM 内存结构

class 文件格式、运行时数据区：堆、栈、方法区、直接内存、运行时常量池、

堆和栈区别

Java 中的对象一定在堆上分配吗？

#### 2.1.2.Java 内存模型

计算机内存模型、缓存一致性、MESI 协议

可见性、原子性、顺序性、happens-before、

内存屏障、synchronized、volatile、final、锁

#### 2.1.3.垃圾回收

GC 算法：标记清除、引用计数、复制、标记压缩、分代回收、增量式回收

GC 参数、对象存活的判定、垃圾收集器（CMS、G1、ZGC、Epsilon）

#### 2.1.4.JVM 参数及调优

-Xmx、-Xmn、-Xms、Xss、-XX:SurvivorRatio、

-XX:PermSize、-XX:MaxPermSize、-XX:MaxTenuringThreshold

#### 2.1.5.Java 对象模型

oop-klass、对象头

#### 2.1.6.HotSpot

即时编译器、编译优化

#### 2.1.7.虚拟机性能监控与故障处理工具

jps, jstack, jmap, jstat, jconsole, jinfo, jhat, javap, btrace, TProfiler

Arthas

### 2.2.类加载机制

classLoader、类加载过程、双亲委派（破坏双亲委派）、模块化（jboss modules、osgi、jigsaw）

### 2.3.编译与反编译

什么是编译（前端编译、后端编译）、什么是反编译

JIT、JIT 优化（逃逸分析、栈上分配、标量替换、锁优化）

编译工具：javac

反编译工具：javap 、jad 、CRF

## 3.进阶篇

### 3.1.Java 底层知识

### 3.2.设计模式

### 3.3.网络编程知识

### 3.4.框架知识

### 3.5.应用服务器知识

### 3.6.工具

## 4.高级篇

### 4.1.新技术

### 4.2.性能优化

### 4.3.线上问题分析

### 4.4.编译原理知识

### 4.5.操作系统知识

### 4.6.数据库知识

### 4.7.数据结构与算法知识

### 4.8.大数据知识

### 4.9.网络安全知识

## 5.架构篇

### 5.1.分布式

### 5.2.微服务

### 5.3.高并发

### 5.4. 监控

### 5.5.负载均衡

### 5.6.DNS

### 5.7.CDN

## 6.扩展篇






