Get started with MicroPython
=================================

Requirements
---------------
  * :doc:`../ch340_driver`
  * `Python <https://www.python.org/downloads/>`_
  * `esptool <https://github.com/espressif/esptool>`_ (for flash esp8266&esp32 firmware.)
  * w600tool

MicroPython firmware
------------------------

Choose the right firmware:
  * `D1 mini/D1 mini Pro firmware <https://micropython.org/download#esp8266>`_ (esp8266)
  * `D32/D32 Pro firmware <https://micropython.org/download#esp32>`_ (esp32)(*D32 Pro cloud use Firmware with SPIRAM support*)
  * w600 firmware (W600-Pico)

Flash firmware
------------------------

.. note::  Don't forget to change **YOUR_PORT_NAME** and **YOUR_FIRMWARE.bin**. In Linux, **YOUR_PORT_NAME** is like /dev/ttyUSB0. In windows, **YOUR_PORT_NAME** is like COM4.


D1 mini
*********************

.. prompt:: bash $

    esptool.py --port YOUR_PORT_NAME erase_flash
    esptool.py --port YOUR_PORT_NAME --baud 1000000 write_flash --flash_size=4MB -fm qio 0 YOUR_FIRMWARE.bin

D32/D32 Pro
*******************

.. prompt:: bash $

    esptool.py --port YOUR_PORT_NAME erase_flash
    esptool.py --port YOUR_PORT_NAME --baud 1000000 write_flash -z 0x1000 YOUR_FIRMWARE.bin



W600-Pico
*******************



