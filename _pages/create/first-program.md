---
layout: single
permalink: create/documentation/first-program.html
sidebar:
  nav: "create"
---


# Writing your first SuperCollider program
In this section we'll present an "Hello World" code example, that explains how to access sensor values inside SuperCollider on a Prynth.

## About SuperCollider

Prynth relies on SuperCollider as a programming language that allows for the full specification of synthesis, controller mapping and other interactions. We choose SuperCollider due to it's maturity, flexibility and high adoption within the community. For more information about SuperCollider, please visit the [SuperCollider Git page](http://supercollider.github.io/).

SuperCollider presents a somewhat steep learning curve but there are several good resources to getting started such as [tutorials](http://supercollider.github.io/tutorials/), [books](http://supercolliderbook.net/) and a newbie friendly [community](http://new-supercollider-mailing-lists-forums-use-these.2681727.n2.nabble.com/SuperCollider-Users-New-Use-this-f2676391.html).

---

## The Oscillator example

The following examples implements a single sinusoidal oscillator, in which the frequency is mapped to the first sensor connected to the [Muxi boards](http://localhost:4000/create/documentation/board-assembly.html).

~~~
fork{
 SynthDef(\test, {
  var sig;
  sig = SinOsc.ar(In.kr(100).range(100, 500), mul: 0.1);
  Out.ar([0,1], sig);
 }).add;

 s.sync;

 Synth(\test);
}
~~~

The most important concept in this example is that it shows an important convention in the Prynth system. We have stipulated that the 80 sensors that are available in Prynth are to be numbered using a convention, where a sensor addresses are composed by concatenating the multiplexer number with the sensor number (both starting at 0) and offsetting that number by 100.

Address = (multiplexer number ++ sensor number) + 100

Thus the address 134 would be the fifth sensor connected to the fourth multiplexer.
134 = (3 ++ 4) + 100

Let's breakdown the following code snippet:

~~~

SynthDef(\test, {
 var sig;
 sig = SinOsc.ar(In.kr(100).range(100, 500), mul: 0.1);
 Out.ar([0,1], sig);
}).add;

~~~

The SynthDef is an object that allows for the definition of the blueprint for a new synthesizer named "test". It contains a variable "sig" that will hold a signal resulting from the object SinOsc, which creates sinusoidal signals.When creating a SinOsc we should specify that it is to work at the audio rate, thus the ".ar" method.

The SinOsc object accepts several parameters, which can be set by order or by name. The first parameter is frequency and the last is the multiplier. Notice that the frequency is given by parameter order (it's the first parameter), while the multiplier is addressed using the "mul" key.

Our frequency is defined by sensor 100 (first sensor on the first multiplexer). This signal is inputed using the In object, which will work at a control rate, thus the ".kr" method. We then scale the sensor value from it's normalized value (0-1) to the desired frequency range for our oscillator (100-500 Hz). The multiplier is used to scale the signal amplitude to 1/10 of the maximum amplitude in order to avoid clipping (and sore ears).

We then create another object named "Out", functioning at an audio rate, and that takes two parameters, the first being the audio channels to which our variable signal should output. The channels are enclosed within square brackets to represent that they are a group of channels that will receive the same signal. Channels [0,1] are by convention the first stereo pair in the output device (audio card).

Finally the Synthdef is sent to the SuperCollider server by invoking the method ".add".

Now let's look again at the rest of the code:

~~~
fork{
 SynthDef(\test, {
  var sig;
  sig = SinOsc.ar(In.kr(100).range(100, 500), mul: 0.1);
  Out.ar([0,1], sig);
 }).add;

 s.sync;

 Synth(\test);
}
~~~

Forgetting the fork and sync functions temporarily, we can see that after the SynthDef has been specified and added to the SuperCollider server, we initialize a synth object by calling it by name. This will play a synth with the previously defined blueprint.

To this we only add one more thing, which is to enclose the code in a fork function, creating a routine (sequential steps). This is important because the synth cannot be instantiated without making sure that SuperCollider has received the corresponding synth definition (the previous code block). To assure this sequential procedure we use the server object (abbreviated "s") and invoke the ".sync" method, which sends a signal to the routine allowing it to continue once the server flagged that it received the synth definition.

These are concepts that are integral to the SuperCollider architecture, so for more in-depth understanding of the necessity of doing this, please refer to the reading materials at the top of this page. Seasoned SuperCollider experts will have no difficulty understanding this procedure.

---

## Accessing samples

There is also a convention for using the sound samples managed via web editor. Notice on the editor page that each sample as an assigned number. The samples are exposed through a reserved variable named ~sounds, that holds an array of Pathname objects pointing to the files.

As an example let's create a buffer that holds the 3rd file in the list:

~~~

~myBuffer = Buffer.read(s, ~sounds[2].fullPath)

~~~

Let's list all of the uploaded files:


~~~

~sounds.do{ |item, i|
	"File number ".post;
	i.post;
	" is named ".post;
	item.fileName.postln;
};

~~~

The returned result by the editor console should be:

~~~

File number 0 is named sample1.wav
File number 1 is named sample2.wav
File number 2 is named sample3.wav

~~~
