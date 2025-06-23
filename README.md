# ESP32CanGauge

ESP32 Can Bus battery gauge used in my EV conversion project.

![alt text](https://github.com/jamiejones85/ESP32CanGauge/blob/main/display.jpg?raw=true)
## Hardware

Not finished the custom board yet, but for now I'm using:
- Wemos S2 Mini dev board
- Can Bus Transciever module board
- Buck converter module
- 240x320 TFT screen from Ali Express https://www.aliexpress.com/item/1005005316683037.html

## Libraries

- TFT_eSPI at version 2.5.0
- SPI at version 2.0.0
- FS at version 2.0.0
- SPIFFS at version 2.0.0
- ACAN_ESP32 at version 1.1.2

## Connections
In order to define which connections to use, you must modify the `TFT_eSPI/User_Setup.h`,
for example, setting:
#define TFT_MOSI 15 // In some display driver board, it might be written as "SDA" and so on.
#define TFT_SCLK 14
#define TFT_CS   5  // Chip select control pin
#define TFT_DC   27  // Data Command control pin
#define TFT_RST  33  // Reset pin (could connect to Arduino RESET pin)

