# sidewinder_registry_mod
Windows 10 registry settings for MS Sidewinder 1.0 to make it work in windows 10

Finally made a 1998 Microsoft Sidewinder Precision Racing Wheel USB version 1.0 work in Windows 10.

What this regestry hack does (i think) is it tell the games it is a racing wheel with a Z axis (for braking)

Tested in WRC7 (i had to manually detect axis and assign them to make it work)
Also seems to work in Colin McRae Rally 2005

Install
--------
- Download the reg file to desktop
- Double click the file to import the settings into registry.

Background
----------

Found the info here:
http://vjoystick.sourceforge.net/site/index.php/forum/5-Discussion/1063-how-richard-burns-rally-detects-a-wheel#3226

Info used to find the new values:
https://sourceforge.net/p/timidity/git/ci/master/tree/windrv/mmddk.h#l230

When connceting the wheel a key is created:
HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\MediaProperties\PrivateProperties\Joystick\OEM\VID_045E&PID_001A
"OEMData"=hex:00,00,08,10,08,00,00,00

This file chage it to 41,00,28,10,08,00,00,00
and also duplicate the key to 
HKEY_CURRENT_USER\System\CurrentControlSet\Control\MediaProperties\PrivateProperties\Joystick\OEM\VID_045E&PID_001A]
