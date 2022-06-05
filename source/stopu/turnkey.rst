.. _turnkey:

Turnkey
============

一站式方案（Turnkey project，又称turn-key），是一种专案类型，指的是卖方将专案架设好并调整完成，在可立即使用的情况下卖给买家，是科技业中一种常见的技术转移方式。

从广义上说，Turnkey是一种设计、提供、安装完备随时可以使用的的产品或服务。用户只需要点击一下按钮就可以开始使用这个产品或服务了。


能量监测
-----------

基于市电输入和输出的信号实时处理，实现电能的计量和分析，包括电能质量和功率负载变化，通过信号处理分析识别各种状态。

.. contents::
    :local:
    :depth: 1


CCR
~~~~~~~~~~~
``Current Characteristics Recognition``

`CCR (Current Characteristics Recognition) <https://github.com/stops-top/CCR>`_ 将成熟的语音识别技术体系运用于电流特征分析，实现对电力负载特征判定


ADCNN
~~~~~~~~~~~
``CNN`` ``ADC`` ``MCU``

`ADCNN <https://github.com/tfmin/ADCNN>`_ 基于MCU的原始ADC数据实现CNN网络处理算法，对ADC的性能及MCU的算力有一定的要求

主控MCU采用 `先楫HPM6750 <https://docs.soc.xin/HPM6750>`_ 封装：LQFP144(14x14) 和 BGA116(7x7)

* 3390CoreMark
* 内置768KB SRAM。
* 3x 16bit-ADC @ 2Msps
* 实时以太网，支持IEEE1588，内置PHY的高速USB，多路CAN-FD及丰富的UART，SPI，I2C。

HPM6300产品系列范围宽广，包括600Mhz 的HPM6360版本，及性价比极高的200MHz入门级的HPM6330版本。

