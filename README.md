# libnds-rs

Library for the Nintendo DS, written in Rust

## DS Technical Data (extracted from GBATEK):

### Processors
* ARM946E-S	32bit RISC CPU - 66MHz (used for video)
* ARM7TDMI	32bit RISC CPU - 33MHz (used for sound and GBA mode in 16MHz)

### Internal memory
* 4096KB	Main RAM
* 96KB		WRAM (64K mapped to ARM7, 32K mapped to ARM7 or ARM9)
* 60KB		TCM(16K for data, 64k for code) / Cache  (4K data, 8K code)
* 656KB		VRAM (allocatable as BG/OBJ/2D/3D/Pallete/Texture/WRAM memory)
* 4KB		OAM/PAL (2K OBJ Attribute Memory, 2K Standard Pallete RAM)
* 248KB		Internal 3D Memory (104K RAM for polygons, 144K RAM for vertices)
* ?KB		Matrix Stack, 48 scanline cache
* 8KB		Wi-Fi RAM
* 256KB		Firmware Flash (512KB in [iQue](https://en.wikipedia.org/wiki/IQue_Player) variant, with chinese charset)
* 36KB		BIOS ROM (4K for ARM9, 16K for ARM7, 16k for GBA mode)

### Video
* 2x LCD screens (256x192 pixel resolution, 3inch size, 18 bit color depth, backlight)
* 2x 2D video engines (extended GBA video controller)
* 3D video engine (assignable to upper or lower screen)
* Video capture (for effects, or forwarding 3D to 2D engine)

### Sound
* 16 sound channels (16x PCM8/PCM16/IMA-ADPCM, 6x PSG-Wave, 2x PSG-Noise)
* 2 sound capture units (echo effects, misc)
* Output: Stereo speakers, headphones socket
* Input: Built-in microphone, microphone socket

### Controls
* Gamepad with 4 direction keys and 8 buttons
* Touchscreen on lower LCD screen

### Communication
* Wi-Fi IEEE802.11b

### Specials
* Built-in RTC (Real-Time Clock)
* Power Management (Hardware)
* Hardware divide and sqrt functions
* CP15 System Control Coprocessor (cache, TCM, PU, BIST, etc)

### External memory
* NDS Slot (encrypted 8bit data bus and serial 1bit bus)
* GBA Slot (including NDS expansions)

### Manufactured cartridges
* ROM: 16MB, 32MB, 64MB
* EEPROM/FLASH/FRAM: 0.5KB, 8KB, 256KB, 512KB 

### Power supply
* Built-in rechargeable Li-ion battery, 3.7V 1000mAh (For the NDSL)
* External Supply: 5.2V DC
