Get started with Arduino [C3 series]
==================================================

Requirements
---------------
  * `Python <https://www.python.org/downloads/>`_
  * `Arduino IDE <https://www.arduino.cc/>`_

Installing Hardware package
-----------------------------
  * `esp32 arduino package <https://github.com/espressif/arduino-esp32>`_ 


Configure Board
-------------------
  * Use lastest `esp32 arduino package`_ 
  * Choose board **LOLIN C3 MINI**


Upload Code
-----------------
* Make C3 boards into **Device Firmware Upgrade (DFU)** mode.

  * Hold on **Button 9**
  * Press **Button Reset**
  * Release **Button 9** When you hear the prompt tone on usb reconnection
 
WIFI
-----------------
You need set WIFI Tx Power to 8.5dBm to use WIFI.

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

Documentation
-------------------------
  * `ESP32-S2 and ESP32-C3 Support <https://github.com/espressif/arduino-esp32#esp32-s2-and-esp32-c3-support>`_


