+++++++++++++
peek()
+++++++++++++

描述
=====
返回传入的串行数据的下一个字节（字符）。\
串口接收到的数据都会暂时存放在接受缓冲区中，使用peek()读取时，不会移除接受缓冲区中的数据。\
而使用read()读取数据后，会将该数据从接收缓冲区移除。\
也就是说，连续调用 peek()将返回相同的字符，其他与调用read()方法相同。

语法
=====
Seria.peek()


参数
====
无

返回
====
返回传入的串口数据的第一个字节（String类型）\
（如果没有可用的数据，则返回-1）

例程
=====
本例程利用peek()方法打印接受到的信号\
由于peek()读取的时候不会清除缓存，而是直接将缓存中的数据复制一份。

.. code:: c

	String newChar= "";   // 传入的串行数据
	void setup() 
	{
	 Serial.begin(9600);     // 打开串口，设置数据传输速率9600
	}
	 
	void loop() 
	{
	 if (Serial.available()) 
	{// 如果接收到数据
	 newChar = Serial.peek();// 读取传入的数据:
			
	 //打印得到的数据
	 Serial.print("I received: ");
	 Serial.println(newChar);
	}
	}




注意
====
无

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态