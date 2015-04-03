# Camera Motion
Use your NVR software to trigger a SmartThings simulated presence sensor

I have lots of cameras that are controlled by dedicated NVR software.  This system is very good at detecting motion, but I had no way to get the motion detection back into SmartThings to trigger devices (turn on lights)

I wrote this very simple SmartApp to create an HTTP REST endpoint for my NVR software to trigger.  When motion is detected, the software hits the "active" URL, and when motion stops it hits the "inactive" URL.  

I used iSpyConnect for this implementation, but BlueIris and ZoneMinder both support the same action.  Lots of other high end NVRs also have this capability. 

![4-3-2015 8-58-41 am](https://cloud.githubusercontent.com/assets/478212/6983182/84981ac8-d9e0-11e4-92d0-a06abe581577.png)

Once you've installed the SmartApp, it will display the active and inactive URL.  Simply copy those into your NVR's action space and everything should be good to go!

Protip:  If you're using this to active some kind of lighting while the camera is running, make sure you have the camera motion detection setup so that when the lights go off you don't retrigger motion!

License
-------
Copyright (c) 2015, Kristopher Kubicki
All rights reserved.
