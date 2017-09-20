---
layout: single
permalink: create/downloads.html
sidebar:
  nav: "create"
---

<style>
table, tr, td, th {border: 0px;font-size: 1em;}
</style>

# Prynth Electronics Boards

The Prynth electronics boards are distributed as [Eagle](https://cadsoft.io/) files.
After downloading the files use a service like [OshPark](https://oshpark.com/), [DirtyPCBs](http://dirtypcbs.com/) or any other manufacturer that accepts low quantity on-line ordering. Many of these accept Eagle board files directly, so we suggest you use them, avoiding the complexity of handling Gerbers files (which are still included mostly for reference). Also check the documentation section on instructions for [board assembly](documentation/board-assembly.html).

[Download  Muxi Control Eagle / Gerbers](https://github.com/prynth/prynth/blob/master/pcb/muxi_control/muxi_control.zip?raw=true){: .btn .btn--warning}

[Download  Muxi Eagle / Gerbers](https://github.com/prynth/prynth/blob/master/pcb/muxi/muxi.zip?raw=true){: .btn .btn--warning}

---

# Raspberry Pi image

We have also created a Linux distribution for the Raspberry Pi, based on the official Raspbian Jessie Lite, but that automatically runs the Prynth software out-of-the-box.

Download the image file and head to the documentation for [installation details](documentation/install-rpi-image.html).

[Download Prynth RPi image (2016-11-10)](https://mt.music.mcgill.ca/~idmilrepo/prynth/2016-11-10-prynth.img.zip){: download .btn .btn--warning}

[Download Prynth RPi image (2017-09-13 v. 0.4 Beta)](https://mt.music.mcgill.ca/~idmilrepo/prynth/2017-09-13-prynth.img.zip){: download .btn .btn--warning} <mark>NEW!</mark>


---

# Teensy source code

Download the Teensy source file program. In the documentation you'll find more instructions on installing the Teensyduino library and [uploading the firmware](documentation/teensy-firmware.html) to the Teensy.

[Download Teensy source code](https://github.com/prynth/prynth/blob/master/teensy/piteensymux.zip?raw=true){: .btn .btn--warning}
