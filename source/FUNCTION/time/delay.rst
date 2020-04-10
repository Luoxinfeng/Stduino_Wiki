+++++++++++++
delay()
+++++++++++++

描述
=====
delay()函数用来保持某一状态。\
它接受单个整数，此数字表示这一状态持续的时间（以毫秒为单位）。\
当程序遇到这个函数时，将会等待时间过去，再继续执行下一命令。\
然而，delay()函数并不是让程序等待的好方法。\

语法
=====
delay(ms)

参数
=====
ms:延迟的以毫秒为单位的时间




返回
====
无

例程
=====
该例程展示一个闪烁灯（接D13引脚），\
为了让闪烁人眼可见，设置完D13引脚输入电平后，需要等待1000毫秒后，再执行下一语句。\


.. code:: c

		void setup() {
			pinMode(D13,OUTPUT);//初始化13号引脚，控制LED
		}

		void loop() {
			digitalWrite(D13,LOW);   //LED灯亮
			delay(1000);             //保持LED灯亮1000毫秒
			digitalWrite(D13,HIGH); //LED灯灭
			delay(1000);            //保持LED灯灭1000毫秒
		}


注意
====
无

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态