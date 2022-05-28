.. _stool:

STool
===============
``Wi-Fi`` ``USB OTG``

在新一轮的嵌入式开发升级中，需要改变以往重环境的现状，标准化环境的灵活部署和协同，云加速及相应硬件端的搭配，实现嵌入式开发的远程化。

* 绑定远端IP实现本地设备调试开发
* 通过地址拉取相应固件并针对下载
* 直接按照编译文件的地址进行烧录


.. list-table::
    :header-rows:  1

    * - Tools
      - CoreMark
      - USB
      - Network
      - Camera
      - OPA
      - ADC
      - DAC
    * - :ref:`stool`
      - 1181(240M)
      - FS(OTG)
      - WiFi 4
      - DVP
      -
      - 2x12bit(100KSPS)
      - 0
    * - :ref:`vtool`
      - 400(144M)
      - HS+FS(OTG)
      - 1Gbps
      - DVP
      - 4
      - 2x12bit(1MSPS)
      - 2x12bit
    * - :ref:`htool`
      - 2778(550M)
      - HS(OTG)
      - 100Mbps
      - PSSI
      - 2
      - 2x16bit(3.6MSPS)
      - 2x12bit(5MSPS)



.. _htool:

HTool
------------------
``Cortex-M7`` ``550MHz`` ``5MSPS-12bit-DAC`` ``3.6MSPS-16bit-ADC`` ``PSSI``


.. _vtool:

VTool
------------------
``RISC-V`` ``USB-HS(480Mbps)`` ``10Mbps(PHY)`` ``1Gbps(MAC)`` ``FSMC`` ``OPA`` ``DVP``



.. hint::
    WiFi/BLE连接 :ref:`stool` 探针，USB/ETH连接 :ref:`vtool` 探针，:ref:`htool` 采集高速信号并处理传输

