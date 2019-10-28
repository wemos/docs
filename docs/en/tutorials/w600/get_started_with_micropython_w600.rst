Get started with MicroPython [W600 series]
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
  * `w600tool <https://github.com/wemos/w600tool>`_ (for flash w600 firmware)
  * `Micropython firmware v1.10 <http://www.winnermicro.com/upload/1/editor/1568709203932.zip>`_



Flash firmware
************************

.. highlight:: bash

::

  w600tool.py -p PORT_NAME --upload-baud 2000000 --upload FIRMWARE.fls



.. note::  
  Don't forget to change **PORT_NAME** and **FIRMWARE.fls**.
  
  In Linux, **PORT_NAME** is like /dev/ttyUSB0.
  In windows, **PORT_NAME** is like COM4.


Quick reference
-------------------------
  * Quick reference for the w600
  


