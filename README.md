# python memory
    一个用python写的内存管理器。
## 安装方法
(1)使用pip包管理器安装：<br>
在命令行中输入

    python -m pip install"pymemory"
即可。<br>
注：导入方法：
    import pymemory
(2)使用GIT的克隆命令安装：<br>
在命令行(推荐使用VSCode)中输入：

    git clone https://gitee.com/ajjdxns/python-memory.git
这会将pymemory导入到命令行所在的路径下面。<br>
注：导入方法：

    from pymemory import pymemory
也可以：

    import pymemory.pymemory
## 使用方法
    变量 = pymemory.memory(要管理的程序路径)
比如：

    mm = pymemory.memory("1.20.1.jar")
这样就创建了一个memory对象。

函数：

    变量.setmemory(内存大小)
设置分配的内存大小。<br>
如：

    mm.setmemory(1024)
    #分配1024MB的内存
<br>

    变量.getmemory()
检查系统剩余内存，返回剩余的内存大小。<type = 'int'><br>
如：

    >>> mm.getmemory()
    128
    #剩余128MB内存
<br>

    变量.process(真或假)
设置是否启用多线程。<br>
如：

    mm.process(true)    #启用多线程
<br>

    变量.run(真或假，真或假)

启动实例。<br>
若值1为true，则在新窗口打开。<br>
若值1为false，则在当前窗口运行。<br>
若值2为true，使用Java虚拟机运行。<br>
若值2为false，使用命令行运行。<br>
警告：若使用Java虚拟机运行，需要指定Java命令行参数才能继续工作！！！<br>
如：

    mm.runcommand = java...此处省略... --quickPlayPath ${quickPlayPath}     #设置Java启动参数
    mm.run(false,true)  #用Java虚拟机运行。
<br><br><br>
## END