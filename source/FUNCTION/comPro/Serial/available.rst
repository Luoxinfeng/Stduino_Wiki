+++++++++++++++++++
available()
+++++++++++++++++++

描述
====
获取从串口读取有效的字节数（字符）。\
常用来判断串口是否接受到信号

语法
====
Serial.available()

参数
====
空

返回
====
可读取的字节数

例程
====
以下例程实现Stduino与电脑间串口通讯，利用Serial1.available()判断串口是否初始化。

.. code:: c

	void setup() 
	{
	  // put your setup code here, to run once:
	  Serial.begin(9600);//串口初始化
	}

	void loop() 
	{
	  // put your main code here, to run repeatedly:
	  if(Serial.available())
	  {
		//判断是否初始化
		if(Serial.read()==49)
		{//判断是否接收到了1，49是1的ASCII码值
		  Serial.println("Hello,world!");
		}
	  }
	}

 


注意
====
测试时注意收到的是十进制还是ascii码。



访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态