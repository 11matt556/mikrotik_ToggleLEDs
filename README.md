# mikrotik_ToggleLEDs

RouterOS scripts to enable or disable all LEDs.

The intended use is to disable all LEDs at night. Example:

```
add interval=1d name=disableLEDs_night on-event=disableLEDs policy=read,write start-date=2023-09-03 start-time=20:00:00
add interval=1d name=enableLEDs_morning on-event=enableLEDs policy=read,write start-date=2023-09-03 start-time=08:00:00
add name=enableLEDs_startup on-event=enableLEDs policy=read,write start-time=startup
```
