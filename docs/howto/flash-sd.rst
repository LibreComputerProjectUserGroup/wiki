***********************
Flashing Micro-SD Cards
***********************

=====
Linux
=====

Materials
---------

* Host computer running Linux

  * Built-in SD/microSD card reader, or adapter

* MicroSD card, large enough to hold uncompressed image file (e.g. *.img)
* `Image file to install on microSD card <http://share.loverpi.com/board/libre-computer-project>`_

Procedure
---------

1. Download an operating system image
2. **OPTIONAL**: If available on the website you are downloading the image from, etc, verify the download with a supplied md5sum/sha256

  * ``md5sum <downloaded-file>`` **OR** ``sha256 <downloaded-file>``, etc.
  * Sometimes you will have to locate the checksums within an extracted archive, covered in the following step

3. Extract the image from compressed file

  * ``unzip file.zip`` **OR** ``tar zxfv file.gz`` **OR** ``unxz file.xz``

4. At this point you should have an image on your local disk (e.g. file.img)
5. Burn the image to your micro-SD card

  * ``sudo fdisk -l`` **OR** ``cat /proc/partitions`` -- look for your new device
  * ``dd if=/path/to/image.img of=/dev/sdX status=progress`` -- X = <a,b,...>; DON'T USE A PARTITION, e.g. sdb1
  * **OPTIONAL**: Grab a snack

6. At this point, given no errors (check for equal in/out blocks read/written), the micro-SD card should contain an image file
7. The card should not have been mounted, so it is safe to remove from the host computer. If it was mounted for some reason, eject the device in the host operating system before removing the card
