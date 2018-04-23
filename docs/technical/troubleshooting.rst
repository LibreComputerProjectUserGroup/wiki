***************
Troubleshooting
***************

------
Issues
------

1. **Where is my video?**

  * Have you written (via ``dd`` or otherwise) the ``*.img`` file to a micro-SD card (as opposed to a USB)?
  * It is a known problem that no video appears when outputting video through the HDMI connector. Try toggling your monitor/TV inputs and see if the video signal appears.
  * Is the blue LED blinking? If not, please diagnose the issue via UART interface (see the :doc:`How-To page <../howto/uart>`) for more detailed information.
  * If the operating system image was not flashed correctly, there will be no video output since these devices do not have a BIOS or POST step during boot.
