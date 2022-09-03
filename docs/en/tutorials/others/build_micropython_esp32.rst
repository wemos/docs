Build MicroPython For ESP32
===================================


Install ESP-IDF
-----------------------------------

.. highlight:: bash

::

   git clone https://github.com/espressif/esp-idf.git
   cd esp-idf
   git checkout v4.4
   git submodule update --init --recursive

::
   
   cd esp-idf
   ./install.sh       
   source export.sh
   # You will need to source export.sh for every new session.   
   

Fetch the Code to Build
-------------------------

.. highlight:: bash

::

   git clone https://github.com/micropython/micropython.git
   cd micropython


Build mpy-cross
-----------------------------------

.. highlight:: bash

::
   
   make -C mpy-cross
   


Build your board
-----------------------------------

.. highlight:: bash

::
   
   cd ports/esp32
   make submodules
   make BOARD=LOLIN_S2_MINI  #Find board name in ./boards



Links
-----------------------------------

* `MicroPython port to the ESP32 <https://github.com/micropython/micropython/tree/master/ports/esp32>`_
  
