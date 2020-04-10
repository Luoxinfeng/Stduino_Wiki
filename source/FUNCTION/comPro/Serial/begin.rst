++++++++++++++++
begin()
++++++++++++++++

描述
====
初始化选择的串口，并设置串行数据传输速率（波特率）。

语法
====
Serial.begin(speed)



参数
====
speed为串行数据传输速率（波特率），单位为比特每秒（bit/s）。\
与计算机进行通信时，常用的波特率为9600和115200两种。\
更多信息参考串口通讯与波特率。


返回
====
无

例程
====
以下例程通过Serial1.begin()实现stduino与电脑间的串口通讯。

.. code:: c

	void setup() 
	{
	  // put your setup code here, to run once:
	  Serial.begin(9600);//初始化
	}

	void loop() 
	{
	  // put your main code here, to run repeatedly:
	  Serial.println("Hello,World");
	  delay(1000);
	}

注意
====
无






访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态