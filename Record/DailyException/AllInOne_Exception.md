# Today Abnormal

[TOC]

------

# Day01

1. 错误: 不兼容的类型: int无法转换为Long
       System.out.println((Long)max + 2);

   correct:   

```java 
   int max = INTEGER.MAX_VALUE;
   System.out.println((long)max + 2);
   //or
   System.out.println(max + 2L);
```

   

​    

1. 找不到或无法加载主类 Test01.class

   `java Test01.class`  

2. javac: 无效的标记: Test01.class

   `javac Test01.class`

3. 错误: 空字符文字

   ```java
   System.out.println('');
   //有且仅有一个字符。
   ```

   

   # Day02 Exception

   1. 错误: 不兼容的类型: 从double转换到int可能会有损失
           x = x + 2.5;

   - 第一种

     ```jav
       	 int x = 10;
           x = x + 2.5;
           System.out.println(x);
     ```

   - 第一种变式

   ```java
   	int num = 8 + 2.5;
       System.out.println(num);
   ```

   

   1. 错误: 不兼容的类型: 从`float`转换到`int`可能会有损失

   - 第一种

     ```java
     int result = 3 > 4 ? 2.5F : 10;
     
     System.out.println(result);
     ```

   - 

   ```java
    	 int num = 8 + 2.5F;
       System.out.println(num);
   ```

   

   1. 错误: 不是语句

      ```java
         a > b ? a : b;
      ```

      ` javac LogicTest.java`

   

   4.==比较三个数的大小?==

   

   - > 错误: 二元运算符 '>' 的操作数类型错误
     >    int otherMaxWay = (x > y) && (x > z) > x ? x :((y > z) ? y : z);
     >                                         ^
     >  第一个类型:  boolean
     >  第二个类型: int
     > 1 个错误

   

   ```java
    int x = 20;
    int y = 40;
    int z = 30;   
    int otherMaxWay = (x > y) && (x > z) > x ? x :((y > z) ? y : z);
   
   ```

   三元数据类型一致.

   - > 错误: 二元运算符 '>' 的操作数类型错误
     >     int otherMaxWay = ((x > y) && (x > y)) > z ? (x > y) && (x < y) : z;
     >                                            ^
     >   第一个类型:  boolean
     >   第二个类型: int
     > OperatorThreeTest.java:23: 错误: 不兼容的类型: INT#1无法转换为int
     >     int otherMaxWay = ((x > y) && (x > y)) > z ? (x > y) && (x < y) : z;
     >                                                ^
     >   其中, INT#1,INT#2是交叉类型:
     >     INT#1扩展Object,Serializable,Comparable<? extends INT#2>
     >     INT#2扩展Object,Serializable,Comparable<?>
     > 2 个错误

   

   ```java
   	// int otherMaxWay = ((x > y) && (x < y)) > z ? (x > y) && (x < y) : z;
       //
       // int otherMaxWay = ((x > y) && (x < y)) > z ? (x > y) && (x < y) : z;
       //
       // int otherMaxWay = ((x > y) && (x > z)) > z ? (x > y) && (x < y) : z;
       //
       // int otherMaxWay = (x > y) && (x > z) > x ? x :((y > z) ? y : z);
   ```

   

   

   5.

# Day03_Exception

1. 不同循环下, 作用域的问题.

```java
	
	for (int i = 0; i < 100; i++) {
      System.out.println("HelloLOOP~~~" + i);
    }
    System.out.println("++++++++++++++++++++++++++++");

    int j = 1;
    while(j < 100) {
      System.out.println("HelloWhile~~~" + j);
      j++;
    }

    System.out.println("++++++++++++++++++++++++++");

    int x = 1;
    do {
      System.out.println("HelloDoWhile~~~" + x);
      x++;
    }
    while (x < 100);
    System.out.println("KEY:x =" + x );//100
    System.out.println("KEY:x =" + j );//100
    System.out.println("KEY:x =" + i );//找不到 i ,超过作用域.

```



2.

______





# daily_Exception_05

1.  `NullPointerExcepton`

```java
int[] array012;
array012 = null;
array012[2] = 3;
System.out.println(array012[2]);
```

2. `java.lang.ArrayIndexOutOfBoundsException`



```java
double[] array022;
array022 = new double[4];
array022[4] = 0.332;
System.out.println(array022[4]);
```
