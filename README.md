Kazam Screencaster v1.3.4


### Introduction
===============

Kazam is a simple screen recording program that will capture the content
of your screen and record a video file that can be played by any video
player that supports VP8/WebM video format.

Optionally you can record sound from any sound input device that is
supported and visible by PulseAudio.

Since Kazam has been stop development since 2014. Continue their work is welcome!

### Installation - development version
======================================

If you want bleeding edge, development version then you will have to get
source code from Launchpad by running the following command:

```git clone https://github.com/tuanphpvn/kazam.git```

If you are running ubuntu 16.04 run :

sudo apt-get install python-distutils-extra
sudo apt-get install python-xdg

Then you need to run setup.py to build and install Kazam:

```cd kazam```
```python setup.py install```

You will have to run setup as root user or use sudo. Default installation
path is /usr/local.

### Running Kazam
=================

If you want to run Kazam from the source tree, there are a few limitations
that you have to take into account. Right now Ubuntu App indicator will not
allow setting custom icons. Every icon has to be taken from currently
installed icon theme.

To run Kazam simply execute te following commands in the source tree:

$ cd bin
$ ./kazam

If you already have Kazam installed then Kazam icon will show in the
indicator, if not, the only way to get to the menu is to click on one
of the icons in the indicator and then move around with the cursor keys.

Keyboard shortcuts
------------------

If you have keybinder3.0 from the unstable PPA installed, then you can
use these keyboard shortcuts for controlling Kazam:

SUPER-CTRL-Q - Quit
SUPER-CTRL-W - Show/Hide main window
SUPER-CTRL-R - Start Recording
SUPER-CTRL-F - Finish Recording

Keyboard shortcuts will work if you installed Kazam 1.3.1 from a PPA,
keybinder 3.0 is now a dependency and will be installed automatically.


### Recording Tips
==================

Framerates above 20fps are unlikely to work well because of software and
hardware limitations. If you increase framerate and framerate in
resulting video drops, that is because encoder can't keep up.

Always do a sound check. Especially if you are recording a live commentary
with background sound. I got the best results when I used earphones to listen
to the audio while recording. This way your mic will not pick up any audio
coming from speakers.


### Debugging & reporting problems
===================================

If you encounter a bug or any kind of unexpected behavior please try to
reproduce it while you run Kazam from standard terminal with --debug option.