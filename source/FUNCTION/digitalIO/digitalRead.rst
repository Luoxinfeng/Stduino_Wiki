+++++++++++++++
digitalRead()
+++++++++++++++

描述
=====
读取指定引脚的电平状态。

语法
=====
digitalRead(pin)

参数
=====
pin:需要读取电平状态的引脚号





返回
====
0或1
 - 0：低电平
 - 1：高电平

例程
=====
该例程展示一个输入引脚控制输出引脚的状态

.. code:: c

	const int ButtonPin = 8;//定义按键引脚号为常量，即D8引脚
	const int LedPin = 13;//定义灯引脚号为常量，即D13引脚
	int ButtonState = 0;//定义按键状态为变量，初始值为0，即低电平
	
	void setup()
	{
	 pinMode(ButtonPin,INPUT);//设置D8引脚为浮空输入模式
	 pinMode(LedPin,OUTPUT);//设置D13引脚为推挽输出模式
	}

	void loop()
	{
	  ButtonState = digitalRead(ButtonPin);//读取按键引脚，并赋值给按键状态
	  
	  if(ButtonState == HIGH)//若是按键状态为高电平
	  {
		digitalWrite(LedPin,HIGH);//灯引脚输出状态更改为高电平
	  }
	  else
	  {
		digitalWrite(LedPin,LOW);//灯引脚输出状态更改为低电平
	  }
	}

注意
====
如果引脚输入模式设为INPUT（浮空输入），该引脚若未接入（例如导线断连等），引脚输入易受干扰，返回值不确定（可能为高，可能为低）。

为保证输入更稳定，可设置输入模式为上拉电阻输入或者下拉电阻输入。详细信息可参考pinMode()中描述的各种输入模式。

模拟引脚(A类口)均能作数字引脚(D类口)使用，例如A0，A1等。