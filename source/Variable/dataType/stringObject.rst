+++++++++++++
String()-类
+++++++++++++

描述
=====
该语句用来构造  ``String类`` 的实例。可以利用不同的数据类型构造字符串（即将这些数据格式化为字符串) 

包括：

- 用""引起来的常量字符串，即char数组

- 用''引起来的单个常量字符

- String对象的另一个实例

- 常数整数或长整数

- 指定的基数的常数整数或长整数

- 整数或长整数变量

- 指定基数的整数或长整数变量

- 具有指定位数的浮点数或双精度浮点数（double）

语法
=====
可以使用下列三者之一声明String类型变量。

- String(val)

- String(val,base)

- String(val,decimalPlaces)

参数
====
val:需要转换为字符串的变量。支持转换的数据类型包括：字符串、字符、字节、整数、长整数、无符号整数、无符号长整数、浮点数、双精度数。

base:（可选）需要转换整数型的基数（即对进制的规定）。

decimalPlaces:仅当val为float或double时，所需的小数位数。









返回
====
String类的一个实例。

例程
=====
声明字符串

.. code:: c

	String stringOne = "Hello,Stduino!";                  // 构建一个常量字符串
	String stringOne = String("a");                       // 将字符转换为字符串
	String stringTwo = String("This is a string");        // 将一个常量字符串转化为字符串
	String stringOne = String(stringTwo + " with more");  // 将两个字符串连接成一个字符串
	String stringOne = String(13);                        // 将一个常量整数型转化为字符串
	String stringOne = String(analogRead(0), DEC);        // 将整数换算为十进制，并转化为字符串
	String stringOne = String(45, Hex);                   // 将整数换算为八进制，并转化为字符串
	String stringOne = String(255,BIN);                   // 将整数换算为二进制，并转化为字符串
	String stringOne = String(millis(), DEC);             // 将长整形数换算为十六进制，并转化为字符串
	String stringOne = String(5,698,3);                   // 将浮点数换保留到小数点后三位，并转化为字符串





注意
====
 
 
访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态