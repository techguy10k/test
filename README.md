﻿# STM32H7 HAL DAC+ADC+FFT(Hanning)
 这是STM32H7 DAC任意波发生器+DMA法ADC采样+RFFT的HAL库实现的工程  
 工程中生成DAC点数的方法为运行时打点而非运行前打点  
 **经过测试发现STM32H7打两个sin函数叠加的点250点需要花费1.1ms时间(用的是通用math函数，而不是arm的快速math函数)**  
 **意思是如果用STM32F1系列单片机的话，由于计算性能不足会无法运行时打点**  
 **对于STM32F1系列的单片机而言还是在程序编译阶段把信号的一个周期存入CODE区来的好**  
 ****
  **另外，需要注意的是 由于HAL库太大不方便放到GitHub托管 使用者需要自行在工程根目录中添加完整的HAL驱动**  
  **工程目录结构的截图在项目中，请自行查看**
 **可以打开CubeMX配置软件让其自动生成代码 自动添加库文件**
  ****
## 硬件平台  
* STM32H743ZI Nucleo-144  
## 软件平台
* MDK5 + CubeMX  HAL Ver1.4
## 编译设置
* 采用ARMCLANG 也就是V6.12
* 采用CMSIS 5.1.2  
* 采用DSP   1.3
