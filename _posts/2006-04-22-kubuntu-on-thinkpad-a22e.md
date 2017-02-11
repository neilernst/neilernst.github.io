---

date: 2006-04-22 14:47:30+00:00
title: Kubuntu on Thinkpad A22e
---

Some notes on installing/using Kubuntu on my A22e:



	
  * I use a standard MS Wheel mouse optical. When I installed Kubuntu on my thinkpad, the middle mouse button (the wheel click) wasn't working, although the wheel was. At first I suspected FIrefox (I use it extensively to open new tabs). However, I eventually narrowed it down to the X11 server configuration. The relevant file is /etc/X11/xorg.conf. Editing that, I found that the auto-config had included the lines commented out below:
`Section "InputDevice"
Identifier      "Configured Mouse"
Driver          "mouse"
Option          "CorePointer"
Option          "Device"                "/dev/input/mice"
Option          "Protocol"              "ImPS/2"
# Option                "Emulate3Buttons"       "true"
Option          "ZAxisMapping"          "4 5"
# Option                "EmulateWheel"
# Option                "EmulateWheelButton"  "2"
` Those emulate options aren't needed since I actually have the functions it was emulating. The middle click now works fine.

	
  * The final step is to go into Firefox and disable the option to load URLs from the middle click. In the address bar type 'about:config' and 'mouse' into the filter. Select the 'middlemouse.contentLoadURL' option and change it to False. This is a very confusing 'feature' of Firefox.

	
  * Speaking of Firefox, I just downloaded the source and installed it myself. The downside to this (i.e. not using apt-get) is that plugins etc must also be manually installed since Firefox has no 'connection' to the package manager.

	
  * There's a program on the package repos, imwheel, that can do legacy wheel support. However, I haven't used it since most new programs natively support wheel scrolling.

	
  * [This page](http://www.tuxme.com/node/544) is a pretty useful set of tips on Kubuntu and Thinkpads.


