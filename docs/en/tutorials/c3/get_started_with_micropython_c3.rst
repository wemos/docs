Get started with MicroPython [C3 series]
=======================================================

Flash MicroPython firmware
----------------------------

The boards were already flashed with MicroPython firmware.
If they lost the firmware or you need the latest version, 
you can flash MicroPython firmware by yourself.

Requirements
---------------

* `Python <https://www.python.org/downloads/>`_
* `esptool <https://github.com/espressif/esptool>`_ (to flash ESP32-C3 firmware)
    
.. highlight:: bash

::

      pip3 install esptool
      
C3 MINI Firmware
------------------
* `c3_mini_micropython_v1.16.bin <../../_static/files/c3_mini_firmware/c3_mini_micropython_v1.16.bin>`_
  



Flash firmware
-------------------
* Put C3 boards into **Device Firmware Upgrade (DFU)** mode.

  * Hold **Button 9**
  * Press **Button Reset**
  * Release **Button 9** when you hear the prompt tone on USB reconnection

* Flash using esptool.py

  .. highlight:: bash

  ::

    esptool.py --port PORT_NAME erase_flash
    esptool.py --port PORT_NAME --baud 1000000 write_flash -z 0 FIRMWARE.bin

.. note::  
  Don't forget to change **PORT_NAME** and **FIRMWARE.bin**.
  
  In Linux, **PORT_NAME** is like /dev/ttyUSB0.
  In Windows, **PORT_NAME** is like COM4.


Quick reference
-------------------------
* `Quick reference for the ESP32 <https://docs.micropython.org/en/latest/esp32/quickref.html>`_
  


