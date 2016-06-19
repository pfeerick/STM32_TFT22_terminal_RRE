
# Minimalistic STM32 and ILI9341 based terminal

Videos demonstrating the original STM32F103 code in action!
* https://www.youtube.com/watch?v=OgaLXoLhz4g
* https://www.youtube.com/watch?v=DAAbDGCeQ1o

My modification has been related to Maple Mini compatibility. 

# For STM32F103C8T6 development board

## Connections
  Port | SPI1
  ---  | ---
  PA4  | CS1 
  PA5  | SCK1
  PA6  | MISO1
  PA7  | MOSI1
  PA11 | RST
  PA12 | DC
  
## TFT2.2 ILI9341 from top left:

 TFT  | STM32
 ---  | ---
 MISO | PA6
 LED  | +3.3V
 SCK  | PA5
 MOSI | PA7
 DC   | PA12
 RST  | PA11 or +3V3
 CS   | PA4
 GND  | GND
 VCC  | +3.3V
  
## Programming STM32 via serial
* Tools/Board set to Generic STM32F103C
* Tools/Upload set to Serial
* Top jumper set to 1, press reset button before uploading

## Serial adapter to STM32
  STM | USB-to-serial adapter
  --- | ---
  PA9 /TX | PC RX
  PA10/RX | PC TX
  3V3 (don't use 5V!) | 3V3 
  GND | GND
  
# For Maple Mini style boards

## Connections
  SPI1 | Maple Mini Pin
  ---  | ---
    CS1   | 7 / PA4
    SCK1  | 6 / PA5
    MISO1 | 5 / PA6
    MOSI1 | 4 / PA7

## TFT2.2 ILI9341 from top left:
TFT   | Maple Mini Pin
---   | ---
MISO  | 5  / PA6
LED   | +3.3V
SCK   | 6  / PA5
MOSI  | 4  / PA7
DC    | 21 / PA14
RST   | 22 / PA13
CS    | 7  / PA4
GND   | GND
VCC   | +3.3V

## For programming via bootloader:
* Tools/Board set to Maple Mini
* Tools/Bootloader version set to Bootloader 2.0 (any will do)
* Press the reset button when bootloader message appears if Maple Mini doesn't automatically reboot.

# Fonter
Improved font conversion tool by CNLohr can be taked from my fork of his pylotron game
