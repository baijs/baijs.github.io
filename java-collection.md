# [译] Java 集合接口/类的继承关系


原文地址[http://www.programcreek.com/2009/02/the-interface-and-class-hierarchy-for-collections/](http://www.programcreek.com/2009/02/the-interface-and-class-hierarchy-for-collections//)



## 1. Collection 和 Collections 的区别

首先，“Collection” 和 “Collections” 是两个不同的概念。 从下图可见：
- “Collection” **是** Java.uitl 包中所有集合类的根**接口**，它定义了基本的容器操作方法，它的超级接口是 Iterator
- “Collections” **是**一个包装**类**。它包含有各种有关集合操作的静态多态方法。此类不能实例化，就像一个工具类，服务于 Java 的 Collection 框架


![image](https://raw.githubusercontent.com/baijs/blog_img/master/java-collection/CollectionVsCollections.jpeg)

## 2. Collection 子类/接口容器继承关系

![image](https://raw.githubusercontent.com/baijs/blog_img/master/java-collection/java-collection-hierarchy.jpeg)

## 3. Map 类的层次结构图

![image](https://raw.githubusercontent.com/baijs/blog_img/master/java-collection/MapClassHierarchy.jpg)

## 4. 总结

![image](https://raw.githubusercontent.com/baijs/blog_img/master/java-collection/collection-summary.png)

![image](https://raw.githubusercontent.com/baijs/blog_img/master/java-collection/collection.bmp)

## 5. 代码示例


```
List<String> a1 = new ArrayList<String>();
a1.add("Program");
a1.add("Creek");
a1.add("Java");
a1.add("Java");
System.out.println("ArrayList Elements");
System.out.print("\t" + a1 + "\n");
 
List<String> l1 = new LinkedList<String>();
l1.add("Program");
l1.add("Creek");
l1.add("Java");
l1.add("Java");
System.out.println("LinkedList Elements");
System.out.print("\t" + l1 + "\n");
 
Set<String> s1 = new HashSet<String>(); // or new TreeSet() will order the elements;
s1.add("Program");
s1.add("Creek");
s1.add("Java");
s1.add("Java");
s1.add("tutorial");
System.out.println("Set Elements");
System.out.print("\t" + s1 + "\n");
 
Map<String, String> m1 = new HashMap<String, String>(); // or new TreeMap() will order based on keys
m1.put("Windows", "2000");
m1.put("Windows", "XP");
m1.put("Language", "Java");
m1.put("Website", "programcreek.com");
System.out.println("Map Elements");
System.out.print("\t" + m1);
```

输出结果：


```
ArrayList Elements
	[Program, Creek, Java, Java]
LinkedList Elements
	[Program, Creek, Java, Java]
Set Elements
	[tutorial, Creek, Program, Java]
Map Elements
	{Windows=XP, Website=programcreek.com, Language=Java}
```
