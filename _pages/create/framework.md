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

[![One sensor](../images/prynth_system_one_sensor.jpg){:width="50%" .align-right}](../images/prynth_system_one_sensor.jpg) The Prynth framework uses the Raspberry Pi (RPi) for sound synthesis and the Teensy microcontroller for sensor signal acquisition. The Teensy communicates with the RPi through an add-on board, which in turn connects to up to 10 multiplexer boards for a total 80 sensor connections (analog resistors or switches).

[![Framework](../images/framework_diagram.png){:width="65%" .align-left}](../images/framework_diagram.png) With the Prynth framework, the RPi boots into a system that automatically runs a web service with a full code editor for the SuperCollider programing language. When powered the synthesizer will also automatically run the last edited program.

The editor also contains other handy features, such as file managers, real-time system report and a SuperCollider debug window.


|  [![Editor](../images/editor.png){: width="500px"}](../images/editor.png) |


Currently the system is prepared to be connected to any Class-Compliant USB 2.0 Audio Card, which should work out-of-the-box. We are also researching the design of our own audio expansion board.

---

# Features

  - PCBs with mostly through-hole components (easy to manufacture and solder).
  - Ready-to-use Linux distribution with minimal configuration necessary.
  - Web-based code editor with debugger.
  - Patch and sample management.
  - System Status panel.

---

# BOM

For the typical application your bill of materials should be something like:

- Raspberry Pi (2 or 3) ([adafruit](https://www.adafruit.com/products/3055), [sparkfun](https://www.sparkfun.com/products/13825))
- Teensy (3.1 or 3.2) ([adafruit](https://www.adafruit.com/products/2756), [sparkfun](https://www.sparkfun.com/products/13736))
- Class-compliant USB 2.0 audio card ([adafruit](https://www.adafruit.com/products/1475))
- Prynth electronics boards ([downloads](/create/downloads.html))
- 8-channel analog multiplexers compatible with the 4051 pin scheme (up to 8 units, depending on the required number of analog input channels). Tested with the [Max4617CPE](http://datasheets.maximintegrated.com/en/ds/MAX4617-MAX4619.pdf). ([arduino](http://playground.arduino.cc/Learning/4051))
- Micro SD Card (at least 4 Gb, class 10 preferred) ([adafruit](https://www.adafruit.com/products/1294), [sparkfun](https://www.sparkfun.com/products/13833))
- 2 x 20 female GPIO header ([adafruit](https://www.adafruit.com/products/2222))
- Male and female headers 0.1''
- Female jumper wire ([adafruit](https://www.adafruit.com/products/266))
- Any analog sensor or switch (10K recommended for variable resistors)
- Micro-USB power supply with 2.4 A
