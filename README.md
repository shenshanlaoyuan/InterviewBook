# Java面试宝典

很多人面试之前没什么准备，也不知道从哪里开始复习，然而机会往往是给有准备的人。笔者根据多年工作经验，整理一份面试宝典，帮助大家快速突击复习和巩固面试常问的技术点，面试拿到心仪的offer。

# [1.基础篇](基础篇/README.md)

## [1.1.面向对象](基础篇/面向对象/README.md)

### [1.1.1.什么是面向对象](基础篇/面向对象/什么是面向对象.md)

面向对象、面向过程

面向对象的三大基本特征和五大基本原则

### [1.1.2.平台无关性](基础篇/面向对象/平台无关性.md)

Java 如何实现的平台无关

JVM 还支持哪些语言（Kotlin、Groovy、JRuby、Jython、Scala）

### [1.1.3.值传递](基础篇/面向对象/值传递.md)

值传递、引用传递

为什么说 Java 中只有值传递

### [1.1.4.封装、继承、多态](基础篇/面向对象/封装继承多态.md)

什么是多态、方法重写与重载

Java 的继承与实现

构造函数与默认构造函数

类变量、成员变量和局部变量

成员变量和方法作用域

## [1.2.Java基础知识](基础篇/基础知识/README.md)

### [1.2.1.基本数据类型](基础篇/基础知识/基本数据类型.md)

8 种基本数据类型：整型、浮点型、布尔型、字符型

整型中 byte、short、int、long 的取值范围

什么是浮点型？什么是单精度和双精度？为什么不能用浮点型表示金额？

### [1.2.2. 自动拆装箱](基础篇/基础知识/自动拆装箱.md)

什么是包装类型、什么是基本类型、什么是自动拆装箱

Integer 的缓存机制

### [1.2.3.String](基础篇/基础知识/String.md)

字符串的不可变性

JDK 6 和 JDK 7 中 substring 的原理及区别、

replaceFirst、replaceAll、replace 区别、

String 对“+”的重载、字符串拼接的几种方式和区别

String.valueOf 和 Integer.toString 的区别、

switch 对 String 的支持

字符串池、常量池（运行时常量池、Class 常量池）、intern

### [1.2.4.熟悉 Java 中各种关键字](基础篇/基础知识/熟悉Java中各种关键字.md)

transient、instanceof、final、static、volatile、synchronized、const 原理及用法

### [1.2.5.集合类](基础篇/基础知识/集合类.md)

常用集合类的使用、ArrayList 和 LinkedList 和 Vector 的区别 、SynchronizedList 和 Vector 的区别、HashMap、HashTable、ConcurrentHashMap 区别、

Set 和 List 区别？Set 如何保证元素不重复？

Java 8 中 stream 相关用法、apache 集合处理工具类的使用、不同版本的 JDK 中 HashMap 的实现的区别以及原因

Collection 和 Collections 区别

Arrays.asList 获得的 List 使用时需要注意什么

Enumeration 和 Iterator 区别

fail-fast 和 fail-safe

CopyOnWriteArrayList、ConcurrentSkipListMap

### [1.2.6.枚举](基础篇/基础知识/枚举.md)

枚举的用法、枚举的实现、枚举与单例、Enum 类

Java 枚举如何比较

switch 对枚举的支持

枚举的序列化如何实现

枚举的线程安全性问题

### [1.2.7.IO](基础篇/基础知识/IO.md)

字符流、字节流、输入流、输出流、

同步、异步、阻塞、非阻塞、Linux 5 种 IO 模型

BIO、NIO 和 AIO 的区别、三种 IO 的用法与原理、netty

### [1.2.8.反射](基础篇/基础知识/反射.md)

反射与工厂模式、反射有什么用

Class 类、java.lang.reflect.*

### [1.2.9.动态代理](基础篇/基础知识/动态代理.md)

静态代理、动态代理

动态代理和反射的关系

动态代理的几种实现方式

AOP

### [1.2.10.序列化](基础篇/基础知识/序列化.md)

什么是序列化与反序列化、为什么序列化、序列化底层原理、序列化与单例模式、protobuf、为什么说序列化并不安全

### [1.2.11.注解](基础篇/基础知识/注解.md)

元注解、自定义注解、Java 中常用注解使用、注解与反射的结合

Spring 常用注解

