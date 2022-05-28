.. _stool:

STool
===============
``Wi-Fi`` ``USB`` ``JTAG``

相关开发逐步上云，但是能够连接云端进行烧录和调试的工具缺乏，不同操作系统对于硬件的支持不同，多系统环境或容器环境下适配差；

如何通过边云协同绑定，实现嵌入式硬件开发的CICD同步，无人干预的自动化测试集成，远程管理服务减少运营成本；

* 绑定远端IP实现本地设备调试开发
* 通过地址拉取相应固件并针对下载
* 直接按照编译文件的地址进行烧录

.. list-table::
    :header-rows:  1

    * - :ref:`stool`
      - WiFi
      - BLE
      - ETH
      - USB
      - DVP
      - DAC
      - JTAG
      - SWD
    * - :ref:`stool_s1`
      - √
      - √
      - √
      - X
      - √
      - √
      - √
      - X
    * - :ref:`stool_s2`
      - √
      - X
      - X
      - √
      - √
      - √
      - √
      - X
    * - :ref:`stool_s3`
      - √
      - √
      - X
      - √
      - √
      - X
      - √
      - X
    * - :ref:`stool_c1`
      - X
      - √
      - √
      - √
      - X
      - X
      - X
      - √
    * - :ref:`stool_c2`
      - X
      - √
      - √
      - √
      - X
      - X
      - X
      - √
    * - :ref:`stool_c3`
      - X
      - X
      - √
      - √
      - √
      - √
      - X
      - √


.. contents::
    :local:
    :depth: 1

.. _stool_s1:

STool-S1
-----------
``ESP32`` ``Wi-Fi`` ``BLE`` ``ETH`` ``JTAG`` ``DVP``

.. _stool_s2:

STool-S2
-----------
``ESP32-S2`` ``Wi-Fi`` ``USB`` ``JTAG`` ``DVP`` ``DAC``

.. _stool_s3:

STool-S3
-----------
``ESP32-S3`` ``Wi-Fi`` ``BLE`` ``USB`` ``JTAG`` ``DVP``


.. _stool_c1:

STool-C1
-----------
``CH579`` ``BLE`` ``ETH`` ``USB`` ``JTAG`` ``SWD``


.. _stool_c2:

STool-C2
-----------
``CH32F208`` ``BLE`` ``ETH`` ``USB`` ``JTAG`` ``SWD``


.. _stool_c3:

STool-C3
-----------
``CH32F207`` ``ETH`` ``USB`` ``JTAG`` ``SWD`` ``DVP``
