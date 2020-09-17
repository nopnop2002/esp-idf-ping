# WiFi station with ping
ping example for esp-idf

## Configure the project
```
git clone https://github.com/nopnop2002/esp-idf-ping
cd esp-idf-ping
make menuconfig
```

![config-1](https://user-images.githubusercontent.com/6020549/72844474-eaa0c600-3cdf-11ea-99aa-84f55a86f671.jpg)

![config-2](https://user-images.githubusercontent.com/6020549/93407157-6b927a80-f8cc-11ea-972a-1c65d62e5991.jpg)


## Build and Flash

Build the project and flash it to the board, then run monitor tool to view serial output:

```
make flash monitor
```

If you want to Serial Flasher Options:

```
make flash monitor ESPPORT=/dev/ttyUSB1
```


(To exit the serial monitor, type ``Ctrl-]``.)

See the Getting Started Guide for full steps to configure and use ESP-IDF to build projects.

## ping request
You can make a ping request using msdn hostname.

![esp-idf-ping](https://user-images.githubusercontent.com/6020549/93407279-ba401480-f8cc-11ea-8e1b-9f9238af9d5d.jpg)
