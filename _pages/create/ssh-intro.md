---
layout: single
permalink: create/documentation/ssh-intro.html
sidebar:
  nav: "create"
---

# Logging to the Raspberry Pi via SSH session
To connect to your Raspberry Pi using the command line you should use a secure shell session (SSH).


1. To do so open your Terminal program and write:
~~~
ssh pi@raspberrypi.local
~~~
![ssh1](../../images/documentation/ssh1.png)
2. On some systems you might be greeted with a message saying that your host (the raspberry) can't be authenticated and asking if you want to proceed. Ignore this and answer "yes".
![ssh2](../../images/documentation/ssh2.png)
3. Next you will be asked for your password. The default password is the same as in the original Raspbian distribution, which is "pi". After proceeding you should be logged to your pi, which can be confirmed by the prompt with "pi@raspberrypi".
![ssh3](../../images/documentation/ssh3.png)
