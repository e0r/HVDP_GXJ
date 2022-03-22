# HVDP_8091
High Voltage Differential Probe base on GS8091
https://circuitcellar.com/research-design-hub/high-voltage-differential-probe/
用国产的GS8091做的，信号那部分的电阻全是0.1%低温漂的，总成本27块。
发现这效果意外的好，目前还没调好电容电阻，效果已经不错了。
百兆的高压探头完全可以用国产运放做，没必要用AD,TI的高价运放。
共模输入范围可以通过+3.3V,-1.8V电源解决。
现在就是插万用表笔后信号变形，还有噪声比较大，大概有200mVrms。
踩过的坑：
不要用二阶LC滤波器，用RC+LC效果更好。
本来想再做个500MHZ的探头的，就用普通运放+BF998交流耦合做跟随器，用AD或者TI的电流反馈放大器做差分转单端，
不过估计会非常难调。
