Get started with MicroPython [D32 series]
=======================================================

Flash MicroPython firmware
----------------------------

The boards were already flashed micropython firmware.
If they lost firmware or you need lasted firmware, 
you can flash MicroPython firmware by yourself.

Requirements
************************

  * :doc:`../../ch340_driver`
  * `Python <https://www.python.org/downloads/>`_
  * `esptool <https://github.com/espressif/esptool>`_ (for flash esp8266&esp32 firmware.)
  * `Micropython firmware <https://micropython.org/download#esp32>`_ (esp32)

  .. note::
    D32 Pro cloud use Firmware with SPIRAM support

Flash firmware
************************

.. prompt:: bash $

    esptool.py --port PORT_NAME erase_flash
    esptool.py --port PORT_NAME --baud 1000000 write_flash -z 0x1000 FIRMWARE.bin

.. note::  
  Don't forget to change **PORT_NAME** and **FIRMWARE.bin**.
  
  In Linux, **PORT_NAME** is like /dev/ttyUSB0.
  In windows, **PORT_NAME** is like COM4.


Quick reference
-------------------------
  * `Quick reference for the ESP32 <https://docs.micropython.org/en/latest/esp32/quickref.html>`_
  


