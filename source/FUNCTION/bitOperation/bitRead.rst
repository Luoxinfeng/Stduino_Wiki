+++++++++++++
bitRead()
+++++++++++++

描述
=====
读取某一个数特定位的值。

语法
=====
bitRead(x,n)

参数
=====
x:想要被读取的数

n：被读取的位，0是最低有效位（最右边）

返回
====
该位的值（0或1）。

例程
=====
该例程展示利用串口通信，从右向左传输11101110的每一位的值。

.. code:: c

	void setup() {
		// put your setup code here, to run once:
		Serial.begin(9600);
	}

	void loop() {
		// put your main code here, to run repeatedly:
		for(int i=0;i <8;i++){
		Serial.println(bitRead(0xEE,i));
		delay(1000);
		}
	}
	
	
注意
====


访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态