### [1.2.12.JMS](基础篇/基础知识/JMS.md)

什么是 Java 消息服务、JMS 消息传送模型

### [1.2.13.JMX](基础篇/基础知识/JMX.md)

java.lang.management.*、 javax.management.*

### [1.2.14.泛型](基础篇/基础知识/泛型.md)

泛型与继承、类型擦除、泛型中 KTVE? object 等的含义、泛型各种用法

限定通配符和非限定通配符、上下界限定符 extends 和 super

List<Object> 和原始类型 List 之间的区别? 

List<?> 和 List<Object> 之间的区别是什么?

### [1.2.15.单元测试](基础篇/基础知识/单元测试.md)

junit、mock、mockito、内存数据库（h2）

### [1.2.16.正则表达式](基础篇/基础知识/正则表达式.md)

java.lang.util.regex.*

### [1.2.17.常用的 Java 工具库](基础篇/基础知识/常用的Java工具库.md)

commons.lang、commons.*...、 guava-libraries、 netty

### [1.2.18.API & SPI](基础篇/基础知识/API&SPI.md)

API、API 和 SPI 的关系和区别

如何定义 SPI、SPI 的实现原理

### [1.2.19.异常](基础篇/基础知识/异常.md)

异常类型、正确处理异常、自定义异常

Error 和 Exception

异常链、try-with-resources

finally 和 return 的执行顺序

### [1.2.20.时间处理](基础篇/基础知识/时间处理.md)

时区、冬令时和夏令时、时间戳、Java 中时间 API

格林威治时间、CET,UTC,GMT,CST 几种常见时间的含义和关系

SimpleDateFormat 的线程安全性问题

Java 8 中的时间处理

如何在东八区的计算机上获取美国时间

### [1.2.21.编码方式](基础篇/基础知识/编码方式.md)

Unicode、有了 Unicode 为啥还需要 UTF-8

GBK、GB2312、GB18030 之间的区别

UTF8、UTF16、UTF32 区别

URL 编解码、Big Endian 和 Little Endian

如何解决乱码问题

### [1.2.22.语法糖](基础篇/基础知识/语法糖.md)

Java 中语法糖原理、解语法糖

语法糖：switch 支持 String 与枚举、泛型、自动装箱与拆箱、方法变长参数、枚举、内部类、条件编译、 断言、数值字面量、for-each、try-with-resource、Lambda 表达式

## [1.3.阅读源代码](基础篇/阅读源代码/README.md)

String、Integer、Long、Enum、

BigDecimal、ThreadLocal、ClassLoader & URLClassLoader、

ArrayList & LinkedList、 

HashMap & LinkedHashMap & TreeMap & CouncurrentHashMap、HashSet & LinkedHashSet & TreeSet

## [1.4.Java并发编程](基础篇/Java并发编程/README.md)

### [1.4.1.并发与并行](基础篇/Java并发编程/并发与并行.md)

什么是并发、什么是并行

并发与并行的区别

### [1.4.2.什么是线程，与进程的区别](基础篇/Java并发编程/什么是线程，与进程的区别.md)

线程的实现、线程的状态、优先级、线程调度、创建线程的多种方式、守护线程

线程与进程的区别

### [1.4.3.线程池](基础篇/Java并发编程/线程池.md)

自己设计线程池、submit() 和 execute()、线程池原理

为什么不允许使用 Executors 创建线程池

### [1.4.4.线程安全](基础篇/Java并发编程/线程安全.md)

死锁、死锁如何排查、线程安全和内存模型的关系

### [1.4.5.锁](基础篇/Java并发编程/锁.md)

CAS、乐观锁与悲观锁、数据库相关锁机制、分布式锁、偏向锁、轻量级锁、重量级锁、monitor、

锁优化、锁消除、锁粗化、自旋锁、可重入锁、阻塞锁、死锁

### [1.4.6.死锁](基础篇/Java并发编程/死锁.md)

什么是死锁

死锁如何解决

### [1.4.7.synchronized](基础篇/Java并发编程/synchronized.md)

synchronized 是如何实现的？

synchronized 和 lock 之间关系、不使用 synchronized 如何实现一个线程安全的单例

synchronized 和原子性、可见性和有序性之间的关系

### [1.4.8.volatile](基础篇/Java并发编程/volatile.md)

