.. _stool:

支持工具
-----------
``Support Tools``

.. note::
    智能硬件开发的关键：硬件方案、软件架构和开发工具；软硬件方案解耦和工具通用是项目持续迭代的关键。

.. list-table::
    :header-rows:  1

    * -
      - 网络
      - 接口
      - USB
      - 测量
      - 供电
      - 相机
      - 调试
    * - :ref:`joint`
      - WiFi/ETH
      - √
      - √
      - X
      - 外接
      - X
      - √
    * - :ref:`torch`
      - WiFi
      - X
      - FS OTG
      - √
      - 电池
      - √
      - √
    * - :ref:`scope`
      - ETH
      - X
      - HS OTG
      - √
      - 外接
      - √
      - √


.. toctree::
    :maxdepth: 1

    转换工具 <joint>
    测试工具 <scope>
    诊断工具 <torch>
