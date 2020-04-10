+++++++++++++
shiftIn()
+++++++++++++

描述
=====
将一个数据的字节一位一位的移入。从哪个最高有效位（最左边）或最低有效位（最右边）开始。\
对于每个位，先拉高时钟电平，再从数据传输线中读取一位，再将时钟线拉低。

语法
=====
shiftIn(dataPin,clockPin,bitOrder)

参数
====
dataPin:数据引脚

clockPin:时钟引脚

bitOrder:移位顺序，高位先入（MSBFIRST）还是低位先入（LSBFIRST）。




返回
====
读取到的数据

例程
=====


.. code:: c






注意
====
如果与Stduino进行数据通讯的设备是在时钟引脚脉冲信号上升沿发送数据，请确保在调用shiftIn()前，\
应先通过digitalWrite(clockPin, LOW)语句，将时钟引脚设置为LOW。

访问\ `Stduino官网 <http://stduino.com/forum.php>`_ ，了解更多Stduino动态