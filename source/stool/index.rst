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
      - :ref:`stool_dvp`
      - DAC
      - :ref:`stool_jtag`
      - :ref:`stool_swd`
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

.. _stool_s:

S Series
-----------

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

.. _stool_c:

C Series
-----------

.. _stool_c1:

STool-C1
~~~~~~~~~~~
``CH579`` ``BLE`` ``ETH`` ``USB`` ``JTAG`` ``SWD``


.. _stool_c2:

STool-C2
~~~~~~~~~~~
``CH32F208`` ``BLE`` ``ETH`` ``USB`` ``JTAG`` ``SWD``


.. _stool_c3:

STool-C3
~~~~~~~~~~~
``CH32F207`` ``ETH`` ``USB`` ``JTAG`` ``SWD`` ``DVP``

.. _stool_cam:

Camera IF
-----------

.. _stool_dvp:

DVP
~~~~~~~~~~~



.. _stool_debug:

Debug IF
-----------

.. _stool_jtag:

JTAG
~~~~~~~~~~~

JTAG(Joint Test Action Group；联合测试工作组)是一种国际标准测试协议（IEEE 1149.1兼容），主要用于芯片内部测试。现在多数的高级器件都支持JTAG协议，如DSP、FPGA器件等。标准的JTAG接口是4线：TMS、TCK、TDI、TDO，分别为模式选择、时钟、数据输入和数据输出线。

JTAG是一种IEEE标准用来解决板级问题，开发于上个世纪80年代。今天JTAG被用来烧录、debug、探查端口。当然，最原始的使用是边界测试。


JTAG调试接口必须使用VCC、GND电源信号，以及TMS、TCK、TDI、TDO四根调试信号，可选TRST、RESET复位信号和RTCK（同步时钟）信号。

* TDI：测试数据输入，数据通过TDI输入JTAG口；
* TDO：测试数据输出，数据通过TDO从JTAG口输出；
* TMS：测试模式选择，用来设置JTAG口处于某种特定的测试模式；
* TCK：测试时钟输入；
* TRST：测试复位；
* VRef：目标板参考电压信号。用于检查目标板是否供电，直接与目标板VDD联，并不向外输出电压；
* TRST：JTAG复位，连接到目标CPU的nTRST引脚，用于复位CPU调试接口的TAP控制器；目标板上应将此脚上拉到高电位，避免意外复位；

虽然TRST、RESET是可选的信号；但一般都建议接上，使得仿真器能够在连接器件前对器件进行复位，以获得较理想的初始状态，便于后续仿真。


.. _stool_swd:

SWD
~~~~~~~~~~~

SWD是ARM公司提出的另一种调试接口，相对于JTAG接口，使用更少的信号。

* SWDIO：串行数据输入输出，作为仿真信号的双向数据信号线，建议上拉；
* SWCLK：串行时钟输入，作为仿真信号的时钟信号线，建议下拉；
* SWO：串行数据输出引脚，CPU调试接口可通过SWO引脚输出一些调试信息。该引脚是可选的；
* RESET：仿真器输出至目标CPU的系统复位信号。
* VRef：目标板参考电压信号。用于检查目标板是否供电，直接与目标板VDD联，并不向外输出电压；
* GND：公共地信号；

同样的，虽然RESET是可选的信号；但一般都建议接上，使得仿真器能够在连接器件前对器件进行复位，以获得较理想的初始状态，便于后续连接仿真。

SWD模式比JTAG在高速模式下面更加可靠。在大数据量的情况下面JTAG下载程序会失败，但是SWD发生的几率会小很多。基本使用JTAG仿真模式的情况下是可以直接使用SWD模式的，只要你的仿真器支持。
