++++++++++++++++
read()
++++++++++++++++

描述
====
读取传入的串口的数据。

语法
====
Serial1.read()

参数
====
为空

返回
====
返回传入的串口数据的第一个字节\
（如果没有可用的数据，则返回-1）

例程
====


.. code:: c

	int newByte = 0;   // 传入的串行数据
	void setup() 
	{
	 Serial1.begin(9600);     // 打开串口，设置数据传输速率9600
	}
	 
	void loop() 
	{
	 if (Serial1.available() > 0) 
	{// 如果接收到数据
	 newByte = Serial.read();// 读取传入的数据:
			
	 //打印得到的数据
	 Serial1.print("I received: ");
	 Serial1.println(newByte);
	}
	}

注意
====
无



访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态