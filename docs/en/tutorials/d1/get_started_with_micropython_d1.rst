Get started with MicroPython [D1/D1 mini series]
=======================================================

Flash MicroPython firmware
----------------------------

The boards were already flashed micropython firmware.
If they lost firmware or you need lastest firmware, 
you can flash MicroPython firmware by yourself.

Requirements
************************

  * `Python <https://www.python.org/downloads/>`_
  * `esptool <https://github.com/espressif/esptool>`_ (for flash esp8266&esp32 firmware.)
      
    .. highlight:: bash

    ::

      pip install esptool

  * `Micropython firmware <https://micropython.org/download#esp8266>`_ (esp8266)

Additional Requirement for Mac OS X <10.14 (Mojave)
************************

  * :doc:`../../ch340_driver`

Flash firmware
************************

.. highlight:: bash

::

    esptool.py --port PORT_NAME erase_flash
    esptool.py --port PORT_NAME --baud 1000000 write_flash --flash_size=4MB -fm dio 0 FIRMWARE.bin  

.. note::  
  Don't forget to change **PORT_NAME** and **FIRMWARE.bin**.
  
  In Linux, **PORT_NAME** is like /dev/ttyUSB0.
  In windows, **PORT_NAME** is like COM4.


Quick reference
-------------------------
  * `Quick reference for the ESP8266 <https://docs.micropython.org/en/latest/esp8266/quickref.html>`_
  


