# HVDP_8091  
基于GS8091的高压差分探头  
High Voltage Differential Probe base on GS8091  
https://circuitcellar.com/research-design-hub/high-voltage-differential-probe/  
对比原设计，改进了：  
1.运放换成国产货GS8091，便宜了很多，虽然带宽也小了很多，用了一堆0.1%低温漂电阻，C0G电容总成本也低于30块  
2.添加2k电阻补偿输入线电感，  
  麦科信的探头的做法是在电容里面串2.2k电阻，仿真结果类似。在P5205上面找不到类似的电阻。  
3.添加2.5欧电阻，增加了一点点带宽，虽然牺牲了幅频特性曲线平坦度  
  麦科信的探头在低端分压电容上面串了100欧电阻，而P5205只在可调电容上串电阻。  
  仿真能看到麦科信的做法会在高频有很大的幅值响应，应该是牺牲了幅频特性曲线的平坦度把带宽拉上去了，不讲武德。  
4.仿真可得后级运放的电阻上并联电容能增加了一点点带宽，实际上会有100MHZ左右的震荡。  
5.为了适配运放的共模输入范围，电源改成LDO出3.3V，34063出-1.8V，便宜了很多，用RC+LC滤波器，纹波还勉强，用二阶LC纹波更大  
6.把运放改成TPH2501，噪声小了一点，100X时900mVpp，500X时1.8Vpp。实际带宽应该超过10MHz。  

![SDS00014](https://user-images.githubusercontent.com/33488997/159395833-b3ff02b7-5d15-4577-8093-3d532e222d59.png)  
![SDS00015](https://user-images.githubusercontent.com/33488997/159395877-71a513a5-425b-4770-947f-e6c24aafe02d.png)
