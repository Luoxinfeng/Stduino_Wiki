+++++++++++++
readString()
+++++++++++++

描述
=====
从串口缓存区读取全部数据到一个字符串型的变量

语法
=====
Serial.readString()

参数
====
无


返回
====
字符串

例程
=====
利用Serial.readString()接收串口通讯的所有数据，并打印出来

.. code:: c

	string serialData ="";
	
	void setup() 
	{
	  Serial.begin(9600);
	  while(Serial.read()>= 0){} 
	}
	void loop() 
	{
	  if(Serial.available()>0)
	  {
	    delay(100);
		seriaData = Serial.readString();
		Serial.print("接收数据为:");
		Serial.println(" ");
	  }
	}





注意
====
无



访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态