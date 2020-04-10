+++++++++++++
analogRead()
+++++++++++++

描述
=====
用于从输入引脚读取模拟信号。

语法
=====
analogRead(Pin)

参数
====
pin:被读取的模拟信号接收引脚。








返回
====
0~4095之间的值

例程
=====
该例程展示读取引脚的模拟量(电压)值变化，并在串口输出显示



.. code:: c

		const int PotentiometerPin=A0;//定义电位器引脚号为常量，即A0引脚
		int PotentiometerValue = 0;//定义电位器读取值为变量

		void setup()
		{
		  Serial.begin(9600); //串口0 开启，波特率设置为9600
		  pinMode(PotentiometerPin,INPUT_AIN);//设置电位器引脚为模拟输入模式
		}

		void loop(){
		  PotentiometerValue= analogRead(PotentiometerPin);//将A0输入信号转换为0-4096之间的数值
		  Serial.println(PotentiometerValue); //通过串口监视器显示电位器读取值
		  delay(1000);//维持现有状态1000ms
		}



注意
====
只有如A1、A2这样的A类端口可以读取模拟信号。

A类端口引脚可接入电位器或其他模拟量元器件，可检测输入电压为0-3.3V。\
输入电压值0~3.3V将被映射到数值0-4096之间。\
超过3.3V的视为满值，例如5V，但是不建议接入5V设备。