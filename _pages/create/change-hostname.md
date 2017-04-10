---
layout: single
permalink: create/documentation/change-hostname.html
sidebar:
  nav: "create"
---

# Changing the hostname of your instrument
Instead of using the default hostname "raspberrypi", you can name your synth anything you want. After that your prynth editor will be reached using a unique name (eg. https://mysynth.local:3000). This is also useful to avoid name clashing, if you have more than one prynth instrument.

1. To do so, you first need to [log into your Raspberry Pi using SSH](ssh-intro.html) and then use the raspi-config program, by typing.
~~~
sudo raspi-config.
~~~
![raspi-config1](../../images/documentation/raspi-config1.png)
2. Choose option 7 "Advanced Options" and then option A2 "Hostname"
![change_hostname1](../../images/documentation/change_hostname1.png)
![change_hostname2](../../images/documentation/change_hostname2.png)
3. After that you will be greeted with some rules about naming convention, after which you can introduce your new hostname.
![change_hostname3](../../images/documentation/change_hostname3.png)
![change_hostname4](../../images/documentation/change_hostname4.png)
4. After rebooting your Prynth you should be start using the new hostname.
