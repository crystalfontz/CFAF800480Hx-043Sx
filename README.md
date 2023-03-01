# CFAF800480Hx-043Sx
 This is Arduino sample code for the CFAF800480Hx-043Sx family of displays. These displays are 4.3" TFTs which use the [Sitronix ST7262](https://www.crystalfontz.com/controllers/Sitronix/ST7262/) LCD controller. This LCD controller supports a 24 bit parallel RGB interface. This demonstration code has been written for usage with the BT817 Embedded Video Engine.

 ## Display information
Here are links to our active displays:\
[CFAF800480Hx-043SN](https://www.crystalfontz.com/product/cfaf800480h0043sn-800x480-4-point-3-inch-tft-display)\
[CFAF800480Hx-043SC](https://www.crystalfontz.com/product/cfaf800480h0043sc-800x480-4-point-3-inch-capacitive-touchscreen-tft-display)\
[CFAF800480Hx-043SR](https://www.crystalfontz.com/product/cfaf800480h0043sr-800x480-4-point-3-inch-resistive-touch-tft-display)

For more information about other TFT offerings, please see our full list [here](https://www.crystalfontz.com/c/tft-lcd-displays/25)

## Display pin function
| Pin      | Symbol | Function               |
|----------|--------|------------------------|
| 1        | VLED-  | Backlight cathode      |
| 2        | VLED+  | Backlight anode        |
| 3        | GND    | Ground                 |
| 4        | Vlogic | Logic power supply     |
| 5-12     | R0-7   | Red data bus lines     |
| 13-20    | G0-7   | Green data bus lines   |
| 21-28    | B0-7   | Blue data bus lines    |
| 29       | GND    | Ground                 |
| 30       | DCLK   | Dot clock signal       |
| 31       | DISP   | Display on/off control |
| 32       | HSYNC  | Horizontal sync        |
| 33       | VSYNC  | Vertical sync          |
| 34       | DEN    | Data enable            |
| 35       | NC     | No connection          |
| 36       | GND    | Ground                 |
| 37-40    | NC     | No connection          |

## Navigating the Code
To toggle on or off different demonstrations, some defines in "BT817_defines.h" can be changed.

```c++
#define BMP_DEMO             (0)  
#define BMP_SCROLL           (0)  
#define SOUND_DEMO           (0)  
#define SOUND_VOICE          (0)  
#define SOUND_PLAY_TIMES     (10)
#define LOGO_DEMO            (1)  
#define LOGO_PNG_0_ARGB2_1   (1)  
#define BOUNCE_DEMO          (1)  
#define MARBLE_DEMO          (0)  
#define TOUCH_DEMO           (0)
```

`BMP_DEMO` - Toggled to 1 will display "splash.a8z" (after it has been written to flash using `PROGRAM_FLASH_FROM_USD (1)`) \
`BMP_SCROLL` - Toggled to 1 will display "clouds.a8z" (after it has been written to flash using `PROGRAM_FLASH_FROM_USD (1)`) scrolling across the screen \
`LOGO_DEMO` - Toggled to 1 will display the Crystalfontz Logo from "Round_Logos.cpp"\
`BOUNCE_DEMO` - Toggled to 1 will show a ball bouncing around the screen\
`MARBLE_DEMO` - Toggled to 1 will demonstrate the earth rotating and bouncing around on the screen in place of the ball (after bluemarb.a8z has been written to flash using `PROGRAM_FLASH_FROM_USD (1)`\
`TOUCH_DEMO` - Toggled to 1 will enable the touch screen (only compatible on touch versions of the display)