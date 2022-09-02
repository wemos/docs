Get started with CircuitPython [C3 series]
=======================================================

Flash CircuitPython firmware
----------------------------

Requirements
---------------

* `Python <https://www.python.org/downloads/>`_
* `esptool <https://github.com/espressif/esptool>`_ (for flash esp32-c3 firmware.)
    
.. highlight:: bash

::

      pip install esptool
      
S2 Firmware
------------------

* `Firmware <https://circuitpython.org/downloads?q=lolin+c3>`_


Flash firmware
-------------------
* Make S2 boards into **Device Firmware Upgrade (DFU)** mode.

  * Press and hold the **[9]** Button
  * Press and release the  **[Reset]** Button
  * Release the **[9]** Button

* Flash using esptool.py

  .. highlight:: bash

  ::

    esptool.py --chip esp32c3 --port PORT_NAME --baud 1000000 write_flash -z 0x0 FIRMWARE.bin

.. note::  
  Don't forget to change **PORT_NAME** and **FIRMWARE.bin**.
  
  In Linux, **PORT_NAME** is like /dev/ttyUSB0.
  In windows, **PORT_NAME** is like COM4.


Quick reference
-------------------------
* `Welcome To CircuitPython <https://learn.adafruit.com/welcome-to-circuitpython>`_
  


