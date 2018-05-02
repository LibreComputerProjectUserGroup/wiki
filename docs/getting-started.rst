.. moduleauthor:: JC Staudt <jc@staudt.io>

.. header:: LCPUG

Getting Started
===============

This guide is designed to get you started using the hardware and software.
The scope of this document is to keep things as simple as possible; there are unlimited ways to configure your computing environment, so we are going for a straight-forward approach.
In this case, this guide describes a stand-alone computer configuration using a USB keyboard, USB mouse, and HDMI cable to a monitor or television.

1. Gather materials
-------------------

* Computer board

  * `Official Libre Computer store <https://libre.computer/purchase/>`__
  * `Board specifications and comparison <https://docs.google.com/spreadsheets/d/1GuB_AInWH0PTC0kyX1ulTQqlnBVnZSCKzQ-KqV7CX4s>`_
  * `Wikipedia: Comparison of single-board computers <https://en.wikipedia.org/wiki/Comparison_of_single-board_computers>`_

* MicroSD card (capacity > boot image file size)

  * :doc:`Compatible microSD cards <technical/sdcard>`

* Peripherals

  * Keyboard, mouse, HDMI cable

* Power supply

  * 10W USB power supply (5V, 2A) and a USB type-A to micro-USB cable **OR**
  * 10W Micro-USB power supply (5V, 2A)

2. Flash (i.e. burn, load) a microSD or eMMC card with your desired boot image file
--------------------------------------------------------------------------------

* :doc:`Flashing a microSD card <howto/flash-sd>`
* `Flashing an eMMC card <https://docs.google.com/presentation/d/1gP-8njKQg6WE3p9HOU55m39NyLyq6IBa0Ukww5N15IU>`_

3. Insert the microSD card into the board
-----------------------------------------

4. Connect peripherals
----------------------

* Connect an HDMI cable into both the computer board and a computer monitor or television, ensuring that you are on the correct video input on the monitor or television
* Connect USB keyboard and mouse to the computer board
* Connect your 5V power supply to a power source and the micro-USB cable lead into the micro-USB power input connector on the computer board

5. The computer board should be booting at this time
----------------------------------------------------

Look on the computer board for a solid red LED (indicating that power is being supplied to the board) a green LED (indicating activity on the computer board) and a "heartbeat" blue LED pattern (indicating that the Linux kernel has booted successfully).

Problems?
=========

* :doc:`Troubleshooting <technical/troubleshooting>`
* :doc:`Setup and serial communication with UART <howto/uart>`
* `Improve your quality of support by asking meaningful questions <https://stackoverflow.com/help/how-to-ask>`_
