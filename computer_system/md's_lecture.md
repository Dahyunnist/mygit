### 这是浙江大学智云课堂上马德老师的《计算机组成》智云课程随笔，结合PPT吸收
### ***This course is about processor and instruction set, the latter of which is both a wall and a bridge between hardware and software.***
## Lecture 2
### Computer design: performance and idea(衡量处理器性能的指标和设计处理器的思路)

1. **Response time and Throughput:** 响应时间和吞吐量
   - 不是响应时间越短，吞吐量就越高; 
   - 版本越高，响应时间越短吞吐量越高； 
   - 多核可以提高吞吐量，但响应时间不一定降低
   - CPU的处理速度受时钟周期限制，而时钟周期不能无限缩短，必须不小于组合逻辑电路的传输延迟时间
<br/>

2. **量化表示**
   1. $CPU time= Clock\, Cycles \times Clock\, Cycle\, Time = \frac{Clock\, Cycles}{Clock\, Rate}$
        - Cycle Count 取决于组合逻辑的复杂度，
        - 设计时需要在 Clock Cycles 和 Clock Rate之间取舍
        > 以乘法为例，如果组合逻辑支持直接乘法，那么Cycle Count会下降（一个时钟周期就可以完成），但是Clock Rate也会下降（组合逻辑复杂度提升，时钟周期变长）；反之，如果组合逻辑仅支持加法，用连续加法实现乘法，那么时钟周期可以下降，但是Cycle Count会上升（需要多个时钟周期才能完成）
    2. $Clock\, Cycles = Instruction\, Count(IC) \times CPI (Cycles Per Instruction)$
     $\Rightarrow CPU time=  IC \times CPI \times Clock\, Cycle\, Time(T_c) = \frac{IC \times CPI}{Clock\, Rate}$
       - Instruction Count 和 ISA (Instruction Set Architecture 指令集架构)有关，相同ISA的电脑，执行同一个任务的Instruction Count相同
    3. Different instruction classes: $Clock Cycles=\sum_{i=1}^{n}{CPI_i\times IC_i}$
$\Rightarrow CPI=\frac{Clock \,Cycles}{IC}=\sum_{i=1}^{n}{(CPI_i \times \frac{IC_i}{IC})}$
   1. Performance Summary: $CPU time=\frac{IC}{Program}\times \frac{Clock \, Cycles}{Instruction}\times \frac{Seconds}{Clock \,cycle}$