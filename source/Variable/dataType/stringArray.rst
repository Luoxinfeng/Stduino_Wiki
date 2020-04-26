++++++++++++++
string-char数组
++++++++++++++

描述
=====
文本可以用两种方式表示。\
您可以使用  ``String数据类型`` ，\
也可以从  ``char类型的数组`` 中生成字符串并以null终止。\
本页描述了后一种方法。\
有关  ``String对象`` 的更多详细信息，请参阅： \ `String对象 <stringObject.html>`_ ，
它以消耗较多的内存为代价提供了更多功能。\

语法
=====
以下节为有效的字符串。

- char Str1[15];//声明一个五个字符大小的char数组
- char Str2[8] = {'S', 't', 'd', 'u', 'i', 'n', 'o'};//声明一个字符数组，并为其赋值
- char Str3[8] = {'S', 't', 'd', 'u', 'i', 'n', 'o', '\0'};//添加空字符
- char Str4[] = "Stduino";//声明一个空数组，并赋值
- char Str5[8] = "Stduino";//声明8个字符长度的数组，并赋值
- char Str6[15] = "Stduino";










例程
=====
声明字符串

.. code:: c

	char *myStrings[] = {
	  "This is string 1", "This is string 2", "This is string 3",
	  "This is string 4", "This is string 5", "This is string 6"
	};

	void setup() {
	  Serial.begin(9600);
	}

	void loop() {
	  for (int i = 0; i < 6; i++) {
		Serial.println(myStrings[i]);
		delay(500);
	  }
	}              // 将浮点数换保留到小数点后三位，并转化为字符串





注意
====
 通常，字符串以空字符（ASCII代码0）结尾。这使函数（如Serial.print()）可以判断字符串的结尾在哪里。
 
 也就是说，字符串需要比需要容纳的文本多留一个空格，\
 这也就是为什么Str2和Str5必须为八个字符的原因，即使"Stduino"只有七个，最后一个位置也会自动填充一个空字符。\
 Str4的大小将自动设置为八个字符，其中一个用于表示多余的null。\
 在Str3中，我们自己明确包含了空字符（写为'\0'）。
 
访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态