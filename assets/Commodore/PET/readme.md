| PET User Port Pin |Signal Description | Target Connection Guide |
|----|----|---|
|Pin 2 |Video Data Signal |Connect to Video Input / Green Line|
|Pin 9 |Vertical Sync |Connect to V-Sync|
|Pin 10| Horizontal Sync (~15.6 kHz) |Connect to H-Sync |
|Pin 1 or A| Signal Ground (GND) |Connect to common ground|



| From PET 2001 Pin | Signal Name | To RGBtoHDMI 12-Way IDC | Flying Lead Colour |
| :--- | :--- | :--- | :--- |
| **User Port Pin 2** | Video Data | Pin 9 (Green 3) | Green |
| **User Port Pin 10** | Horizontal Sync | Pin 8 (HSYNC) | Yellow |
| **User Port Pin 9** | Vertical Sync | Pin 10 (VSYNC) | Blue |
| **User Port Pin 1 or A**| Signal Ground | Pin 3 (GND) | Black |

* Pin 1: Video (Traced back to Pin 6 of the E9 IC)
* Pin 2: Ground (0V)
* Pin 3: Vertical Drive (Traced back to Pin 11 of the D8 IC)
* Pin 4: Ground (0V)
* Pin 5: Horizontal Drive (Traced back to Pin 2 of the C5 IC) [1]



 Critical Settings ChecklistTTL Voltage Compatibility: The PET outputs raw 5V TTL logic levels. The RGBtoHDMI Pi Zero setup is natively a 3.3V logic device. Ensure your version of the RGBtoHDMI hat contains a TTL buffer board/chip (like the 6-bit or 12-bit TTL buffering editions) to prevent frying the Raspberry Pi GPIO pins.
 
 Profile Selection: Once powered on, open the RGBtoHDMI software menu. Load the Commodore PET configuration sub-profile. It will adjust the clock and pixel timings automatically so that your image stays centered without rolling.


### RGBtoHDMI 12-Way Header Wiring Matrix

| Pin | Signal Function | Target Connection (PET 2001) |
| :--- | :--- | :--- |
| **1** | +5V Power Input | *Leave Disconnected* (Draw 5V from Datasette port) |
| **2** | +5V Power Input | *Leave Disconnected* |
| **3** | Ground (GND) | User Port Pin 1 or A (GND) |
| **4** | Ground (GND) | *Optional Ground Tap* |
| **5** | Red Data Bit | *Unused* |
| **6** | Blue Data Bit | *Unused* |
| **7** | Green Data Bit 1 | *Unused* |
| **8** | Horizontal Sync (HSYNC) | User Port Pin 10 (H-Sync) |
| **9** | Green Data Bit 3 (Mono) | User Port Pin 2 (Video Data) |
| **10**| Vertical Sync (VSYNC) | User Port Pin 9 (V-Sync) |
| **11**| Green Data Bit 2 | *Unused* |
| **12**| Ground (GND) | *Unused* |

      ┌───[ KEYWAY NOTCH ]───┐
      │  (2)  (4)  (6)  (8) (10) (12) │
      │  [·]  [·]  [·]  [·]  [·]  [·] │
(▲)   │  [·]  [·]  [·]  [·]  [·]  [·] │
      │  (1)  (3)  (5)  (7)  (9) (11) │
      └───────────────────────┘
