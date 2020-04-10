+++++++++++++
micros()
+++++++++++++

描述
=====
返回Stduino从运行当前程序开始的微秒数。这个数字将在约71分钟后溢出。\


语法
=====
micros()

参数
====
无

返回
====
返回从运行当前程序开始的微秒数（无符号整型unsigned int）。

例程
=====


.. code:: c

	unsigned int time;
	void setup()
	{
	 Serial1.begin(9600);
	}
	void loop()
	{
	 //Serial.print("Time:");
	 time = micros();
	 //打印从程序开始的时间
	 Serial1.println(time);
	 //等待一秒钟
	 delay(1000);
	}




注意
====
1毫秒=1000微秒,1秒=1000毫秒。

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态