# String

## 字符串的不可变性

这里有一组图片来说明Java字符串的不可变性。

**1. 声明一个字符串**

以下代码初始化了一个字符串s.

```java
String s = "abcd";
```

如下所示，变量s储存了一个字符串对象的引用。箭头可以被当做“储存引用”。

![String-Immutability-1.jpeg](https://i.loli.net/2019/06/17/5d074e22beae448963.jpeg)

**2. 将一个字符串变量分配给另一个字符串变量**

下面代码将s分配给了s2.

```java
String s2 = s;
```

s2储存了一个相同的引用值，因为它是同一个字符串对象。

![String-Immutability-2.jpeg](https://i.loli.net/2019/06/17/5d074f4b1c45192435.jpeg)

**3.合并字符串**

当我们合并一个字符串”ef”到s，

```java
s = s.concat("ef");
```

如下所示，s存储新创建的字符串对象的引用：

![string-immutability-650x279.jpeg](https://i.loli.net/2019/06/17/5d074f4b1a52e14825.jpeg)

**总结**

综上所述： 一旦在内存（堆）中创建了一个字符串，它就不能被改变。所有字符串的方法都没有去改变字符串自己，而是返回了一个新对象。

如果我们需要一个可以修改的字符串，我们将需要使用**StringBuffer** 或 **StringBuilder**. 否则，垃圾收集会浪费大量时间，因为每次创建一个新的字符串。

## 参考文章

[Diagram to show Java String’s Immutability](https://www.programcreek.com/2009/02/diagram-to-show-java-strings-immutability/)

