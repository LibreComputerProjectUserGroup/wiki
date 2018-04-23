.. moduleauthor:: JC Staudt <jc@staudt.io>

.. header:: LCPUG

Serial Communication To Your Device Via UART
============================================

This is a brief how-to guide showing you how to communicate to your device via the UART interface.

Materials
---------

You will need:

* Host computer (e.g. laptop, desktop)
* USB/TTL adapter or cable
* Target device (e.g. Libre Computer board)
* USB power input for target device

Wiring
------

On a "Le Potato" board, locate the 3-pin male header block **located between the USB power input and the female HDMI connector**.
There is silk-screened tect below the header which reads **GND/TX/RX**.

+-----+
| GND |
+-----+
| TX  |
+-----+
| RX  |
+-----+

GND=Ground; TX=Transmit; RX=Receive

Make sure to leave any positive voltage lead unplugged for this process, as we are already supplying power via USB.
For this example, I have colored jumper cables as such: **RED/BROWN/BLACK/WHITE**

+-----------------+---------------+
| USB/TTL Adapter | Target Device |
+=================+===============+
| BROWN: GND      | BROWN: GND    |
+-----------------+---------------+
| BLACK: RX       | BLACK: TX     |
+-----------------+---------------+
| WHITE: TX       | WHITE: RX     |
+-----------------+---------------+

Before powering the target device, plug in the USB/TTL adapter to a spare USB slot on the host computer.
A 'USB' LED **may** illuminate, depending on what sort of adapter/cable you are using.

Begin listening to the target device
------------------------------------

On the host computer, open a terminal and enter the following command:

    sudo screen /dev/ttyUSB0 115200

...OR if you would like to write the output to a file in the **present working directory** ``pwd`` on the host computer at the point the command is run, enter:

    sudo screen -L /dev/ttyUSB0 115200

This ``-L`` flag creates a file called ``screenlog.<N>`` in your pwd.
N = the index of your screen session.

Moment of truth
---------------

Now power on the target device.
You should see some text display on the the host computer terminal.
This method of serial communication is quite useful if, say, the target device is not successfully booting.
