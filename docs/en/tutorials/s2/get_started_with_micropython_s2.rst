Get started with MicroPython [S2 series]
=======================================================

Flash MicroPython firmware
----------------------------

The boards were already flashed micropython firmware.
If they lost firmware or you need lastest firmware, 
you can flash MicroPython firmware by yourself.

Requirements
---------------

* `Python <https://www.python.org/downloads/>`_
* `esptool <https://github.com/espressif/esptool>`_ (for flash esp32-s2 firmware.)
    
.. highlight:: bash

::

      pip install esptool
      
S2 MINI Firmware
------------------
* `s2_mini_micropython_v1.16-200-g1b87e1793.bin <../../_static/files/s2_mini_firmware/s2_mini_micropython_v1.16-200-g1b87e1793.bin>`_
  



Flash firmware
-------------------
* Make S2 boards into flash mode.
* Flash using esptool.py

  .. highlight:: bash

  ::

    esptool.py --port PORT_NAME erase_flash
    esptool.py --port PORT_NAME --baud 1000000 write_flash -z 0x1000 FIRMWARE.bin

.. note::  
  Don't forget to change **PORT_NAME** and **FIRMWARE.bin**.
  
  In Linux, **PORT_NAME** is like /dev/ttyUSB0.
  In windows, **PORT_NAME** is like COM4.


Quick reference
-------------------------
* `Quick reference for the ESP32 <https://docs.micropython.org/en/latest/esp32/quickref.html>`_
  


