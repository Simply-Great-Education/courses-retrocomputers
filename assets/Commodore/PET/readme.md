| PET User Port Pin |Signal Description | Target Connection Guide |
|----|----|---|
|Pin 2 |Video Data Signal |Connect to Video Input / Green Line|
|Pin 9 |Vertical Sync |Connect to V-Sync|
|Pin 10| Horizontal Sync (~15.6 kHz) |Connect to H-Sync |
|Pin 1 or A| Signal Ground (GND) |Connect to common ground|



| From PET 2001 Pin | Signal Name | To RGBtoHDMI 12-Way IDC | To 16-Way Extender IDC |
| :--- | :--- | :--- | :--- |
| **User Port Pin 2** | Video Data | Pin 9 (Green 3) | Pin 13 (Green 3) |
| **User Port Pin 10** | Horizontal Sync | Pin 8 (HSYNC) | Pin 12 (HSYNC) |
| **User Port Pin 9** | Vertical Sync | Pin 10 (VSYNC) | Pin 14 (VSYNC) |
| **User Port Pin 1 or A**| Signal Ground | Pin 3 (GND) | Pin 7 (GND) |


 Critical Settings ChecklistTTL Voltage Compatibility: The PET outputs raw 5V TTL logic levels. The RGBtoHDMI Pi Zero setup is natively a 3.3V logic device. Ensure your version of the RGBtoHDMI hat contains a TTL buffer board/chip (like the 6-bit or 12-bit TTL buffering editions) to prevent frying the Raspberry Pi GPIO pins.
 
 Profile Selection: Once powered on, open the RGBtoHDMI software menu. Load the Commodore PET configuration sub-profile. It will adjust the clock and pixel timings automatically so that your image stays centered without rolling.
