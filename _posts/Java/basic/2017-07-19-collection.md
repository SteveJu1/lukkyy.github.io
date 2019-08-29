---
layout: post
title:  "集合Collection"
date:    2017-07-19 
categories: Java
tags:  Java
---

* content
{:toc}
​       Java.util包提供很多集合类，也叫做容器。集合类可以分为collection集合类和Map集合类两大类，它们都是接口类型，下面有很多子类和实现类。逻辑关系见图

![集合类关系图](https://lukkyy.github.io/assets/java/basic/collection.png)







### Collection	

  Collection集合有3个子类接口，分别是

- List，List集合中元素是有序的，可重复
  - ArrayList
  - LikedList
- Set，元素是无序的，不可重复
  - HashSet，（是一个HashMap的实例）
  - TreeSet，映射关系有一定的顺序
- Queue

#### List

​     下有两个实现类：**ArrayList**(动态数组存储的，查询效率高，插入删除效率低)；**LikedList**（链表存储，查询效率低，插入删除效率高）

遍历方法有三种：

```java
//    1.for循环
for(int i=0;i<list.size(),i++)
{
    system.out.printf(list.get(i));
}
// 下面两种遍历方法，集合都能用
//2.增强的for循环
for(object item：list)
{
    system.out.printf((String)item);
}
//3.迭代器循环
Iterator iterator= list.iterator();
while(iterator.hasNext){
   object item =iterator.next();
   system.out.printf((String)item);
}
```



### Map

Map(映射)是有两个集合构成的，**Key（键）集合和Value（值）集合**

> Note:key是用Set存储，不能有重复，而且是通过**散列函数**计算出存储的位置

Map常用的实现类有HashMap（哈希表）和TreeMap

HashMap：键，值可以为null