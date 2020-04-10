+++++++++++++
noTone()
+++++++++++++

描述
=====
停止由tone()产生的方波。\
如果没有使用tone()将不会有效果。

语法
=====
noTone(pin)

参数
====
pin: 所要停止产生声音接了扬声器等元件的引脚




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
如果你想在多个引脚上产生不同的声音，你要在对下个引脚使用tone()前对刚才的引脚调用noTone().

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态