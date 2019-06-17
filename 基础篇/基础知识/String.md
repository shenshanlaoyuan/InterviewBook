# String

## 字符串的不可变性

Here are a set of diagrams to illustrate Java String's *immutability*.

**1. Declare a string**

The following code initializes a string *s*.

```java
String s = "abcd";
```

The variable *s* stores the reference of a string object as shown below. The arrow can be interpreted as "store reference of".

![String-Immutability-1.jpeg](https://i.loli.net/2019/06/17/5d074e22beae448963.jpeg)

**2. Assign one string variable to another string variable**

The following code assign *s* to *s2*.

```java
String s2 = s;
```

*s2* stores the same reference value since it is the same string object.

![String-Immutability-2.jpeg](https://i.loli.net/2019/06/17/5d074f4b1c45192435.jpeg)

**3. Concat string**

When we concatenate a string "ef" to *s*,

```java
s = s.concat("ef");
```

s stores the reference of the newly created string object as shown below.

![string-immutability-650x279.jpeg](https://i.loli.net/2019/06/17/5d074f4b1a52e14825.jpeg)

**Summary**

In summary, once a string is created in [memory](https://www.programcreek.com/2013/04/jvm-run-time-data-areas/)(heap), it can not be changed. All methods of String do not change the string itself, but rather return a new String.

If we need a string that can be modified, we will need *StringBuffer* or *StringBuilder*. Otherwise, there would be a lot of time wasted for Garbage Collection, since each time a new String is created.

## 参考文章

[Diagram to show Java String’s Immutability](https://www.programcreek.com/2009/02/diagram-to-show-java-strings-immutability/)

