D1 mini Pro
=====================

==================  ==================  
 |TOP_IMG|_           |BOTTOM_IMG|_  
==================  ==================

.. |TOP_IMG| image:: ../_static/boards/d1_mini_pro_v2.0.0_1_16x16.jpg
.. _TOP_IMG: ../_static/boards/d1_mini_pro_v2.0.0_1_16x16.jpg

.. |BOTTOM_IMG| image:: ../_static/boards/d1_mini_pro_v2.0.0_2_16x16.jpg
.. _BOTTOM_IMG: ../_static/boards/d1_mini_pro_v2.0.0_2_16x16.jpg



A mini wifi board with 16MB flash, external antenna connector and built-in ceramic antenna based on ESP-8266EX.
`[Buy it] <https://www.aliexpress.com/store/product/WEMOS-D1-mini-Pro-16M-bytes-external-antenna-connector-ESP8266-WIFI-Internet-of-Things-development-board/1331105_32724692514.html>`_

Features
------------------

  * 11 digital input/output pins
  * Interrupt/pwm/I2C/one-wire
  * 1 analog input(3.2V max input)
  * 16M bytes(128M bit) Flash
  * External antenna connector
  * Built-in PCB antenna
  * Lithium battery interface, 500mA Max charging current
  * LOLIN I2C Port
  * Compatible with Arduino, MicroPython, NodeMCU
  * Default firmware: lastest MicroPython

Tutorials
----------------------
  * :doc:`../tutorials/micropython`
  * :doc:`../tutorials/arduino`

Documentation
----------------------
  * `Schematic V2.0.0[PDF] <../_static/files/sch_d1_mini_pro_v2.0.0.pdf>`_
  * `Dimension V2.0.0[PDF] <../_static/files/dim_d1_mini_pro_v2.0.0.pdf>`_
  * :doc:`../ch340_driver`

Technical specs
----------------------
+------------------------+------------+
| Operating Voltage      | 3.3V       |
+------------------------+------------+
| Digital I/O Pins       | 11         |
+------------------------+------------+
| Analog Input Pins      | 1(3.2V Max)|
+------------------------+------------+
| Clock Speed            | 80/160MHz  |
+------------------------+------------+
| Flash                  | 16M Bytes  |
+------------------------+------------+
| Size                   | 48*25.4mm  |
+------------------------+------------+
| Weight                 | 4.5g       |
+------------------------+------------+

Pin
----------------------
+------+------------------------------+--------------+
| Pin  | Function                     | ESP-8266 Pin |
+======+==============================+==============+
| TX   | TXD                          | TXD          |
+------+------------------------------+--------------+
| RX   | RXD                          | RXD          |
+------+------------------------------+--------------+
| A0   | Analog input, max 3.2V       | A0           |
+------+------------------------------+--------------+
| D0   | IO                           | GPIO16       |
+------+------------------------------+--------------+
| D1   | IO, SCL                      | GPIO5        |
+------+------------------------------+--------------+
| D2   | IO, SDA                      | GPIO4        |
+------+------------------------------+--------------+
| D3   | IO, 10k Pull-up              | GPIO0        |
+------+------------------------------+--------------+
| D4   | IO, 10k Pull-up, BUILTIN_LED | GPIO2        |
+------+------------------------------+--------------+
| D5   | IO, SCK                      | GPIO14       |
+------+------------------------------+--------------+
| D6   | IO, MISO                     | GPIO12       |
+------+------------------------------+--------------+
| D7   | IO, MOSI                     | GPIO13       |
+------+------------------------------+--------------+
| D8   | IO, 10k Pull-down, SS        | GPIO15       |
+------+------------------------------+--------------+
| G    | Ground                       | GND          |
+------+------------------------------+--------------+
| 5V   | 5V                           | \-           |
+------+------------------------------+--------------+
| 3V3  | 3.3V                         | 3.3V         |
+------+------------------------------+--------------+
| RST  | Reset                        | RST          |
+------+------------------------------+--------------+

.. note:: All of the IO pins run at 3.3V.

Version
----------------------
  * V2.0.0 (current version)
  * V1.1.0
  * V1.0.0
