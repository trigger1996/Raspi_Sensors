,can# Raspi_Sensors


This is a integrated simple Rpi Sensor moduled for px4 autopilot, which is designed for mostly compatibility with Navio
And it's drawn by Altium Designer (or Dxp)


2017.11.25
	
	修改意见之二：
	
	1 在电源处用来隔离的小电阻有问题，在上面有2V多的压降，参考HT_HAWK的原理图，那个电阻大可不要，或者换成开关管
	
	2 电感太大，挡住了别的器件
	
	3 备用电源可以取消了，因为Lidar不会从那边走了
	
	4 MS5611还是要往下移动一点，还是会被挡住

	5 灯也会5611被挡住
	
	6 靠GPIO的两个螺丝孔位不对
	
	
2017.11.20

Block 1 is not cabable enough for its strong internal crosstalk. So we attempt to reroute and a couple of copnents to reduce interference from the motor and power source, such as an inductor and a diode, etc.



2017.10.9

修改意见:


1  PCA9685的宽度画大了

2  5V和Vcc没有在一起，这个是最要命的！

3  严重低估了排母躺下来以后的大小

4  过摄像头的镂空的口的宽度可以缩小1/3，还有摄像头的出口其实被PCA9685挡住了

5  SBUS不要和9685距离太近，排母剪断以后会占用一点额外空间

6  5611少画了一格

7  电源插头和LED太靠内

8  5611和SBUS的丝印没有表示方向

9 LED从BGR->BRG

10 GPS的接口可以改成SPI的，因为串口已经99%用不了了。GPS建议单独做一个模块，单独的模块注意隔离