happens-before、内存屏障、编译器指令重排和 CPU 指令重

volatile 的实现原理

volatile 和原子性、可见性和有序性之间的关系

有了 symchronized 为什么还需要 volatile

### [1.4.9.sleep 和 wait](基础篇/Java并发编程/sleep和wait.md)

### [1.4.10.wait 和 notify](基础篇/Java并发编程/wait和notify.md)

### [1.4.11.notify 和 notifyAll](基础篇/Java并发编程/notify和notifyAll.md)

### [1.4.12.ThreadLocal](基础篇/Java并发编程/ThreadLocal.md)

### [1.4.13.写一个死锁的程序](基础篇/Java并发编程/写一个死锁的程序.md)

### [1.4.14.写代码来解决生产者消费者问题](基础篇/Java并发编程/写代码来解决生产者消费者问题.md)

### [1.4.15.并方包](基础篇/Java并发编程/并方包.md)

Thread、Runnable、Callable、ReentrantLock、ReentrantReadWriteLock、Atomic*、Semaphore、CountDownLatch、ConcurrentHashMap、Executors

# [2.底层篇](底层篇/README.md)

## [2.1.JVM](底层篇/JVM/README.md)

### [2.1.1.JVM 内存结构](底层篇/JVM/JVM内存结构.md)

class 文件格式、运行时数据区：堆、栈、方法区、直接内存、运行时常量池、

堆和栈区别

Java 中的对象一定在堆上分配吗？

### [2.1.2.Java 内存模型](底层篇/JVM/Java内存模型.md)

计算机内存模型、缓存一致性、MESI 协议

可见性、原子性、顺序性、happens-before、

内存屏障、synchronized、volatile、final、锁

### [2.1.3.垃圾回收](底层篇/JVM/垃圾回收.md)

GC 算法：标记清除、引用计数、复制、标记压缩、分代回收、增量式回收

GC 参数、对象存活的判定、垃圾收集器（CMS、G1、ZGC、Epsilon）

### [2.1.4.JVM 参数及调优](底层篇/JVM/JVM参数及调优.md)

-Xmx、-Xmn、-Xms、Xss、-XX:SurvivorRatio、

-XX:PermSize、-XX:MaxPermSize、-XX:MaxTenuringThreshold

### [2.1.5.Java 对象模型](底层篇/JVM/Java对象模型.md)

oop-klass、对象头

### [2.1.6.HotSpot](底层篇/JVM/HotSpot.md)

即时编译器、编译优化

### [2.1.7.虚拟机性能监控与故障处理工具](底层篇/JVM/虚拟机性能监控与故障处理工具.md)

jps, jstack, jmap, jstat, jconsole, jinfo, jhat, javap, btrace, TProfiler

Arthas

## [2.2.类加载机制](底层篇/类加载机制/README.md)

classLoader、类加载过程、双亲委派（破坏双亲委派）、模块化（jboss modules、osgi、jigsaw）

## [2.3.编译与反编译](底层篇/编译与反编译/README.md)

什么是编译（前端编译、后端编译）、什么是反编译

JIT、JIT 优化（逃逸分析、栈上分配、标量替换、锁优化）

编译工具：javac

反编译工具：javap 、jad 、CRF

# [3.进阶篇](进阶篇/README.md)

## [3.1.Java 底层知识](进阶篇/Java底层知识/README.md)

### 3.1.1.字节码、class 文件格式

### 3.1.2.CPU 缓存，L1，L2，L3 和伪共享

### 3.1.3.尾递归

### 3.1.4.位运算

用位运算实现加、减、乘、除、取余

## [3.2.设计模式](进阶篇/设计模式/README.md)

设计模式的六大原则：

开闭原则（Open Close Principle）、里氏代换原则（Liskov Substitution Principle）、依赖倒转原则（Dependence Inversion Principle）

接口隔离原则（Interface Segregation Principle）、迪米特法则（最少知道原则）（Demeter Principle）、合成复用原则（Composite Reuse Principle）

### 3.2.1.了解 23 种设计模式

创建型模式：单例模式、抽象工厂模式、建造者模式、工厂模式、原型模式。

结构型模式：适配器模式、桥接模式、装饰模式、组合模式、外观模式、享元模式、代理模式。

