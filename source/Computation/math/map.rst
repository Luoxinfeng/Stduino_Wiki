+++++++++++++
map()
+++++++++++++

描述
=====
将变量从范围A映射到范围B。\
例如将10位模拟输入结果转换至8位模拟输出、利用模拟输入值控制舵机角度等。\


语法
=====
x = map(value,fromLow,fromHigh,toLow,toHigh)

参数
====
value:需要映射的值。

fromLow/fromHigh:映射前域的上/下限。

toLow/toHigh:需要映射后的域的上/下限。







返回
====
被映射后的值

例程
=====
将一个10位模拟结果转换至8位模拟输出。

.. code:: c

	void setup()
	{
	  pinMode(A1,Input);//设置A1引脚位输入引脚
	  pinMode(8,OUTPUT);//设置8号引脚为输出引脚
	}
	 
	void loop()
	{
	  int x = analogRead(A1);将A1引脚模拟输入值存入x
	  x = map(x, 0, 1023, 0, 255);将x的值从10位缩放到8位，以符合模拟输出取值范围
	  analogWrite(8, x);//从8号引脚以PWM方式输出
	}





注意
====
map()函数使用整型数进行运算，因此小数的余数部分会被舍弃。

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态