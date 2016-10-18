# DOL实例分析

### 1. 代码修改以及截图
    example1:修改square.c文件里面的square_fire函数（将 i = i*i 改为 i = i*i*i）
![icon1](http://i1.piimg.com/567571/79ee0a5aec9f062e.png)


	example2:修改example2.xml文件，更改迭代次数（value = "3" 改为 value = "2")
![icon](http://i1.piimg.com/567571/cd20cd88f94f1e05.png)

### 2. 实验结果截图
	example1：
![icon2](http://p1.bqimg.com/567571/8fdaa02909667983.png)
	
	example2:
![icon3](http://p1.bqimg.com/567571/8a419478939999bc.png)

### 3. 实验感想
	   在本次实验中，遇到的主要问题是当编译编译完example1后，再编译example2后发现编译失败，
	原因是没有删除之前编译完的example1文件夹。然后又遇到个问题，如何删除系统文件夹，百度后了
	解到可以用命令 rm -rf xxx(文件夹名）删除文件夹，命令 rm -f xxx（文件名）可删除文件。