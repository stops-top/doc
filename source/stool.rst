
.. _stool:

S-Tool
===============
``Wi-Fi`` ``USB OTG``

`GitHub <https://github.com/stops-top/S-Tool>`_ : `ESP32-S2/ESP32-S3 <https://docs.SoC.xin/ESP32-S3>`_

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

* 绑定远端IP实现本地设备调试开发
* 通过地址拉取相应固件并针对下载
* 直接按照编译文件的地址进行烧录
