---
{"dg-publish":true,"permalink":"/personal-projects/e-reader/"}
---

<p><iframe src="https://drive.google.com/file/d/1ugCoqEGnQrw_Ymg9dZLZ2uUBESus7AHl/preview"  allow="autoplay" frameborder ="0" allowfullscreen></iframe></p>

I set out to program a tiny e-reader using the ESP32-2432S028R, known colloquially as the Cheap Yellow Display (CYD). The board, sold for under $20 contained what I needed; a ESP32 WROOM chip, a 240x320 LCD display, resistive touch screen and SD card slot. 

>[!success] Features
>- Reads .txt files from SD card
>- Text appears on screen with a typewriter effect
>- Text speed control
>- Jumping to next or previous page
>- Autosaving and loading last loaded page
>- Only loads segments of large text files at a time

# Hardware
The ESP32-2432S028R has a community documenting hardware and software:
https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display
However, the model was a variation, bought from this link: [AliExpress](https://www.aliexpress.com/item/1005005616073472.html?aff_fcid=34b101dd3c2747c3bc61234d62e1ff51-1760704301507-00606-_DBNqsgr&tt=CPS_NORMAL&aff_fsk=_DBNqsgr&aff_platform=shareComponent-detail&sk=_DBNqsgr&aff_trace_key=34b101dd3c2747c3bc61234d62e1ff51-1760704301507-00606-_DBNqsgr&terminal_id=b03c841628eb4477b1d921f7088d188a&afSmartRedirect=y). This one had a USB C port and LiPo battery pins, and did not have a datasheet available. 

The main challenge was finding the GPIO pin outputs for the ESP32, since this was one of many variants of the CYD. In the end, I could not find the datasheet anywhere for this specific board, so I had to probe the pins myself using a multimeter. Luckily, most of the pins were the same as the common CYD model.

# Firmware
Firmware was coded in C++ and compiled using PlatformIO plugin in VS Code. Using PlatformIO, compatibility with other hardware can be added later through its config file. This is available at my [GitHub repository](https://github.com/EpicCyborg/CYD_Text_Display).

The typewriter text scrolling was inspired by RPG and visual novel video games, where letters in dialogue appear individually. Text speed can be increased by holding button A, and text can be skipped with button B. When a textbox is complete, button A is pushed to proceed to the next textbox, while button B is pushed to go back. On this device, halves of the touch screen were mapped as buttons with right side being button A and left side button B.

The text file on the SD card is read via an algorithm that splits it into segments with maximum word count below a set character limit per line. A segment is each line of text, while a page is a group of segments to be displayed, and both are indexed. Since the LCD library only supports ASCII text, UTF-8 characters such as curly " are converted to ASCII equivalents.

# Expansion
>[!info] Future Plans
>- Battery-powered (LiPo + BMS)
>- 3D-printed enclosure
>- Switching between multiple text files
>- More visually appealing UI
>- Move to hardware with larger LCD screen
