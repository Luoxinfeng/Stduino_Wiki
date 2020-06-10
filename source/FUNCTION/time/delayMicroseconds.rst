+++++++++++++++++++
delayMicroseconds()
+++++++++++++++++++

描述
=====
函数接受单个整数（或数字）参数。此数字表示时间，以微秒(us)为单位。一毫秒等于一千微秒，一秒等于一千毫秒。\

对于超过几千微秒的延迟，应该使用delay()函数。\
实际上微妙级别的延时会有误差。


语法
=====
delayMicroseconds(us)


参数
=====
us:延迟的以微秒为单位的时间




返回
====
无

例程
=====



.. code:: c

		void setup() {
			pinMode(D13,OUTPUT);//初始化13号引脚，控制LED
		}

		void loop() {
			digitalWrite(D13,LOW);   //LED灯亮
			delayMicroseconds(1000);  //保持LED灯亮1000微秒
			digitalWrite(D13,HIGH);  //LED灯灭
			delayMicroseconds(1000);  //保持LED灯灭1000微秒
		}



注意
====
无


访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态