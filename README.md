# esp-idf-ping
ping example for esp-idf.   
This project pings your WiFi router.   
ICMP Echo document is [here](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/protocols/icmp_echo.html).   

# Installation
```
git clone https://github.com/nopnop2002/esp-idf-ping
cd esp-idf-ping
idf.py set-target {esp32/esp32s2/esp32s3/esp32c3}
idf.py menuconfig
idf.py flash monitor
```

# Configuration
![config-top](https://user-images.githubusercontent.com/6020549/142784392-17edc93c-f642-45a3-a6d7-82d013f34ff8.jpg)

Target is own gateway   
![config-app-1](https://user-images.githubusercontent.com/6020549/183223688-984ddd77-dd58-4a47-9925-2b78dcdaf8e5.jpg)

Target is www.espressif.com   
![config-app-2](https://user-images.githubusercontent.com/6020549/183223692-9a39550c-0270-42a3-8bbd-b2d6b882b40a.jpg)

# Screen Shot
![esp-idf-ping](https://user-images.githubusercontent.com/6020549/183223706-f3e5b641-0ad7-4da7-8b9f-ab959c2b41c8.jpg)

