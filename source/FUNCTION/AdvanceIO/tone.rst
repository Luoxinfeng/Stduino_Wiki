+++++++++++++
tone()
+++++++++++++

描述
=====
可以产生固定频率的PWM信号驱动扬声器发声。发出声音的长度和声调（即频率）都可以通过参数来控制。\
发声持续时间需要利用tone()开启，noTone()来停止发声这种方式来控制。

语法
=====
tone(pin,frequency)

参数
====
pin:接入引脚（该引脚需要连接扬声器）

frequency:发声频率（单位：赫兹）——无符号整数型数据（unsigned int）


返回
====
无

例程
=====
利用A6和A7引脚接扬声器来制作警报声。

.. code:: c

	void setup() 
	{
		
	}
	 
	void loop() 
	{  
	 tone(A6, 440);  //6号引脚发声200毫秒
	 delay(200);
	 noTone(A6);   //停止6号引脚发声
		
	 tone(A7, 494); //7号引脚发声500毫秒
	 delay(500);
	 noTone(A7); //停止7号引脚发声

	 delay(300);

	}




注意
====
无

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态