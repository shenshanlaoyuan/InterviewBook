# String

## 1. 字符串的不可变性

这里有一组图片来说明Java字符串的不可变性。

### 声明一个字符串

以下代码初始化了一个字符串s.

```java
String s = "abcd";
```

如下所示，变量s储存了一个字符串对象的引用。箭头可以被当做“储存引用”。

![String-Immutability-1.jpeg](https://i.loli.net/2019/06/17/5d074e22beae448963.jpeg)

### 将一个字符串变量分配给另一个字符串变量

下面代码将s分配给了s2.

```java
String s2 = s;
```

s2储存了一个相同的引用值，因为它是同一个字符串对象。

![String-Immutability-2.jpeg](https://i.loli.net/2019/06/17/5d074f4b1c45192435.jpeg)

### 合并字符串

当我们合并一个字符串”ef”到s，

```java
s = s.concat("ef");
```

如下所示，s存储新创建的字符串对象的引用：

![string-immutability-650x279.jpeg](https://i.loli.net/2019/06/17/5d074f4b1a52e14825.jpeg)

### 总结

综上所述： 一旦在内存（堆）中创建了一个字符串，它就不能被改变。所有字符串的方法都没有去改变字符串自己，而是返回了一个新对象。

如果我们需要一个可以修改的字符串，我们将需要使用**StringBuffer** 或 **StringBuilder**. 否则，垃圾收集会浪费大量时间，因为每次创建一个新的字符串。

## 2. JDK 6 和 JDK 7 中 substring 的原理及区别

`substring(int beginIndex, int endIndex)`方法在不同版本的JDK中的实现是不同的。了解他们的区别可以帮助你更好的使用他。为简单起见，后文中用`substring()`代表`substring(int beginIndex, int endIndex)`方法。

### substring() 的作用

`substring(int beginIndex, int endIndex)`方法截取字符串并返回其[beginIndex,endIndex-1]范围内的内容。

```java
String x = "abcdef";
x = x.substring(1,3);
System.out.println(x);
```

输出内容：

```java
bc
```

### 调用substring()时发生了什么？

你可能知道，因为x是不可变的，当使用`x.substring(1,3)`对x赋值的时候，它会指向一个全新的字符串：

![string-immutability1-650x303.jpeg](https://i.loli.net/2019/06/19/5d0996bbc35ca73080.jpeg)

然而，这个图不是完全正确的表示堆中发生的事情。因为在jdk6 和 jdk7中调用substring时发生的事情并不一样。

### JDK 6中的substring

String是通过字符数组实现的。在jdk 6 中，String类包含三个成员变量：`char value[]`， `int offset`，`int count`。他们分别用来存储真正的字符数组，数组的第一个位置索引以及字符串中包含的字符个数。

当调用substring方法的时候，会创建一个新的string对象，但是这个string的值仍然指向堆中的同一个字符数组。这两个对象中只有count和offset 的值是不同的。

![string-substring-jdk6-650x389.jpeg](https://i.loli.net/2019/06/19/5d099734d54df52875.jpeg)

下面是证明上说观点的Java源码中的关键代码：

```java
//JDK 6
String(int offset, int count, char value[]) {
    this.value = value;
    this.offset = offset;
    this.count = count;
}

public String substring(int beginIndex, int endIndex) {
    //check boundary
    return  new String(offset + beginIndex, endIndex - beginIndex, value);
}
```

### JDK 6中的substring导致的问题

如果你有一个很长很长的字符串，但是当你使用substring进行切割的时候你只需要很短的一段。这可能导致性能问题，因为你需要的只是一小段字符序列，但是你却引用了整个字符串（因为这个非常长的字符数组一直在被引用，所以无法被回收，就可能导致内存泄露）。在JDK 6中，一般用以下方式来解决该问题，原理其实就是生成一个新的字符串并引用他。

```java
x = x.substring(x, y) + ""
```

关于JDK 6中subString的使用不当会导致内存系列已经被官方记录在Java Bug Database中：

![leak.png](https://i.loli.net/2019/06/19/5d0997d01ae8062131.png)

> 内存泄露：在计算机科学中，内存泄漏指由于疏忽或错误造成程序未能释放已经不再使用的内存。 内存泄漏并非指内存在物理上的消失，而是应用程序分配某段内存后，由于设计错误，导致在释放该段内存之前就失去了对该段内存的控制，从而造成了内存的浪费。

### JDK 7 中的substring

上面提到的问题，在jdk 7中得到解决。在jdk 7 中，substring方法会在堆内存中创建一个新的数组。

![string-substring-jdk71-650x389.jpeg](https://i.loli.net/2019/06/19/5d099876a6ef635654.jpeg)

Java源码中关于这部分的主要代码如下：

```java
//JDK 7
public String(char value[], int offset, int count) {
    //check boundary
    this.value = Arrays.copyOfRange(value, offset, offset + count);
}

public String substring(int beginIndex, int endIndex) {
    //check boundary
    int subLen = endIndex - beginIndex;
    return new String(value, beginIndex, subLen);
}
```

以上是JDK 7中的subString方法，其使用`new String`创建了一个新字符串，避免对老字符串的引用。从而解决了内存泄露问题。

所以，如果你的生产环境中使用的JDK版本小于1.7，当你使用String的subString方法时一定要注意，避免内存泄露。

## 3. replaceFirst、replaceAll、replace 区别



