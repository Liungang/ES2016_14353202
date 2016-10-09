## DOL安装 ##


### 1. Description###

**Distributed operation layer (DOL)** is a software development framework to program parallel applications. The DOL allows to specify applications based on the Kahn process network model of computation and features a simulation engine based on SystemC. Moreover, the DOL provides an XML-based specification format to describe the implementation of a parallel application on a multi-processor systems, including binding and mapping.


### 2. How to install ###

 - 安装必要文件
 
	![pi img](http://i1.piimg.com/567571/3bb082d5e56d0335.png)
- 编译systemc
 	
        1.解压文件后进入systemc-2.3.1的目录下：
	
			$ cd systemc-2.3.1
			
        2.新建一个临时文件夹objdir：
	
			$ mkdir objdir
			
		3.进入该文件夹objdir： 
	
			$ cd objdir
			
		4.运行configure（能根据系统的环境设置参数，用于编译）：
	
		  	$ ../configure CXX=g++ --disable-async-updates
			
		5.编译并自行记录编译完后文件目录：
	
			$ sudo make install
			
- 编译DOL

		  1.进入DOL的文件夹，修改build_zip.xml文件
		
			找到下面这段话，就是说上面编译的systemc位置在哪里，
		  
		 	   <property name="systemc.inc" value="YYY/include"/>
		    
		 	   <property name="systemc.lib" value="YYY/lib-linux/libsystemc.a"/>
		    
			把YYY改成上页pwd的结果
		  
		  2.编译：
		
			$ ant -f build_zip.xml all
			
		        若成功会显示build successful
		  

- 安装结果

      (由于安装过程中没有截图，只能展示运行example的结果)
               ![pi img1](http://p1.bpimg.com/567571/76d384a67b4f1231.png)


### 3. Experimental experience ###
		本次实验只是安装DOL，主要了解到的是一些Linux指令的应用，如新建文件夹的指令为mkdir。
	还有初次接触markdown以及github，功能很强大。


