HR8833 Motor Shield
===========================

==================  ==================  
 |TOP_IMG|_           |BOTTOM_IMG|_  
==================  ==================

.. |TOP_IMG| image:: ../_static/d1_shields/hr8833_v1.0.0_1_16x16.jpg
.. _TOP_IMG: ../_static/d1_shields/hr8833_v1.0.0_1_16x16.jpg

.. |BOTTOM_IMG| image:: ../_static/d1_shields/hr8833_v1.0.0_2_16x16.jpg
.. _BOTTOM_IMG: ../_static/d1_shields/hr8833_v1.0.0_2_16x16.jpg

I2C dual motor driver shield based on HR8833.
`[Buy it]`_

.. _[Buy it]: https://www.aliexpress.com/item/1005003697301523.html

Features
---------------------

  * I2C interface
  * Power supply voltage: VM=3-10V
  * Output current: Iout=1.5A(average) / 2.5A (peak)
  * CW/CCW/short brake/stop motor control modes

Pins
----------------------

===========    ===========    ===========
**D1 mini**    **GPIO**       **Shield**
D1             5              SCL
D2             4              SDA
===========    ===========    ===========

  * **VM:** Motor power supply + (3-10VDC)
  * **GND:** Motor power supply -
  * **1-A-2:** Motor A
  * **2-B-1:** Motor B

Documents
-----------------------

  * `Schematic v1.0.0 [PDF]`_

.. _Schematic v1.0.0 [PDF]: ../_static/files/sch_hr8833_v1.0.0.pdf




Arduino
------------------------

  * Install `LOLIN_I2C_MOTOR_Library`_
  * `Arduino Examples`_


.. _LOLIN_I2C_MOTOR_Library: https://github.com/wemos/LOLIN_I2C_MOTOR_Library
.. _Arduino Examples: https://github.com/wemos/LOLIN_I2C_MOTOR_Library/tree/master/examples

   








