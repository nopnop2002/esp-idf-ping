# esp-idf-ping
ping example for esp-idf

# Installation
```
git clone https://github.com/nopnop2002/esp-idf-ping
cd esp-idf-ping
idf.py set-target esp32
idf.py menuconfig
idf.py flash monitor
```

![config-1](https://user-images.githubusercontent.com/6020549/72844474-eaa0c600-3cdf-11ea-99aa-84f55a86f671.jpg)

![config-2](https://user-images.githubusercontent.com/6020549/93407157-6b927a80-f8cc-11ea-972a-1c65d62e5991.jpg)

# ping request
You can make a ping request using mDNS hostname.
- esp-idf V4.3 or earlier   
 You will need to manually change the mDNS strict mode according to [this](https://github.com/espressif/esp-idf/issues/6190) instruction.   
- esp-idf V4.4 or later  
 If you set CONFIG_MDNS_STRICT_MODE = y in sdkconfig.default, the firmware will be built with MDNS_STRICT_MODE = 1.

![esp-idf-ping](https://user-images.githubusercontent.com/6020549/93407279-ba401480-f8cc-11ea-8e1b-9f9238af9d5d.jpg)
