Get started with MicroPython [C3 series]
=======================================================

Flash MicroPython firmware
----------------------------

The boards were already flashed with MicroPython firmware.
If they lost the firmware or if you need the latest version, 
you can flash MicroPython firmware yourself.

Requirements
---------------

* `Python <https://www.python.org/downloads/>`_
* `esptool <https://github.com/espressif/esptool>`_ (to flash ESP32-C3 firmware)
    
.. highlight:: bash

::

      pip3 install esptool
      
C3 Firmware
------------------

.. * `C3 Mini Firmware <https://micropython.org/download/LOLIN_C3_MINI/>`_

* `C3 Mini Firmware <https://github.com/wemos/micropython/releases/download/v1.16/firmware.bin>`_


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


WIFI
------------------
You need set WIFI Tx Power to 8.5dBm to use WIFI.

Use **sta_if.config(txpower=8.5)** after **sta_if.active(True)**

.. code-block:: python
  
  def do_connect():
    import network
    sta_if = network.WLAN(network.STA_IF)
    
    if not sta_if.isconnected():
        print('connecting to network...')
        sta_if.active(True)
        sta_if.config(txpower=8.5) 
        sta_if.connect('ssid', 'passwd')
        while not sta_if.isconnected():
            pass
    print('network config:', sta_if.ifconfig())

Quick reference
-------------------------
* `Quick reference for the ESP32 <https://docs.micropython.org/en/latest/esp32/quickref.html>`_
  


