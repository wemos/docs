Build CircuitPython
===================================

Fetch the Code to Build
-------------------------

.. highlight:: bash

::

   git clone https://github.com/adafruit/circuitpython.git
   cd circuitpython
   make fetch-submodules

Install Required Packages
-----------------------------------

.. highlight:: bash

::

   # Install needed Python packages from pypi.org.
   pip3 install --upgrade -r requirements-dev.txt
   pip3 install --upgrade -r requirements-doc.txt

   sudo apt install ninja-build cmake python-is-python3

Install pre-commit
-----------------------------------

.. highlight:: bash

::
   
   cd circuitpython
   # You only need to do this once in each clone.
   pre-commit install

Build mpy-cross
-----------------------------------

.. highlight:: bash

::
   
   make -C mpy-cross
   

Set ESP-IDF
-----------------------------------

.. highlight:: bash

::

   # Download tools

   cd ports/espressif
   ./esp-idf/install.sh

.. highlight:: bash

::

   # Do this in each new terminal.
   # Set up the correct PATH and other environment variables.

   cd ports/espressif
   source esp-idf/export.sh

Build your board
-----------------------------------

.. highlight:: bash

::

   make BOARD=lolin_s2_mini

Use All Your CPUs When Building
-----------------------------------

.. highlight:: bash

::

   getconf _NPROCESSORS_ONLN
   12
   # This CPU has 6 cores and 12 threads.

.. highlight:: bash

::

   #Use 12 threads 

   make -j12 BOARD=lolin_s2_mini

Updating Your Repo
-----------------------------------

.. highlight:: bash

::

   git pull
   # only if necessary, from the top level directory
   make fetch-submodules
   # Then make again.

Links
-----------------------------------

* `Adafruit Build CircuitPython <https://learn.adafruit.com/building-circuitpython/build-circuitpython>`_
* `Espressif Builds <https://learn.adafruit.com/building-circuitpython/espressif-build>`_
