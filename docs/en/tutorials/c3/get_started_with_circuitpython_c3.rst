Get started with MicroPython [C3 series]
=======================================================

Flash MicroPython firmware
----------------------------

The boards were originally flashed with MicroPython firmware.
To install CircuitPython flash the firmware with the following steps.

Requirements
---------------

* `Python <https://www.python.org/downloads/>`_
* `esptool <https://github.com/espressif/esptool>`_ (to flash ESP32-C3 firmware)

.. highlight:: bash

::

      pip3 install esptool

C3 CircuitPython Firmware
------------------

.. * `C3 Mini Firmware <https://circuitpython.org/board/lolin_c3_mini/>`_



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
    esptool.py --chip esp32c3 --port PORT_NAME --baud 460800 write_flash -z 0x0 firmware.bin

.. note::
  Don't forget to change **PORT_NAME** and **FIRMWARE.bin**.

  In Linux, **PORT_NAME** is like /dev/ttyUSB0.
  In Windows, **PORT_NAME** is like COM4.


WIFI
------------------
You need set WIFI Tx Power to 8.5dBm to use WIFI.

Use **sta_if.config(txpower=8.5)** after **sta_if.active(True)**

.. code-block:: python

  import wifi

  wifi.radio.tx_power = 8.5
  wifi.radio.connect("wifi_ssid", "wifi_password")

Quick reference
-------------------------
* `Quick reference for the ESP32 <https://docs.micropython.org/en/latest/esp32/quickref.html>`_
