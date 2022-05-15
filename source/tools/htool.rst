
.. _htool:

H-Tool
===============

``Cortex-M7`` ``550MHz`` ``5MSPS-12bit-DAC`` ``3.6MSPS-16bit-ADC`` ``PSSI``

`GitHub <https://github.com/stops-top/H-Tool>`_ : `STM32H730/STM32H7B0 <https://docs.SoC.xin/STM32H730>`_

H-Tool扩展 `H7-Tool <https://www.armbbs.cn/forum.php?mod=forumdisplay&fid=61&page=1>`_ 实现更多样化场景适配


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
