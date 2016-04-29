基于RSA算法的加密解密系统
===================================

##功能说明
这是一个关于RSA加密算法的简单程序，在最近的版本中，可以进行英文文本的加密，解密和密钥对的生成。**密钥长度较低**，仅作为对RSA加密算法的探究。



##安装说明
		linux下在对应的文件夹下执行 make ，windows下请参考Makefile自行寻找编译器编译。



##使用说明
###一 加密
	将需要加密的文件，放在source.txt中，程序启动后，按照提示输入指令，选择加密功能。
	之后按照提示输入公钥即可完成加密。加密后的密文将存放在result.txt中。

###二 解密
	解密过程与加密过程相反，操作类似。

###三 生成密钥对
	程序启动后，按照提示输入指令，选择生成密钥对功能，即可随机生成一对密钥，同时在程序所在文件夹中，将产生
	Pub_key,txt和Pri_key.txt文件，其中包含按照时间排列的密钥对记录。
    


##错误处理
如果文件在运行过程中产生一些**可以预料的**错误，将会在程序所在文件夹中生成Error.txt文件。



##其他文件
在程序初次运行时，会产生primer_number.txt和configuration,txt，其中包含生成密钥对所需要的素数表以及程序的配置信息。


##配置说明
configuration.txt中包含了程序运行过程中需要的参数。<br />
以下对其中的参数进行说明<br />
[Configuration From File]  是否从文件读取配置信息，1表示是，0表示否，默认1<br />
[Total Number]             素数表中的素数总数<br />
[L_MIT]                    素数表左边界，默认5000<br />
[R_MIT]                    素数表右边界，默认9999<br />
[BITWIDTH]                 一个加密单位包含的字符数，默认3<br />
**注意：** <br />
1.调整边界和加密单位可能导致溢出，请谨慎调节。<br />
2.调整素数表边界之后，请删除原有素数表，以便以程序在下次启动是重新生成，并同时调整程序中内置的hash值<br />



