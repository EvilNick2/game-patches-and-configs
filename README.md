# Game Patches, Fixes and Configs
This personal repository is meant to store all configs and patches for games I really love and am still playing or would like to return to at some point.

These settings were tested on PC:
* **OS:** Windows 11 Pro (64-bit)
* **Motherboard:** [MSI MEG Z590 ACE](https://www.msi.com/Motherboard/MEG-Z590-ACE)
* **CPU:** [Intel Core i9-11900K 3.50 GHz (5.30 GHz Max)](https://ark.intel.com/content/www/us/en/ark/products/212325/intel-core-i9-11900k-processor-16m-cache-up-to-5-30-ghz.html)
* **CPU Cooler:** [NZXT Kraken Z73](https://nzxt.com/en-GB/product/kraken-z73)
* **GPU:** [Palit GeForce RTX 3090 GamingPro 24 GB](https://www.palit.com/palit/vgapro.php?id=3731&lang=en)
* **RAM:** [Corsair Vengeance 32 GB DDR4-3600 MHz (2x16 GB)](https://www.corsair.com/uk/en/p/memory/cmh32gx4m2d3600c18/vengeance-rgb-pro-sl-32gb-2x16gb-ddr4-dram-3600mhz-c18-memory-kit-a-black-cmh32gx4m2d3600c18)
* **Case:** [Corsair iCUE 5000X RGB](https://www.corsair.com/uk/en/p/pc-cases/cc-9011212-ww/icue-5000x-rgb-tempered-glass-mid-tower-atx-pc-smart-case-black-cc-9011212-ww)
* **PSU:** [Corsair RM850x 850W Gold+ Full Modular](https://www.corsair.com/uk/en/p/psu/cp-9020180-uk/rmx-series-rm850x-850-watt-80-plus-gold-certified-fully-modular-psu-uk-cp-9020180-uk)
* **Storage:**
	* **OS:** [WD_BLACK SN850 1 TB NVMe M.2 (SSD)](https://www.amazon.co.uk/WD_BLACK-Internal-Gaming-Technology-speeds/dp/B08KFS6THF)
	* **Games:** [WD_BLUE SN550 2 TB NVMe M.2 (SSD)](https://www.amazon.co.uk/WD_BLUE-SN550-2280-PCIe-speed/dp/B08K4NP5DQ)
	* **Games 2:** [Samsung 970 EVO Plus 2 TB NVMe M.2 (SSD)](https://www.amazon.co.uk/Samsung-MZ-V7S2T0BW-970-EVO-Plus/dp/B07MLJD32L)
	* **Files:** [Western Digital Blue 4 TB 5400 RPM (HDD)](https://www.amazon.co.uk/Western-Digital-BlueTM-Interne-WD40EZAZ/dp/B09889DL48)
	* **Recordings:** [Western Digital Red 2 TB 5400 RPM (HDD)](https://www.amazon.co.uk/Red-Plus-Internal-Hard-Drive/dp/B0C4X31Q9F)

| Table of Contents 										|
|-----------------------------------------------------------|
| [1. Folder names](#folder-names) 							|
| [3. Mods](#mods) 											|
| [5. Steam launch parameters](#steam-launch-parameters)	|

## Folder names
Each root folder represents the name of the engine, and inside each one is a folder with the name of the game made with said engine. Most of the files are configuration and keybinds, but sometimes they can include actual patches. The folder `_Unknown` contains settings from games which I do not know what engine was used.

There's also certain folders that contain complex names with brackets. Whatever files are inside of them, you must place them in the correct path inside of your computer.

**EXAMPLE:**
* idTech
	* DOOM (2016)
		* [%USERPROFILE%] [Saved Games] [id Software] [DOOM] [base]

The above example would correspond to Windows Explorer's path: `%USERPROFILE%/Saved Games/id Software/DOOM/base` for DOOM (2016)'s config files.

If the folder DOES NOT contain complex names with brackets, that means the files are stored/placed inside Steam's game directory.

**EXAMPLE:**
* Source
  * Counter-Strike Global Offensive
    * game
      * csgo
        * cfg

The above example would correspond to the following path in your computer: `<Your_Steam_Library_Folder>/steamapps/common/Counter-Strike Global Offensive/game/csgo/cfg`.

**One last thing:** some files could not be added to the repository due to file size, so I'll be linking them below.

## Mods, patches and source ports
Have a look at [this file](./MODS_AND_PATCHES.md) for a full list of mods and other patches.

## Steam launch parameters
To use these: right click the game > Properties > Launch Options

- **BioShock**
```
-nointro
```
<br/>

- **DOOM**
```
+set com_skipIntroVideo 1 +set r_skipFog 1 -USEALLAVAILABLECORES -heapsize 2097152 -sm4
```
<br/>

- **DOOM 3**
```
+set g_fov 120 +set g_gunX -2 +set g_gunZ -0.5 +set r_fullscreen 1
```
<br/>

- **Half-Life** (and general GoldSrc Engine games)
```
-novid -noforcemaccel -noforcemparms -noforcemspd -nojoy -width [MONITOR WIDTH] -height [MONITOR HEIGHT] -nomsaa -nofbo +gl_vsync 0 +fps_max [MONITOR REFRESH RATE] +fps_override 1 +rate 20000 +cl_cmdrate 106 +cl_updaterate 101
```
Replace `[MONITOR WIDTH]` and `[MONITOR HEIGHT]` with your monitor's resolution, and `[MONITOR REFRESH RATE]` with your monitor's native refresh rate.

If using Xash3D FWGS, add `-console` to enable the console.

If playing Opposing Force, make sure `fps_max` is equal or lower than 120. Anything higher will break rope physics.

<br/>

- **Half-Life 2** (and general Source Engine games)
```
-novid -nojoy -w [MONITOR WIDTH] -h [MONITOR HEIGHT] +fps_max [MONITOR REFRESH RATE] -high +mat_motion_blur_percent_of_screen_max 0 +mat_postprocess_enable 0
```
Replace `[MONITOR WIDTH]` and `[MONITOR HEIGHT]` with your monitor's resolution, and `[MONITOR REFRESH RATE]` with your monitor's native refresh rate.
<br/>

- **Half-Life: Alyx**
```
-novid -console -vconsole -nowindow +vr_fidelity_level_auto 0 +vr_fidelity_level 2 +vr_msaa 2 +vr_fxaa 0 +hlvr_continuous_normal_speed 110 +hlvr_continuous_combat_speed 135
```