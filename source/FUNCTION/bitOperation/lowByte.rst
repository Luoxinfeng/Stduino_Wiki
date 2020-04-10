+++++++++++++
lowByte()
+++++++++++++

描述
=====
返回一个变量的低位（最右边）的字节。

语法
=====
lowByte(x)

参数
====
x:任何类型的值




返回
====
字节（Byte）

例程
=====
利用lowByte()返回整数300的低位字节

.. code:: c

	int intValue = 300; // 300 的 16 进制为 0x12C
	void setup()
	{
	  Serial.begin(9600);
	}
	void loop()
	{
	  byte loByte;
	  loByte = lowByte(intValue); //取出 intValue 的高位
	  
	  Serial.println(intValue,DEC);//打引输出变量的十进制数值
	  Serial.println(intValue,HEX);//打印输出变量的十六进制数值
	  
	  Serial.println(loByte,DEC);
	  delay(10000); 
	}





注意
====
无

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态