行为型模式：模版方法模式、命令模式、迭代器模式、观察者模式、中介者模式、备忘录模式、解释器模式（Interpreter 模式）、状态模式、策略模式、职责链模式(责任链模式)、访问者模式。

### 3.2.2.会使用常用设计模式

单例的七种写法：懒汉——线程不安全、懒汉——线程安全、饿汉、饿汉——变种、静态内部类、枚举、双重校验锁

工厂模式、适配器模式、策略模式、模板方法模式、观察者模式、外观模式、代理模式等必会

### 3.2.3.实现线程安全的单例模式

不用 synchronized 和 lock

### 3.2.4.实现 AOP

### 3.2.5.实现 IOC

### 3.2.6.nio 和 reactor 设计模式

## [3.3.网络编程知识](进阶篇/网络编程知识/README.md)

### 3.3.1.tcp、udp、http、https 等常用协议

三次握手与四次关闭、流量控制和拥塞控制、OSI 七层模型、tcp 粘包与拆包

### 3.3.2.http/1.0 http/1.1 http/2 之前的区别

http 中 get 和 post 区别

常见的 web 请求返回的状态码

404、302、301、500分别代表什么

### 3.3.3.http/3

### 3.3.4.Java RMI，Socket，HttpClient

### 3.3.5. cookie 与 session

cookie 被禁用，如何实现 session

### 3.3.6.用 Java 写一个简单的静态文件的 HTTP 服务器

### 3.3.7.了解 nginx 和 apache 服务器的特性

并搭建一个对应的服务器

### 3.3.8.用 Java 实现 FTP、SMTP 协议

### 3.3.9.进程间通讯的方式

### 3.3.10.什么是 CDN？如何实现？

### 3.3.11.DNS

什么是 DNS 、记录类型: A 记录、CNAME 记录、AAAA 记录等

域名解析、根域名服务器

DNS 污染、DNS 劫持、公共 DNS：114 DNS、Google DNS、OpenDNS

### 3.3.12.反向代理

正向代理、反向代理

反向代理服务器

## [3.4.框架知识](进阶篇/框架知识/README.md)

### 3.4.1.Servlet

生命周期

线程安全问题

filter 和 listener

web.xml 中常用配置及作用

### 3.4.2.Hibernate

什么是 OR Mapping

Hibernate 的懒加载

Hibernate 的缓存机制

Hibernate / Ibatis / MyBatis 之间的区别

### 3.4.3.Spring

Bean 的初始化

AOP 原理

实现 Spring 的IOC

Spring 四种依赖注入方式

### 3.4.4.Spring MVC

什么是 MVC

Spring mvc 与 Struts mvc 的区别

### 3.4.5.Spring Boot

Spring Boot 2.0、起步依赖、自动配置、

Spring Boot 的 starter 原理，自己实现一个 starter

### 3.4.6.Spring Security

### 3.4.7.Spring Cloud

服务发现与注册：Eureka、Zookeeper、Consul

负载均衡：Feign、Spring Cloud Loadbalance

服务配置：Spring Cloud Config

服务限流与熔断：Hystrix

服务链路追踪：Dapper

服务网关、安全、消息

## [3.5.应用服务器知识](进阶篇/应用服务器知识/README.md)

### 3.5.1.JBoss

### 3.5.2.tomcat

### 3.5.3. jetty

### 3.5.4.Weblogic

## [3.6.工具](进阶篇/工具/README.md)

### 3.6.1.git & svn

### 3.6.2.maven & gradle

### 3.6.3.Intellij IDEA

常用插件：Maven Helper 、FindBugs-IDEA、阿里巴巴代码规约检测、GsonFormat

Lombok plugin、.ignore、Mybatis plugin

# [4.高级篇](高级篇/README.md)

## 4.1.新技术

### 4.1.1.Java 8

lambda 表达式、Stream API、时间 API

### 4.1.2.Java 9

Jigsaw、Jshell、Reactive Streams

### 4.1.3.Java 10

局部变量类型推断、G1 的并行 Full GC、ThreadLocal 握手机制

### 4.1.4.Java 11

ZGC、Epsilon、增强 var

### 4.1.5.Spring 5

响应式编程

### 4.1.6.Spring Boot 2.0

### 4.1.7.HTTP/2

### 4.1.8.**HTTP/3** 

## 4.2.性能优化

使用单例、使用 Future 模式、使用线程池

