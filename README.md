# Quant-MovingAverage
> First-time Quant code test. Featured with rational thinking and careful design.

```
考虑某一时间序列P，每过一段时间我们能获得一对数(t, Pt)，分别为当前的时间戳t和当前取值Pt，需要计算该序列在[t-W, t]时间段内的平均取值，
其中W是事先给定的窗口大小，单位和t相同。

算法需要满足以下要求：

1. 相邻数据点之间的间隔不固定，可能有较大变化，在计算的时候应考虑数据间隔变化极端的情况下的鲁棒性;
2. 计算的平均取值应能较好反映序列在窗口时间内的“平均水平”
3. 假设在相邻两次数据到达期间内，序列的真实取值都等于前一次数据的值
4. 所谓平均水平指的是序列在窗口内的简单移动平均（SMA）而不是指数移动平均（EMA）
5. 可用的内存大小是有限的，为O(num_bin)规模，当窗口内到达的数据量超过可用的存储空间时，应做一定的取舍，既不突破内存限制，又尽可能保证结果的精确性（只是简单地把尾部数据删除是不行的）
6. 尽量使用性能较优的算法和实现方法

num_bin: 使用的内存大小应为O(num_bin)级别
window：移动平均的窗口长度
timestamp是时间戳，浮点数，数据间隔不固定，可能一秒来几十个数据，也可能几小时来一个数据
```
