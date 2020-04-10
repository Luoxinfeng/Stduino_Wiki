+++++++++++++
highByte()
+++++++++++++

描述
=====
返回变量高字节。\
如果该变量有两个以上的字节，则取第二低字节（如有四个字节时，返回的是从右数第二个字节）\

一般一个16位（双字节）的数据，比如FF1E（16进制）。那么高位字节就是FF，低位是1E，highByte()返回FF。

如果是32位（四字节）的数据，比如3E68 C16A（16进制）。\
高位字（不是字节）是3E68，低位字是C16A，但是利用highByte()\
返回的是C1（第二低字节）。


语法
=====
highByte(x)

参数
====
x：被取高字节的变量（可以是任何变量类型）








返回
====
字节（byte）

例程
=====
利用highByte()返回整数300的高位字节

.. code:: c

	int intValue = 300; // 300 的16进制为0x12C
	void setup()
	{
	  Serial.begin(9600);
	}
	void loop()
	{
	  byte hiByte;
	  hiByte = highByte(intValue); //取出 intValue 的高位
	  
	  Serial.println(intValue,DEC);//打引输出变量的十进制数值
	  Serial.println(intValue,HEX);//打印输出变量的十六进制数值
	  
	  Serial.println(hiByte,DEC);
	  delay(10000); 
	}





注意
====
无

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态