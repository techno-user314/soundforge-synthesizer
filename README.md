# SoundForge - A Digital Subtractive Synthesizer
<sup>v1.0.0</sup>  
SoundForge is a digital audio synthesizer designed to allow simple music creation without the need for a full DAW. It can run on a headless Raspberry Pi, and is controlled via MIDI input.

## Features
- SoundForge creates sound via subtractive synthesis.
- Every one of the 16 oscillators has it's own filter and waveform selection, along with it's own independant envelopes and modulators for amplitude, pitch shifting, and filter cutoff frequancy.
- There are four distinct, toggleable layers. Each layer has it's own customizable oscillators, effectively acting like four synthesizers that can play together, or seperately.
- Each layer has the ability to record and play back inputs. While you are playing live on layer 1, the other layers can each be looping a differant harmony that you have pre-recorded.
- Oscillators react to setting changes in realtime. Even while a recording is playing!

## Installation
Here are the steps to install and begin using SoundForge:
1. Ensure that both Python and a C compiler are installed on your system.
1. Clone this repo.
2. Compile the files in "src/c_synth" into a shared library called "libcsynth.so" (or "libcsynth.dll" for windows).
  - Using GCC, this command would be: `gcc -shared -o libcsynth.so -fPIC control.c synthesis.c`
3. Run main.py with a Python interperator running Python 3.7+

## Usage
Run mainx-x-x.py with a Python interperater to launch the synthesizer. SoundForge should automatically interface with any connected MIDI device.

## Coming Soon
- [ ] Better documentation!
- [ ] More of the synth implemented in C, as currently it takes a good machine to run smoothly.