选择就绪、减少上下文切换、减少锁粒度、数据压缩、结果缓存

## 4.3.线上问题分析

### 4.3.1.dump 获取

线程 Dump、内存 Dump、gc 情况

### 4.3.2.dump 分析

分析死锁、分析内存泄露

### 4.3.3.dump 分析及获取工具

jstack、jstat、jmap、jhat、Arthas

### 4.3.4.自己编写各种 outofmemory，stackoverflow 程序

HeapOutOfMemory、 Young OutOfMemory、

MethodArea OutOfMemory、ConstantPool OutOfMemory、

DirectMemory OutOfMemory、Stack OutOfMemory Stack OverFlow

### 4.3.5.Arthas

jvm 相关、class/classloader 相关、monitor/watch/trace 相关、

options、管道、后台异步任务

文档：https://alibaba.github.io/arthas/advanced-use.html

### 4.3.6.常见问题解决思路

内存溢出、线程死锁、类加载冲突

### 4.3.7.使用工具尝试解决以下问题，并写下总结

当一个 Java 程序响应很慢时如何查找问题

当一个 Java 程序频繁 FullGC 时如何解决问题

如何查看垃圾回收日志

当一个 Java 应用发生 OutOfMemory 时该如何解决

如何判断是否出现死锁

如何判断是否存在内存泄露

使用 Arthas 快速排查 Spring Boot 应用404/401问题

使用 Arthas 排查线上应用日志打满问题

利用 Arthas 排查 Spring Boot 应用 NoSuchMethodError

## 4.4.编译原理知识

### 4.4.1.编译与反编译

### 4.4.2.Java 代码的编译与反编译

### 4.4.3.Java 的反编译工具

javap 、jad 、CRF

### 4.4.4.即时编译器

### 4.4.5.编译过程

词法分析，语法分析（LL 算法，递归下降算法，LR 算法）

语义分析，运行时环境，中间代码，代码生成，代码优化

## 4.5.操作系统知识

### 4.5.1.Linux 的常用命令

### 4.5.2.进程间通信

### 4.5.3.进程同步

生产者消费者问题、哲学家就餐问题、读者写者问题

### 4.5.4.缓冲区溢出

### 4.5.5.分段和分页

### 4.5.6.虚拟内存与主存

### 4.5.7.虚拟内存管理

### 4.5.8.换页算法

## 4.6.数据库知识

### 4.6.1.MySQL 执行引擎

### 4.6.2.MySQL 执行计划

如何查看执行计划，如何根据执行计划进行 SQL 优化

### 4.6.3.索引

Hash 索引、B 树索引（B+树、和B树、R树）

普通索引、唯一索引

覆盖索引、最左前缀原则、索引下推

### 4.6.4.SQL 优化

### 4.6.5.数据库事务和隔离级别

事务的隔离级别、事务能不能实现锁的功能

### 4.6.7.数据库锁

行锁、表锁、使用数据库锁实现乐观锁、

### 4.6.8.连接

内连接，左连接，右连接

### 4.6.9.数据库主备搭建

### 4.6.10.binlog

### 4.6.11.redolog

### 4.6.12.内存数据库

h2

### 4.6.13.分库分表

### 4.6.14.读写分离

### 4.6.15.常用的 NoSql 数据库

redis、memcached

### 4.6.16.分别使用数据库锁、NoSql 实现分布式锁

### 4.6.17.性能调优

### 4.6.18.数据库连接池

## 4.7.数据结构与算法知识

### 4.7.1.简单的数据结构

栈、队列、链表、数组、哈希表、

栈和队列的相同和不同之处

栈通常采用的两种存储结构

### 4.7.2.树

二叉树、字典树、平衡树、排序树、

B 树、B+ 树、R 树、多路树、红黑树

### 4.7.3.堆

大根堆、小根堆

### 4.7.4.图

有向图、无向图、拓扑

### 4.7.5.排序算法

稳定的排序：冒泡排序、插入排序、鸡尾酒排序、桶排序、计数排序、归并排序、原地归并排序、二叉排序树排序、鸽巢排序、基数排序、侏儒排序、图书馆排序、块排序

不稳定的排序：选择排序、希尔排序、Clover 排序算法、梳排序、堆排序、平滑排序、快速排序、内省排序、耐心排序

各种排序算法和时间复杂度 

