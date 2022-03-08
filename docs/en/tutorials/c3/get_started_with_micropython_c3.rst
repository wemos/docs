Get started with MicroPython [C3 series]
=======================================================

Flash MicroPython firmware
----------------------------

The boards were already flashed micropython firmware.
If they lost firmware or you need lastest firmware, 
you can flash MicroPython firmware by yourself.

Requirements
---------------

* `Python <https://www.python.org/downloads/>`_
* `esptool <https://github.com/espressif/esptool>`_ (for flash ESP32-C3 firmware.)
    
.. highlight:: bash

::

      pip install esptool
      
S2 MINI Firmware
------------------
* `c3_mini_micropython_v1.16.bin <../../_static/files/c3_mini_firmware/c3_mini_micropython_v1.16.bin>`_
  



Flash firmware
-------------------
* Make S2 boards into **Device Firmware Upgrade (DFU)** mode.

  * Hold on **Button 9**
  * Press **Button Reset**
  * Release **Button 9** When you hear the prompt tone on usb reconnection

* Flash using esptool.py

  .. highlight:: bash

  ::

    esptool.py --port PORT_NAME erase_flash
    esptool.py --port PORT_NAME --baud 1000000 write_flash -z 0 FIRMWARE.bin

.. note::  
  Don't forget to change **PORT_NAME** and **FIRMWARE.bin**.
  
  In Linux, **PORT_NAME** is like /dev/ttyUSB0.
  In windows, **PORT_NAME** is like COM4.


Quick reference
-------------------------
* `Quick reference for the ESP32 <https://docs.micropython.org/en/latest/esp32/quickref.html>`_
  

