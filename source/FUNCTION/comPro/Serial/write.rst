++++++++++++++++++
write()
++++++++++++++++++

描述
====
写入二进制数据到串口。发送的数据以一个字节或者一系列的字节为单位。\
例如Serial.write(78),会传输78的二进制01001110，机器会识别为ASCII码，在串口监视窗口打印“N”（即ASCII码78对应的字符）。\

语法
====
Serial.write(val)

或

Serial.write(str)

或

Serial.write(buf, len)

参数
====
val: 字节

str: 一串字节

buf: 字节数组

len: buf的长度

返回
====
返回写入的字节数

例程
====
该例程测试println()和write()参数为78时的不同输出结果。

.. code:: c

	int byteTest = 78;

	void setup(){
		Serial1.begin(9600);
	}

	void loop(){
		Serial.println("输出的结果为：");
		Serial.print("使用println函数：");
		Serial.println(byteTest);
		
		Serial.print("使用write函数：");
		Serial.write(byteTest);
		
		delay(1000);
	}
	
注意
====
无

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态