+++++++++++++
shiftOut()
+++++++++++++

描述
=====
将一个字节的数据通过移位输出方式逐位输出。\
数据可以从最高位（最左位）或从最低位（最右位）输出。\
在输出数据时，当一位数据写入数据输出引脚时，时钟引脚将输出脉冲信号，指示该位数据已被写入数据输出引脚等待读取。

Stduino开发板的普通IO引脚是有限的，必要时要对IO口进行拓展，才能满足外部设备对IO口的需求。\
如利用74HC595芯片来拓展Stduino的IO口，来设计流水灯。

语法
=====
shiftOut(dataPin,clockPin,bitOrder,val)

参数
====
dataPin：输出数据的引脚，引脚需配置成输出模式。
clockPin：时钟引脚。
bitOrder：移位顺序。有高位先出（MSBFIRST）和低位优先（LSBFIRST）两种方式。
val：所要输出的数据值，该数据值将以byte形式输出。









返回
====
无

例程
=====
Stduino外接74HC595芯片，用3个IO口控制8路LED灯。

.. code:: c

	int latchPin = 10;//锁存引脚
	int clockPin = 9; //时钟引脚
	int dataPin = 8; //数据引脚

	void setup ()
	{
	  pinMode(D10, OUTPUT);//锁存引脚
	  pinMode(D9, OUTPUT);//时钟引脚
	  pinMode(D8, OUTPUT); //数据引脚
	}
	void loop()
	{
	  for (int data = 0; data < 255; data++)
	  {
		digitalWrite(D10, LOW); //将ST_CP口上加低电平让芯片准备好接收数据
		shiftOut(D8, D9, LSBFIRST, data);
		digitalWrite(D10, HIGH); //将ST_CP这个针脚恢复到高电平
		delay(1000); //延迟1秒钟观看显示
	  }
	}





注意
====
 - 使用shiftOut()函数前，数据引脚（dataPin）和时钟引脚（clockPin）必须先通过pinMode()指令设置为输出（OUTPUT）模式。

 - 如果读取数据的设备是在Stduino的时钟引脚脉冲信号上升沿读取Stduino的输出数据，请确保在调用shiftOut()输出数据前，应先通过digitalWrite(clockPin, LOW)语句，将时钟引脚设置为LOW，以确保数据读取准确无误。

 - shiftOut一次只能输出1字节（8位）数据。如果需要输出大于255的数值，需要通过两次使用shiftOut()输出数据。\
如下程序所示：

.. code:: c

	// 高位字节先出模式
	int data = 500; //待输出数据
	shiftOut(dataPin, clock, MSBFIRST, (data >> 8)); // 输出高位字节
	shiftOut(dataPin, clock, MSBFIRST, data); // 输出低位字节

	// 低位字节先出模式
	data = 500; //待输出数据
	shiftOut(dataPin, clock, LSBFIRST, data); // 输出低位字节
	shiftOut(dataPin, clock, LSBFIRST, (data >> 8)); // 输出高位字节

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态