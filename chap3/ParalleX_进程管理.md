#第三章  内核提供的服务
##3.1 进程管理

###3.1.1 进程定义
进程：计算机执行的一项任务以及其所需要的资源称之为一个进程。

进程的创建：
第一步： 分配进程控制结构task_struct。
第二步： 填充控制结构信息,填写最基本的初始信息。
第三步： 将创建好的“静态进程”挂载到任务初始化链表上。
第四步： 发送请求调度消息。

进程的运行：
调度程序遍历任务消息处理链表，将请求被调度的进程到预备运行的位置。

进程的结束：
进程主动结束，发送请求结束消息，调度程序定期遍历消息链表，释放进程的资源。


###

