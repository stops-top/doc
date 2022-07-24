
.. _usbc:

USBC
===============

``USB-C`` ``USB-PD`` ``SWD`` ``UART``


`USBC 应用场景 <https://special.wch.cn/zh_cn/type-c_application_index/>`_

.. contents::
    :local:
    :depth: 1


应用场景
-----------

.. contents::
    :local:
    :depth: 1

设备调试
~~~~~~~~~~~

标准接插端子中具备多通道，可以单线实现USB连接和UART连接，不需要再找端口找接线

设备部署
~~~~~~~~~~~

具备通信和供电能力，可以对设备进行供电，同时采集设备运行数据，转换相应的通信数据



标准接口
-----------

USB（Universal Serial Bus）支持热插拔，协议版本有USB1.0、USB1.1、USB2.0、USB3.1等，USB2.0目前比较常用。

.. toctree::
    :maxdepth: 1

    USB简介  <usb>

* USB Type-C：8.3mmx2.50mm
* Micro USB：7.4mmx2.35mm
* Lightning：7.5mmx2.50mm


常见主板的接口标识：

* 带有USB标识：表示支持USB2.0，普通的速率480Mb/s；
* 带有USB标识，外加SS字样：表示支持USB3.1，速率5Gb/s；
* 带有USB标识，外加SS字样，右上角多了数字10：表示支持USB3.1，速率10Gb/s；
* 带有USB标识，外加SS字样，右上角多了数字10，右边增加D字样：表示支持USB3.1，速率10Gb/s，支持视频显示;
* 带有USB标识，且有一个黑色的背景：全部支持PD协议，其中5Gb/s的字体为白色

接口定义
~~~~~~~~~~~

type-c接口的各种特性使用，包括PD和视频信号输出，通过DEMUX电路实现更多功能的集成和智能的选择使能，该单元是可编程控制单元，有自己的协议和相应的管理范围。

USB Type-C是一个全新的正反插USB连接器规范，能够支持USB 3.1（Gen1和Gen2）、Display Port和USB PD等一系列新标准，最高速率可达10Gbps，Type-C端口默认最高可支持5V3A。

USB PD是BMC编码的信号，而之前的USB则是FSK。

.. image:: ./images/USBC.jpg
    :target: https://baike.baidu.com/item/USB%20Type-C/16565059?fr=aladdin

USB PD是在CC pin上传输，PD有个VDM （Vendor defined message）功能，定义了装置端ID，读到支持DP或PCIe的装置，DFP就进入替代（alternate）模式。

如果DFP认到device为DP，便切换MUX/ConfiguraTIon Switch，让Type-C USB3.1信号脚改为传输DP信号。AUX辅助由Type-C的SBU1，SUB2来传。HPD是检测脚，和CC差不多，所以共用。

而DP有lane0-3四组差分信号， Type-C有RX/TX1-2也是四组差分信号，所以完全替代没问题。而且在DP协议里的替代模式，可以USB信号和DP信号同时传输，RX/TX1传输USB数据，RX/TX2替换为lane0，1两组数据传输，此时可支持到4k。

如果DFP认到device为DP，便切换MUX/ConfiguraTIon Switch，让Type-C USB3.1信号脚改为传输PCIe信号。同样的，PCIe使用RX/TX2和SBU1，SUB2来传输数据，RX/TX1传输USB数据。



CC(Configuration Channel)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

配置通道，这是USB Type-C里新增的关键通道。它的作用有检测正反插，检测USB连接识别可以提供多大的电压和电流，USB设备间数据与VBUS的连接建立与管理等。

DFP(Downstream Facing Port)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

下行端口，可以理解为Host，DFP提供VBUS，可以提供数据。在协议规范中DFP特指数据的下行传输，笼统意义上指的是数据下行和对外提供电源的设备。典型的DFP设备是电源适配器。

UFP(Upstream Facing Port)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

上行端口，可以理解为Device，UFP从VBUS中取电，并可提供数据。典型设备是U盘，移动硬盘。

DRP(Dual Role Port)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

双角色端口，DRP既可以做DFP(Host)，也可以做UFP(Device)，也可以在DFP与UFP间动态切换。典型的DRP设备是笔记本电脑。


线缆品类
-----------

.. contents::
    :local:
    :depth: 1

WiFi通信
~~~~~~~~~~~

用于扩展原有设备的WiFi通信能力

以太网通信
~~~~~~~~~~~

用于扩展原有设备的以太网通信能力

RS485通信
~~~~~~~~~~~

用于扩展原有设备的RS485通信能力


.. include:: stopi.rst
