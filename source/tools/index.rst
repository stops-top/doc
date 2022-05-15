.. _tools:

Tools
==================


==================  ==================  ==================  ==================
|无线探针|_          |有线探针|_         |信号探头|_          |综合测量|_
------------------  ------------------  ------------------  ------------------
`无线探针`_          `有线探针`_         `信号探头`_          `综合测量`_
==================  ==================  ==================  ==================

.. |有线探针| image:: ./images/contribute.png
.. _有线探针: tools/vtool.html

.. |信号探头| image:: ./images/guide.png
.. _信号探头: tools/atool.html

.. |无线探针| image:: ./images/espressif.png
.. _无线探针: tools/stool.html

.. |综合测量| image:: ./images/started.png
.. _综合测量: tools/htool.html

.. toctree::
    :maxdepth: 1

    有线探针 V-Tool <vtool>
    信号探头 A-Tool <atool>
    无线探针 S-Tool <stool>
    综合测量 H-Tool <htool>


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

.. hint::
    WiFi/BLE连接 :ref:`stool` 探针，USB/ETH连接 :ref:`vtool` 探针，:ref:`atool` 采集高精度模拟信号，:ref:`htool` 采集高速信号并处理传输

