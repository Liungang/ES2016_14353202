## ROS安装 ##
### 1.安装过程
####1.1 Setup sources.list
	sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" >
	 /etc/apt/sources.list.d/ros-latest.list'
####1.2 Set up your keys
	sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116
####1.3 Installation
	First, make sure your Debian package index is up-to-date
		sudo apt-get update
	Desktop-Full Install: 
		sudo apt-get install ros-kinetic-desktop-full
	Desktop Install:
		sudo apt-get install ros-kinetic-desktop
	ROS-Base: (Bare Bones) 
		sudo apt-get install ros-kinetic-ros-base
	Individual Package:
		sudo apt-get install ros-kinetic-PACKAGE
####1.4 Initialize rosdep
	sudo rosdep init
	rosdep update
####1.5 Environment Setup
	echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
	source ~/.bashrc
####1.6 Getting rosinstall
	sudo apt-get install python-rosinstall

###2. ROS 测试
####2.1 获取软件包有关信息（路径）
![img1](http://yotuku.cn/link?url=N1SvFaAlM&tk_plan=free&tk_storage=tietuku&tk_vuid=55ef2d88-bde9-4228-8433-5808f59d10b6&tk_time=2016111122)
####2.2 查看环境变量
![img2](http://yotuku.cn/link?url=EJL2KaRgf&tk_plan=free&tk_storage=tietuku&tk_vuid=55ef2d88-bde9-4228-8433-5808f59d10b6&tk_time=2016111122)
####2.3 查看一级依赖包信息，内容大致为packages.xml所示信息
![img3](http://yotuku.cn/link?url=41LJq6Cxf&tk_plan=free&tk_storage=tietuku&tk_vuid=55ef2d88-bde9-4228-8433-5808f59d10b6&tk_time=2016111122)
####2.4 检查ROS系统
![img4](http://yotuku.cn/link?url=V1c19TAgM&tk_plan=free&tk_storage=tietuku&tk_vuid=55ef2d88-bde9-4228-8433-5808f59d10b6&tk_time=2016111122)
###3. ROS总结
	    ROS（机器人操作系统，Robot Operating System），是专为机器人软件开发所设计出来的一套电脑操作系统架构。
	它是一个开源的元级操作系统（后操作系统），提供类似于操作系统的服务，包括硬件抽象描述、底层驱动程序管理、共用
	功能的执行、程序间消息传递、程序发行包管理，它也提供一些工具和库用于获取、建立、编写和执行多机融合的程序。
	ROS的运行架构是一种使用ROS通信模块实现模块间P2P的松耦合的网络连接的处理架构，它执行若干种类型的通讯，包括
	基于服务的同步RPC（远程过程调用）通讯、基于Topic的异步数据流通讯，还有参数服务器上的数据存储。