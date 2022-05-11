
.. _vtool:

V-Tool
===============
``RISC-V`` ``USB-HS(480Mbps)`` ``10Mbps(PHY)`` ``1Gbps(MAC)`` ``FSMC`` ``OPA`` ``DVP``

`GitHub <https://github.com/stops-top/V-Tool>`_ : `CH32V305/CH32V307/CH32V208 <https://docs.SoC.xin/CH32V208>`_

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
