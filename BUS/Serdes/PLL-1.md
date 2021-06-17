# PLL 锁相环教程和入门
锁相环、PLL 应用
锁相环接收一个它锁定的信号，然后可以从它自己的内部 VCO 输出这个信号。乍一看，这可能看起来不是特别有用，但只要稍加创意，就有可能开发出大量的锁相环应用。

一些锁相环应用包括：

FM 解调：   一种主要的锁相环应用是 FM 解调器。由于 PLL 芯片现在相对便宜，因此这种 PLL 应用能够从 FM 信号中解调出高质量的音频。
AM 解调：   锁相环可用于调幅信号的同步解调。使用这种方法，PLL 锁定到载波上，以便可以在接收器内生成参考。由于这与载波的频率完全对应，因此它可以与输入信号混频以同步解调 AM。
间接频率合成器：   在频率合成器中使用是最重要的锁相环应用之一。虽然也使用直接数字合成，但间接频率合成是主要的锁相环应用之一。
信号恢复：   锁相环能够锁定信号这一事实使其能够提供干净的信号，并在出现短暂中断时记住信号频率。这种锁相环应用用于信号可能会在短时间内中断的许多领域，例如在使用脉冲传输时。
定时分配：   另一个锁相环应用是在数字逻辑电路和系统中分配精确定时的时钟脉冲，例如在微处理器系统内。
锁相环基本概念——相位
锁相环 PLL 工作的关键是两个信号之间的相位差，以及检测它的能力。然后使用关于两个信号之间的相位误差或相位差的信息来控制环路的频率。

为了更多地了解相位和相位差的概念，可以将两个波形可视化，通常被视为正弦波，就像它们可能出现在示波器上一样。如果同时触发两个信号的触发器，它们将出现在屏幕上的不同点。

线性图也可以用圆圈的形式表示。循环的开始可以表示为圆上的一个特定点，随着时间的推移，波形上的点会围绕圆移动。因此一个完整的周期相当于 360° 或 2π 弧度。圆圈上的瞬时位置代表在给定时刻相对于循环开始的相位。

正弦波上点的相位角
正弦波上点的相位角
相位差的概念使这个概念更进一步。虽然我们之前看到的两个信号具有相同的频率，但波峰和波谷并不出现在同一个地方。

据说两个信号之间存在相位差。该相位差被测量为它们之间的角度。可以看出，它是两个波形上同一点之间的夹角。在这种情况下，已采用零交叉点，但只要两者相同，任何点都足够了。

这种相位差也可以用圆圈表示，因为由于相位差，两个波形将位于周期上的不同点。以角度测量的相位差：它是从圆心到表示波形的点的两条线之间的角度。

两个信号之间的相位差
信号之间的相位差
当两个信号具有不同的频率时，发现两个信号之间的相位差总是在变化的。这样做的原因是每个周期的时间不同，因此它们以不同的速度绕着圆圈移动。

由此可以推断，两个完全相同频率的信号的定义是它们之间的相位差是恒定的。两个信号之间可能存在相位差。这仅意味着它们不会同时到达波形上的同一点。如果相位差是固定的，则意味着一个信号落后或领先另一个信号相同的量，即它们处于相同的频率。

锁相环基础知识
锁相环，PLL，基本上是伺服环的形式。尽管 PLL 对射频信号执行其操作，但环路稳定性和其他参数的所有基本标准都是相同的。通过这种方式，可以将相同的理论应用于锁相环，就像应用于伺服环一样。

基本锁相环基本图
基本锁相环基本图
基本锁相环 PLL 由三个基本元素组成：

相位比较器/检测器：   顾名思义，PLL内的这个电路块比较两个信号的相位，并根据两个信号之间的相位差产生电压。该电路可以采用多种形式。   . . . . 阅读有关相位检测器的更多信息。
压控振荡器，VCO：   压控振荡器是产生射频信号的电路块，通常被认为是环路的输出。其频率可以在环路所需的操作频带内进行控制。  . . . . 阅读有关 压控振荡器 VCO 的更多信息。
环路滤波器：   该滤波器用于对锁相环 PLL 中的相位比较器的输出进行滤波。它用于从 VCO 线路中去除正在对其相位进行比较的信号的任何分量，即参考和 VCO 输入。它还控制回路的许多特性，包括回路稳定性、锁定速度等   。. . . 阅读有关 PLL 环路滤波器的更多信息。
锁相环操作
锁相环运算的基本概念比较简单，虽然其运算的数学分析和许多要素相当复杂

基本锁相环图显示了 PLL 的三个主要元件：相位检测器、压控振荡器和环路滤波器。

在基本 PLL 中，参考信号和来自压控振荡器的信号连接到鉴相器的两个输入端口。鉴相器的输出被传递到环路滤波器，然后滤波后的信号被施加到压控振荡器。

显示电压的锁相环
显示电压的锁相环图
PLL 内的压控振荡器 VCO 产生进入相位检测器的信号。在这里，来自 VCO 的信号的相位与输入的参考信号进行比较，并产生最终的差异或误差电压。这对应于两个信号之间的相位差。

来自相位检测器的误差信号通过一个低通滤波器，该滤波器控制环路的许多特性并去除信号上的任何高频元素。一旦通过滤波器，误差信号就会作为其调谐电压施加到 VCO 的控制端。该电压的任何变化的意义在于它试图降低相位差，从而降低两个信号之间的频率。最初环路将失锁，误差电压会将 VCO 的频率拉向参考频率，直到它无法进一步降低误差并且环路被锁定。

当 PLL（锁相环）处于锁定状态时，会产生一个稳态误差电压。通过在相位检测器和 VCO 之间使用放大器，信号之间的实际误差可以降低到非常小的水平。然而，在 VCO 的控制端子上必须始终存在一些电压，因为这会产生正确的频率。

存在稳定误差电压的事实意味着参考信号和 VCO 之间的相位差没有变化。由于这两个信号之间的相位没有变化，这意味着这两个信号的频率完全相同。



锁相环 PLL 是一个非常有用的构建块，特别是对于射频应用。PLL 构成了许多 RF 系统的基础，包括间接频率合成器、FM 解调器的一种形式，它能够从脉冲波形中恢复稳定的连续载波。这样，锁相环 PLL 是必不可少的 RF 构建工具。

https://www.electronics-notes.com/articles/radio/pll-phase-locked-loop/tutorial-primer-basics.php 