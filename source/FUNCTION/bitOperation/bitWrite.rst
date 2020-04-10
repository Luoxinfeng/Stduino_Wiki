++++++++++++
bitWrite()
++++++++++++

描述
=====
修改一个数的某位上的数值。

语法
=====
bitWrite(x,n,b)

参数
=====
x:想要修改的数值变量。

n：要写入的数值的位。右边为最低位，n=0。

b:写入的数值（0或1）。

返回
====
该位的值（0或1）。

例程
=====
修改11101110（0xEE）的右边第二位的值为0，并利用窗口通信传输改变后的值。

.. code:: c

	void setup() {
		// put your setup code here, to run once:
		Serial.begin(9600);
	}

	void loop() {
		// put your main code here, to run repeatedly:
		Serial.println(bitRead(0xEE,1));//传输没有修改前的右边第二位值
		delay(500);
		
		bitWrite(0xEE,1,0);//修改右边第二位的值为0；
		Serial.println(bitRead(0xEE,1));//传输修改后的右边第二的值
		delay(500);
	}
	
	
注意
====




访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态