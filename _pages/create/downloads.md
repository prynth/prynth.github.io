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
After downloading the files use a service like [OshPark](https://oshpark.com/), [DirtyPCBs](http://dirtypcbs.com/) or any other manufacturer that accepts low quantity on-line ordering. Many of these accept Eagle board files directly, so we suggest you use them, avoiding the complexity of handling Gerbers files (which are still included for reference). Also check the [documentation](../doc/#assembling-the-pcbs) section on instructions for the board assembly.

[Download  Control Eagle / Gerbers](https://github.com/prynth/prynth/blob/master/pcb/control/control.zip?raw=true){: .btn .btn--warning}

[Download  Muxi Eagle / Gerbers](https://github.com/prynth/prynth/blob/master/pcb/muxi/muxi.zip?raw=true){: .btn .btn--warning}

---

# Raspberry Pi image

We have also created a Linux distribution for the Raspberry Pi, based on the official Raspbian Jessie Lite, but that automatically runs the Prynth software out-of-the-box.

Download the image file and head to the documentation for [installation details](../doc/#installing-the-raspberry-pi-image).

[Download Prynth v0.5 RPi image (2018-06-04)](http://idmil.org/pub/software/prynth/2018-06-04-prynth-v05.img.zip){: download .btn .btn--warning} <mark>NEW!</mark>

[Previous Prynth RPi v0.41 beta image (2018-03-22 v. 0.41 Beta)](http://idmil.org/pub/software/prynth/2018-03-22-prynth-v041.img.zip){: download .btn .btn--warning} (if using pcb versions prior to v0.5)


---

# Teensy source code

Download the Teensy source file program. In the documentation you'll find more instructions on installing the Teensyduino library and [uploading the firmware](../doc/#uploading-the-teensy-firmware) to the Teensy.

[Download Teensy v0.5 source code ](https://github.com/prynth/prynth/blob/master/teensy/teensy.zip?raw=true){: .btn .btn--warning}
