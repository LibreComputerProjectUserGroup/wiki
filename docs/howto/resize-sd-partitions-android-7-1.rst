************************************************
Resize android 7.1 image paritions on a micro SD
************************************************

=====
Linux
=====

Materials
---------

* Host computer running Linux

  * Built-in SD/micro-SD card reader, or adapter

* Micro-SD card pre loaded with aml-s905x-cc-android-7-1-preview-1-img

Procedure
---------

1. Open GParted GUI. You should see a parent partition containing 4 child partitions; this is what you need to resize first
2. Resize the parent partition as desired. Note that you need to add the same amount of space to this partition that you want to make available to Android
3. Keeping the first child partition in place, move all three of its' siblings to the end of the parent partition
4. Resize the first child partition (this should be labelled DATA) to the desired size
