# linux top命令查看CPU使用率 #

%Cpu(s):  0.5 us,  0.2 sy,  0.0 ni, 99.3 id,  0.1 wa,  0.0 hi,  0.0 si,  0.0 st

    1.3 CPU 状态:
    
    这里显示不同模式下所占cpu时间百分比，这些不同的cpu时间表示：
    us, user： 运行(未调整优先级的) 用户进程的CPU时间
    sy，system: 运行内核进程的CPU时间
    ni，niced：运行已调整优先级的用户进程的CPU时间
    wa，IO wait: 用于等待IO完成的CPU时间
    hi：处理硬件中断的CPU时间
    si: 处理软件中断的CPU时间
    st：这个虚拟机被hypervisor偷去的CPU时间（译注：如果当前处于一个hypervisor下的vm，实际上hypervisor也是要消耗一部分CPU处理时间的）。
    可以使用't'命令切换显示。
    
    1.3% us — 用户空间占用CPU的百分比。
    1.0% sy — 内核空间占用CPU的百分比。
    0.0% ni — 改变过优先级的进程占用CPU的百分比
    97.3% id — 空闲CPU百分比
    0.0% wa — IO等待占用CPU的百分比
    0.3% hi — 硬中断（Hardware IRQ）占用CPU的百分比
    0.0% si — 软中断（Software Interrupts）占用CPU的百分比
    在这里CPU的使用比率和windows概念不同，如果你不理解用户空间和内核空间，需要充充电了。

参考链接：

https://www.cnblogs.com/zhoug2020/p/6336453.html