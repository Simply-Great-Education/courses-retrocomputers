### Commodore 64

![AudioVideo_8pol_Pinbelegung](https://github.com/user-attachments/assets/f775ad5e-bdb5-4c80-9fb2-8575065c46ca) 8 Pin DIN
![AudioVideo_5pol_Pinbelegung](https://github.com/user-attachments/assets/9520cbe9-7299-4df7-bdbb-76d688c9c7ec) 5 pin DIN


| pin	| C64 signal|	notes |	ASSY 326298 (5-pin C64)	| VIC-20	| C128	| Plus/4 |
|---|---|---|---|---|---|---|
|1 |LUMINANCE	|luminance, video y-signal, brightness | COMPOSITE (luminance and chrominance) video signal	|6 volts DC, max 10 mA power supply for rf modulator	|like C64	|like C64|
|2 |GND	ground|	GND	|like C64 |	like C64|	like C64|
|3 |AUDIO OUT	|audio output|	AUDIO OUT	|like C64	|like C64|	AUDIO OUT (1VPP)|
|4 |VIDEO OUT	|composite video signal (mixed colour/brightness signal)	|VIDEO OUT	|"VLOW" video low	|like C64	|like C64|
|5 |AUDIO IN	|audio input |	AUDIO IN	|"VHIGH" video high	|like C64	|AUDIO IN|
|6 |CHROMINANCE	|chrominance, video c-signal, colour	|-	|-	|like C64	|like C64|
|7 |-	|not connected	|-	|-	|like C64	|like C64|
|8 |often +5VDC	|not connected	|-	|-	|5 volts DC|like C64|


Notes:
The eight pin jack is not the more common DIN 45326 (pins spanning 270°, circular), but DIN 41524 (pins spanning 262°, a "U" shape with a more open end, like a horseshoe). It's possible to forcibly plug in a wrong plug into the jack, but one should get the right plug in the first place on a new purchase. Should you happen to get the wrong plug and wasn't planning to use the +5V pin then you can remove the upper two pins out for a perfect fit.
On the VIC-20 the composite video signal is on pin four like on the C64 or C128. Additionally it is on pin five with a higher voltage level. Therefore a C64 a/v cable that uses only pins 2, 3, 4 (ground, audio, video) can be used unmodified on a VIC-20 or C128. Attention is advised when using a special a/v cable where incompatible signals could collide with each other.
Installation instructions for a second SID (stereo SID) often propose to use pin five (audio in) as the output of the right channel.[1]Though this is compatible with the pin assignment of stereo sets that used five pin DIN plugs in former times, it's not advisable. Due to the RCA plugs used nowadays, instead using the not connected pin 7 is an obvious choice.
Very smart DIYers can use the empty pin to provide additional 12V through it for the automatic AV mode selection in TV Sets when the computer is being turned on. Since the C64 and also the C128 have a 12V line available, one single wire is enough to connect it to PIN 7 at the DIN Jack of the computer. You will need an additional wire in the SCART cable to have this one available at the SCART Plug, PIN Number 16 and 8 (also 5 V is obviously sufficient to get the AV mode turned on elsewhere, both pins are also bridged by a resistor of 180 OHMs, directly connection to SCART PIN 8, and PIN No 16 through the resistor, so we also could first try to use the 5 V coming from Pin Number 8 at the DIN Jack. A matter of some testing.
Signal Description

VIDEO OUT: video output
This is a video signal in the format of the analog TV signal before RF modulation. In the C64 it is the standard format for PAL (most of the world) or NTSC (U.S.A./Japan). If a TV set has a composite video input it should be preferred over the RF signal, which loses quality by modulation in the C64 and demodulation in the TV set.
Because the signal contains the information of the video brightness and colour it is named composite video signal or CVBS (Colour Video Blanking Signal).
LUMINANCE: luminance, Y
This (TV-) signal contains all information necessary for monochrome video transmission. It consists of the brightness and synchronisation signals and therefore is called VBS (Video Baseband Signal)
CROMINANCE: chrominance, C
The chrominance (colour) is a part of the s-video signal (also Y/C signal). S-video is used in many monitors and should also be preferred if using a TV set providing a corresponding input (seperate or on the SCART jack).
AUDIO OUT: audio output
maximum 2 volts audio signal, transistor coupled from the SID
AUDIO IN: audio input
This audio input (maximum 3 volts) is connected to the audio input (pin 26) of the SID sound chip. This signal is routed through the SID filters and/or output stage, depending on the programming. It is then put out together with the internally generated voices through the volume regulation of the SID on the audio output.

<img width="400" height="227" alt="400px-scart" src="https://github.com/user-attachments/assets/02f75551-6828-4651-914d-eecf4e4f2a17" /> scart
<img width="222" height="131" alt="svhs-fem" src="https://github.com/user-attachments/assets/fe917e9e-f50f-4a82-a946-6e543dbd632e" /> S Video


| signal	| C64 A/V	|SCART jack	|s-video|
|---|---|---|---|
|ground	|2	|4, 17	|1,2|
|audio	|3|	2, 6	|-|
|video	|4|	20/-*	|-|
|luminance (Y)	|1	|-/20*	|3|
|chrominance (C)	|6|	-/15*	|4|
|* Only on Y/C-video over SCART. Not all devices with SCART connector support Y/C signals|
