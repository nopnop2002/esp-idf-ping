# WiFi station with ping
ping example for esp-idf

## Configure the project

```
git clone https://github.com/nopnop2002/esp-idf-ping
cd esp-idf-ping
make menuconfig
```

* Set WiFi SSID and WiFi Password and Maximum retry under Example Configuration Options.

![config-1](https://user-images.githubusercontent.com/6020549/72844474-eaa0c600-3cdf-11ea-99aa-84f55a86f671.jpg)

![config-2](https://user-images.githubusercontent.com/6020549/72844479-ee344d00-3cdf-11ea-83c4-01ff97501370.jpg)


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

## Example Output
Note that the output, in particular the order of the output, may vary depending on the environment.

Console output if station connects to AP successfully:
```
I (589) wifi station: ESP_WIFI_MODE_STA
I (599) wifi: wifi driver task: 3ffc08b4, prio:23, stack:3584, core=0
I (599) system_api: Base MAC address is not set, read default base MAC address from BLK0 of EFUSE
I (599) system_api: Base MAC address is not set, read default base MAC address from BLK0 of EFUSE
I (629) wifi: wifi firmware version: 2d94f02
I (629) wifi: config NVS flash: enabled
I (629) wifi: config nano formating: disabled
I (629) wifi: Init dynamic tx buffer num: 32
I (629) wifi: Init data frame dynamic rx buffer num: 32
I (639) wifi: Init management frame dynamic rx buffer num: 32
I (639) wifi: Init management short buffer num: 32
I (649) wifi: Init static rx buffer size: 1600
I (649) wifi: Init static rx buffer num: 10
I (659) wifi: Init dynamic rx buffer num: 32
I (759) phy: phy_version: 4180, cb3948e, Sep 12 2019, 16:39:13, 0, 0
I (769) wifi: mode : sta (30:ae:a4:d9:bc:c4)
I (769) wifi station: wifi_init_sta finished.
I (889) wifi: new:<6,0>, old:<1,0>, ap:<255,255>, sta:<6,0>, prof:1
I (889) wifi: state: init -> auth (b0)
I (899) wifi: state: auth -> assoc (0)
I (909) wifi: state: assoc -> run (10)
I (939) wifi: connected with #!/bin/test, aid = 1, channel 6, BW20, bssid = ac:9e:17:7e:31:40
I (939) wifi: security type: 3, phy: bgn, rssi: -68
I (949) wifi: pm start, type: 1

I (1029) wifi: AP's beacon interval = 102400 us, DTIM period = 3
I (2089) esp_netif_handlers: sta ip: 192.168.77.89, mask: 255.255.255.0, gw: 192.168.77.1
I (2089) wifi station: got ip:192.168.77.89
I (2089) wifi station: connected to ap SSID:myssid password:mypassword
I (2091) wifi station: wifi_init_sta finished.
I (2101) wifi station: Connection success
I (2111) PING: IP Address: 192.168.10.102
I (2111) PING: Subnet mask: 255.255.255.0
I (2111) PING: Gateway: 192.168.10.1
I (2121) PING: gateway_addr.type=0
I (2121) PING: gateway_addr=192.168.10.1
I (2131) PING: ping start
I (2131) wifi station: initialize_ping success
I (2581) PING: 64 bytes from 192.168.10.1 icmp_seq=1 ttl=64 time=449 ms
I (12151) PING: 64 bytes from 192.168.10.1 icmp_seq=2 ttl=64 time=18 ms
I (22141) PING: 64 bytes from 192.168.10.1 icmp_seq=3 ttl=64 time=8 ms
I (32131) PING: 64 bytes from 192.168.10.1 icmp_seq=4 ttl=64 time=4 ms
I (42211) PING: 64 bytes from 192.168.10.1 icmp_seq=5 ttl=64 time=80 ms
I (52131) PING: 64 bytes from 192.168.10.1 icmp_seq=6 ttl=64 time=2 ms
I (62131) PING: 64 bytes from 192.168.10.1 icmp_seq=7 ttl=64 time=1 ms
I (72131) PING: 64 bytes from 192.168.10.1 icmp_seq=8 ttl=64 time=4 ms
I (82131) PING: 64 bytes from 192.168.10.1 icmp_seq=9 ttl=64 time=2 ms
I (92131) PING: 64 bytes from 192.168.10.1 icmp_seq=10 ttl=64 time=1 ms
```

Console output if the station failed to connect to AP:
```
I (589) wifi station: ESP_WIFI_MODE_STA
I (599) wifi: wifi driver task: 3ffc08b4, prio:23, stack:3584, core=0
I (599) system_api: Base MAC address is not set, read default base MAC address from BLK0 of EFUSE
I (599) system_api: Base MAC address is not set, read default base MAC address from BLK0 of EFUSE
I (629) wifi: wifi firmware version: 2d94f02
I (629) wifi: config NVS flash: enabled
I (629) wifi: config nano formating: disabled
I (629) wifi: Init dynamic tx buffer num: 32
I (629) wifi: Init data frame dynamic rx buffer num: 32
I (639) wifi: Init management frame dynamic rx buffer num: 32
I (639) wifi: Init management short buffer num: 32
I (649) wifi: Init static rx buffer size: 1600
I (649) wifi: Init static rx buffer num: 10
I (659) wifi: Init dynamic rx buffer num: 32
I (759) phy: phy_version: 4180, cb3948e, Sep 12 2019, 16:39:13, 0, 0
I (759) wifi: mode : sta (30:ae:a4:d9:bc:c4)
I (769) wifi station: wifi_init_sta finished.
I (889) wifi: new:<6,0>, old:<1,0>, ap:<255,255>, sta:<6,0>, prof:1
I (889) wifi: state: init -> auth (b0)
I (1889) wifi: state: auth -> init (200)
I (1889) wifi: new:<6,0>, old:<6,0>, ap:<255,255>, sta:<6,0>, prof:1
I (1889) wifi station: retry to connect to the AP
I (1899) wifi station: connect to the AP fail
I (3949) wifi station: retry to connect to the AP
I (3949) wifi station: connect to the AP fail
I (4069) wifi: new:<6,0>, old:<6,0>, ap:<255,255>, sta:<6,0>, prof:1
I (4069) wifi: state: init -> auth (b0)
I (5069) wifi: state: auth -> init (200)
I (5069) wifi: new:<6,0>, old:<6,0>, ap:<255,255>, sta:<6,0>, prof:1
I (5069) wifi station: retry to connect to the AP
I (5069) wifi station: connect to the AP fail
I (7129) wifi station: retry to connect to the AP
I (7129) wifi station: connect to the AP fail
I (7249) wifi: new:<6,0>, old:<6,0>, ap:<255,255>, sta:<6,0>, prof:1
I (7249) wifi: state: init -> auth (b0)
I (8249) wifi: state: auth -> init (200)
I (8249) wifi: new:<6,0>, old:<6,0>, ap:<255,255>, sta:<6,0>, prof:1
I (8249) wifi station: retry to connect to the AP
I (8249) wifi station: connect to the AP fail
I (10299) wifi station: connect to the AP fail
I (10299) wifi station: Failed to connect to SSID:myssid, password:mypassword
```
