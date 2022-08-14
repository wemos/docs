Get started with MicroPython [S3 series]
=======================================================

Flash MicroPython firmware
----------------------------

The boards were already flashed micropython firmware.
If they lost firmware or you need lastest firmware, 
you can flash MicroPython firmware by yourself.

Requirements
---------------

* :doc:`../../ch340_driver`
* `Python <https://www.python.org/downloads/>`_
* `esptool <https://github.com/espressif/esptool>`_ 
    
.. highlight:: bash

::

      pip install esptool
      
S3 Firmware
------------------

* `S3 Firmware <https://micropython.org/download/>`_
  



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
  


