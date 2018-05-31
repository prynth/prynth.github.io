---
layout: single
permalink: create/framework.html
sidebar:
  nav: "create"
---

<style>
table, tr, td, th {border: 0px;font-size: 1em;}
</style>

# Framework

[![One sensor](../images/framework_intro/prynth_system_one_sensor.jpg){:width="50%" .align-right}](../images/prynth_system_one_sensor.jpg) The Prynth framework uses the Raspberry Pi (RPi) for sound synthesis and the Teensy microcontroller for sensor signal acquisition. The Teensy communicates with the RPi through an add-on board, which in turn connects to up to 10 multiplexer boards for a total 80 analog sensor connections (pots, resistors or switches). It also includes connections for digital sensors through I2C and SPI buses.

With the Prynth framework, the RPi boots into a system that automatically runs a web service with a full code editor for the SuperCollider programing language. When powered the synthesizer will also automatically run a specified program.

[![Framework](../images/framework_intro/editor_simple_sine.png){:width="100%" .align-left}](../images/framework_diagram.png)

Like the original SuperCollider for desktop and laptop computers, in Prynth it is possible to execute programs on-the-fly. Just-in-time compilation allows for dynamic editing, fine-tuning or complete repurpose of the synthesizers, without going through any compilation stage or processing interruption.

The Prynth editor also contains many more handy features, such as file managers, sensor configuration panels, real-time system report and a SuperCollider debug window.

[![Sensor Settings](../images/framework_intro/sensor_settings_action.png){:width="500px"}](../images/framework_intro/sensor_settings_action.png)

Prynth can use any audio device that works with the Raspberry Pi, including I2S cards and class-compliant USB 2.0 cards.

---

# Features

  - PCBs with mostly through-hole components (easy to manufacture and solder).
  - Ready-to-use Linux distribution with minimal configuration necessary.
  - Web-based code editor with debugger.
  - Just-in-time compiling.
  - Patch and sample management.
  - Sensor configuration panel.
  - System Status panel.

---

# BOM

For the typical application your bill of materials should be something like:

- Raspberry Pi (2 or 3) ([adafruit](https://www.adafruit.com/products/3055), [sparkfun](https://www.sparkfun.com/products/13825)).
- Teensy (3.1 or 3.2) ([adafruit](https://www.adafruit.com/products/2756), [sparkfun](https://www.sparkfun.com/products/13736)).
- I2S audio card or class-compliant USB 2.0 audio card ([adafruit](https://www.adafruit.com/?q=audio%20card%20raspberry%20pi), [Audio Injector](http://www.audioinjector.net/), [Fe-Pi](https://fe-pi.com/)).
- Prynth electronics boards ([downloads](/create/downloads.html)).
- 8-channel analog multiplexers compatible with the 4051 pin scheme (up to 8 units, depending on the required number of analog input channels). Tested with the [Max4617CPE](http://datasheets.maximintegrated.com/en/ds/MAX4617-MAX4619.pdf). ([arduino](http://playground.arduino.cc/Learning/4051)).
- Micro SD Card (at least 4 Gb, class 10 preferred) ([adafruit](https://www.adafruit.com/products/1294), [sparkfun](https://www.sparkfun.com/products/13833)).
- 2 x 20 female GPIO header ([adafruit](https://www.adafruit.com/products/2222)).
- Male and female headers 0.1''.
- Female jumper wire ([adafruit](https://www.adafruit.com/products/266)).
- Any analog sensor or switch (10K recommended for variable resistors).
- Micro-USB power supply with 2.4 A.