### 4.7.6.两个栈实现队列，和两个队列实现栈

### 4.7.7.深度优先和广度优先搜索

### 4.7.8.全排列、贪心算法、KMP 算法、hash 算法

### 4.7.9.海量数据处理

分治，hash 映射，堆排序，双层桶划分，Bloom Filter，bitmap，数据库索引，mapreduce 等。

## 4.8.大数据知识

### 4.8.1.Zookeeper

基本概念、常见用法

### 4.8.2.Solr，Lucene，ElasticSearch

在 linux 上部署 solr，solrcloud，新增、删除、查询索引

### 4.8.3.Storm，流式计算，了解 Spark，S4

在 linux 上部署 storm，用 zookeeper 做协调，运行 storm hello world，local 和 remote 模式运行调试 storm topology。

### 4.8.4.Hadoop，离线计算

HDFS、MapReduce

### 4.8.5.分布式日志收集 flume，kafka，logstash

### 4.8.6.数据挖掘，mahout

## 4.9.网络安全知识

### 4.9.1.XSS

XSS 的防御

### 4.9.2.CSRF

### 4.9.3.注入攻击

SQL 注入、XML 注入、CRLF 注入

### 4.9.4.文件上传漏洞

### 4.9.5.加密与解密

对称加密、非对称加密、哈希算法、加盐哈希算法

MD5，SHA1、DES、AES、RSA、DSA

彩虹表

### 4.9.6.DDOS攻击

DOS 攻击、DDOS 攻击

memcached 为什么可以导致 DDos 攻击、什么是反射型 DDoS

如何通过 Hash 碰撞进行 DOS 攻击

### 4.9.7.SSL、TLS，HTTPS

### 4.9.8.用 openssl 签一个证书部署到 apache 或 nginx



# [5.架构篇](架构篇/README.md)

## 5.1.分布式

数据一致性、服务治理、服务降级

### 5.1.1.分布式事务

2PC、3PC、CAP、BASE、 可靠消息最终一致性、最大努力通知、TCC

### 5.1.2.Dubbo

服务注册、服务发现，服务治理

http://dubbo.apache.org/zh-cn/

### 5.1.3.分布式数据库

怎样打造一个分布式数据库、什么时候需要分布式数据库、

mycat、otter、HBase

### 5.1.4.分布式文件系统

mfs、fastdfs

### 5.1.5.分布式缓存

缓存一致性、缓存命中率、缓存冗余

### 5.1.6.限流降级

Hystrix、Sentinal

### 5.1.7.算法

共识算法、Raft 协议、Paxos 算法与 Raft 算法、

拜占庭问题与算法、2PC、3PC

## 5.2.微服务

SOA、康威定律

### 5.2.1.ServiceMesh

sidecar

### 5.2.2.Docker & Kubernets

### 5.2.3.Spring Boot

### 5.2.4.Spring Cloud

## 5.3.高并发

### 5.3.1.分库分表

### 5.3.2.CDN 技术

### 5.3.3.消息队列

ActiveMQ

## 5.4. 监控

### 5.4.1.监控什么

CPU、内存、磁盘 I/O、网络 I/O 等

### 5.4.2.监控手段

进程监控、语义监控、机器资源监控、数据波动

### 5.4.3.监控数据采集

日志、埋点

### 5.4.4.Dapper

## 5.5.负载均衡

tomcat 负载均衡、Nginx 负载均衡

四层负载均衡、七层负载均衡

## 5.6.DNS

DNS 原理、DNS 的设计

## 5.7.CDN

数据一致性

# [6.扩展篇](扩展篇/README.md)

## 6.1.云计算

IaaS、SaaS、PaaS、虚拟化技术、openstack、Serverlsess

## 6.2.搜索引擎

Solr、Lucene、Nutch、Elasticsearch

## 6.3.权限管理

Shiro

## 6.4.区块链

哈希算法、Merkle 树、公钥密码算法、共识算法、

Raft 协议、Paxos 算法与 Raft 算法、拜占庭问题与算法、消息认证码与数字签名

### 比特币

挖矿、共识机制、闪电网络、侧链、热点问题、分叉

### 以太坊

### 超级账本

## 6.5.人工智能

数学基础、机器学习、人工神经网络、深度学习、应用场景。

### 常用框架

TensorFlow、DeepLearning4J








