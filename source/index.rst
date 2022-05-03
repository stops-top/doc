
STOPs
==================

**出租车送到家，公交车送到站，方便和实惠都有光明的前途**

`STOPs <https://STOPs.top>`_ 求解如下问题：

* 如何提高开发效率，降低工程师的学习成本和诊断成本
* 如何提高生产效率，利用中间数据，优化迭代生产流程
* 如何提高使用体验，产品全生命周期管理，产品即服务
* 如何提高价值转换，细粒度的劳动成果交换和需求连接

针对不同平台的协同分工，大致的规划如下：

`SoC.Xin <https://docs.SoC.Xin>`_ 解决不知道用什么，中心是 ``芯片`` ，芯片既是最初级生产资料，动态更新和对比，推荐最佳方案、替换方案及替换必要性，通过实例和经典项目代码提供探索实践。

`OS-Q.com <https://docs.OS-Q.com>`_ 解决不知道有什么，中心是 ``资源`` ，聚焦开源生态和系统化集成，评价开源项目的实用价值，提供更多的探索方式和应用总结，在一定程度上构建替代梯度和兼容梯度。

`STOPs.top <https://www.STOPs.top>`_ 解决不知道干什么，中心是 ``需求`` ，产品定义和实现与产品制造推广分离，精细化分层分工，实现市场定价和资源互补，尤其是实现技术实力和资源实力的平等联姻。


.. toctree::
    :caption: Tools
    :maxdepth: 1

    无线工具 S3-Tool <s3>
    有线工具 V3-Tool <v3>
    综合工具 H3-Tool <h3>

.. list-table::
    :header-rows:  1

    * - Tools
      - CoreMark
      - USB
      - Network
      - UART
      - ADC
      - DAC
    * - :ref:`s3`
      - 1181
      - FS(OTG)
      - WiFi 4
      - 2
      - 2x12bit(100KSPS)
      - 0
    * - :ref:`v3`
      -
      - HS+FS(OTG)
      - 1Gbps
      - 8
      - 2x12bit(1MSPS)
      - 2x12bit
    * - :ref:`h3`
      - 2778
      - HS(OTG)
      - 100Mbps
      - 10
      - 2x16bit(3.6MSPS)
      - 2x12bit(5MSPS)

3系列的工具集差异化体现在场景上，通过无线连接的 :ref:`s3` 侧重于单点测试和烧录，:ref:`v3` 作为综合数据网关连接多设备，:ref:`h3` 用于模拟信号采集和处理传输

.. toctree::
    :caption: STOPi
    :maxdepth: 1

    硬件开发环境 PCI-E <pcie>
    集成控制板卡 NGFF <ngff>
    通信转换接头 USBC <usbc>
    标准测试中心 Qhub <qhub>


`STOPi <https://www.STOPi.cn>`_ 提供相应标准，实现高效统一的嵌入式开发生态。

