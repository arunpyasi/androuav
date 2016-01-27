# Introduction #

Android is not a real-time OS. That is the reason why it is relegated to data acquisition. If a call starts ringing (happens) or an e-mail is received or even the battery goes off, manual mode has to be activated (although this is Arduino's job). In other words: Android software is not critical.

We use HTC Magic and can't support any other device, for now.

# Communications #

Serial communication is not enabled by default in Android devices. This implies some serious hacking and is, by far, the hardest part of the project. You can even brick (i.e. kill) your phone so, please, try this at home but with caution and only if you know what you're doing.

## Kernel changes ##

In HTC devices, serial communication is disabled, [android-serial-api](http://code.google.com/p/android-serialport-api/wiki/Htc) is the main resource in which this hack is explained.

Once the device is correctly communicating (the best way is to cross-circuit TX and RX pins on the HTC connector and send something with the [example app at android-serialport-api](http://code.google.com/p/android-serialport-api/wiki/Htc). If the same data is received, AndroUAV application is ready to be used.

# Usage #

The first time that the application is run, click on Configuration and select ttyMSM2 and 9600 bps. If ttyMSM2 is not shown, your kernel is not ready.

When "start" is clicked, compass and GPS data is sent each time a change occurs.
