.. _stools:

外设工具
-----------
``Support Tools``

.. note::
    智能硬件开发的关键：硬件、软件和工具；软硬件方案解耦，工具通用是项目能持续迭代的关键。

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
      - 带宽
    * - :ref:`joint`
      -
      - √
      - √
      - X
      -
      - X
      - √
      -
    * - :ref:`torch`
      -
      - X
      - FS OTG
      - √
      - 电池
      - √
      - √
      -
    * - :ref:`scope`
      -
      - X
      - HS OTG
      - √
      - 外接
      - √
      - √
      -


.. toctree::
    :maxdepth: 1

    连接转换 <joint>
    分析测量 <scope>
    现场诊断 <torch>
