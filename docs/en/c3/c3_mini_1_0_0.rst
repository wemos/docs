C3 mini v1.0.0
================

==================  ==================  
 |TOP_IMG|_           |BOTTOM_IMG|_  
==================  ==================

.. |TOP_IMG| image:: ../_static/boards/c3_mini_v1.0.0_1_16x16.jpg
.. _TOP_IMG: ../_static/boards/c3_mini_v1.0.0_1_16x16.jpg

.. |BOTTOM_IMG| image:: ../_static/boards/c3_mini_v1.0.0_2_16x16.jpg
.. _BOTTOM_IMG: ../_static/boards/c3_mini_v1.0.0_2_16x16.jpg

A mini wifi & Bluetooth5 (LE) boards based ESP32-C3FH4. 
`[Buy it]`_

.. _[Buy it]: https://www.aliexpress.com/item/1005004005736554.html

Features
------------------
* based ESP32-C3 WIFI & Bluetooth LE RISC-V Single-Core CPU
* Type-C USB
* 4MB Flash
* 12x IO
* ADC, I2C, SPI, UART
* Compatible with LOLIN D1 mini shields 
* Compatible with MicroPython, Arduino, CircuitPython and ESP-IDF
* Default firmware: MicroPython

Tutorials
----------------------

* :doc:`../tutorials/c3/get_started_with_micropython_c3`
* :doc:`../tutorials/c3/get_started_with_arduino_c3`
* :doc:`../tutorials/c3/get_started_with_circuitpython_c3`

Documentation
----------------------

* `Schematic V1.0.0[PDF] <../_static/files/sch_c3_mini_v1.0.0.pdf>`_
* `Dimension V1.0.0[PDF] <../_static/files/dim_c3_mini_v1.0.0.pdf>`_
* `ESP32-C3 Datasheet <https://www.espressif.com/sites/default/files/documentation/esp32-c3_datasheet_en.pdf>`_

About WIFI
----------------------
You need set WIFI Tx Power to 8.5dBm to use WIFI.


Arduino
**************

Use **WiFi.setTxPower(WIFI_POWER_8_5dBm)** after 
**WiFi.begin()** or **WiFi.softAP()**

.. code-block:: arduino

  WiFi.begin(ssid, password);
  WiFi.setTxPower(WIFI_POWER_8_5dBm);

.. code-block:: arduino

  WiFi.softAP(ssid, password);
  WiFi.setTxPower(WIFI_POWER_8_5dBm);

**simple test:**

.. code-block:: arduino

  #include <WiFi.h>

  const char* ssid = "yourssid";
  const char* password = "yourpasswd";
  void setup() {
    Serial.begin(115200);
    delay(1000);

    Serial.println("Connecting...");
    WiFi.mode(WIFI_STA);
    WiFi.disconnect();
    
    WiFi.begin(ssid, password);

    WiFi.setTxPower(WIFI_POWER_8_5dBm);

    while (WiFi.status() != WL_CONNECTED){
      Serial.print(".");
      delay(500);
    }

    Serial.println("Connected");
    Serial.print("IP address: ");
    Serial.println(WiFi.localIP());
  }

  void loop() {
  } 

MicroPython
**********************

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


Technical specs
----------------------

+----------------------+------------+
| Operating Voltage    | 3.3V       |
+----------------------+------------+
| Digital I/O Pins     | 12         |
+----------------------+------------+
| Clock Speed          | 160MHz     |
+----------------------+------------+
| Flash                | 4M Bytes   |
+----------------------+------------+
| Size                 | 34.3*25.4mm|
+----------------------+------------+
| Weight               | 2.4g       |
+----------------------+------------+

Pin
----------------------

.. image:: ../_static/boards/c3_mini_v1.0.0_4_16x9.jpg
   :target: ../_static/boards/c3_mini_v1.0.0_4_16x9.jpg

Version
----------------
* `V2.1.0 <./c3_mini.html>`_  *lastest version*
* `V1.0.0 <./c3_mini_1_0_0.html>`_

