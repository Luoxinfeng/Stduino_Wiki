+++++++++++++++++++
millis()
+++++++++++++++++++

描述
=====
用来返回微处理器从开始运行到该条命令的时间（以毫秒为单位）\
可以一直计时50天左右。\
50天之后则会溢出，重新归零。\


语法
=====
millis()

参数
=====
无

返回
====
返回一个无符号长整形类型的值

例程
=====
该例程利用串口通讯报告程序持续时间

.. code:: c

unsigned int time;
void setup() {
	// put your setup code here, to run once:
	Serial.begin(9600);
}

void loop() {
	// put your main code here, to run repeatedly:
	
	Serial.print((char*) "Time:"); 
	time = millis();
	Serial.println(time); //打印从程序开始到现在的时间
	delay(1000); // 等待一秒钟，避免发送大量数据
}


注意
====
serial.print()目前还不能接受string类型，需要强转为char*类型。



访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态