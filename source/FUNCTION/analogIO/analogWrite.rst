+++++++++++++++
analogWrite()
+++++++++++++++

描述
=====
将模拟信号写入引脚。可用于制作呼吸灯或者以不同的速度驱动电动机。

语法
=====
digitalWrite(pin,value)

参数
====
pin:要设置的模拟信号引脚（int类型）
value:占空比，在0~255之间。



返回
====
无

例程
=====
该例程展示一个呼吸灯的制作。

.. code:: c
		
		int analogPin = A2;
		
		void setup()
		{
		  pinMode(analogPin,OUTPUT_PWM);//初始化
		}

		void loop() 
		{
		  for(int i=0; i<256; i++) 
		  {
			//for循环语句，让亮度从0到255
			analogWrite(analogPin,i);
			delay(15);//变化太快可能看不清
		  }
			
		  for(int i=255;i>-1;i--) 
		  {
			//for循环语句，让亮度从255到0
			analogWrite(analogPin,i);
			delay(15);
		  }
		}
 

注意
====
初始化引脚时，需要设置为OUT_PWM模式。