# How-to-get-the-most-performance-out-of-your-PC-Guide
The ultimate gamer's guide to fixing PC lag, debloating Windows, and boosting FPS through deep system tuning.

### Disclaimer & Liability

By proceeding with this guide, you accept full responsibility for your hardware, data, and system stability. I have structured this guide to isolate risks so you know exactly what you are changing.

Risk Breakdown by Category:

- **Basic & Advanced Optimizations (Windows):** Completely safe. These steps utilize vetted software and standard OS settings. They will not cause data loss, hardware damage, or OS corruption.
- **Extreme Optimizations (Hardware & Deep OS):** Installing custom, stripped-down operating systems (ReviOS / AtlasOS), adjusting BIOS parameters, and tuning GPU clocks via MSI Afterburner carry inherent risks. While generally safe if instructions are followed precisely, incorrect values can lead to system instability, thermal throttling, crashes, or the need for a clean Windows reinstall.
- **Linux Optimizations:** Completely safe. The Linux section relies strictly on standard Steam launch options and basic terminal commands. No deep kernel-level modifications are required.

Safety Measures:
- Do your own research on your own components like idle/use temps, CPU PL1 & PL2, Overclocking limits based on the options when working on BIOS.
- Use HWMonitor to keep on voltage/wattage of components
- Use TaskManager or HWMonitor to keep track of your thermals

# Tested Hardware
The hardware mentioned here are my own that was owned at some point.

### PC CPUs & GPUs
- i5 4570 + GTX 1050 Ti 4gb (Z230 Workstation)
- i7 4770 + GTX 1650 4gb (Asus Q87M-E)
- Ryzen 5 5600X + GTX 1080 8gb (Biostar B450)
- i7 11700K + RTX 3060 Ti 8gb (Gigabyte Z590D)

### Laptops
- HP Probook 6570b | i7 3840QM (integrated)
- Dell Latitude | i7 (integrated)
- Lenovo Thinkpad E595 | Ryzen 7 3700U (integrated)
- Lenovo Thinkbook 15 G4 ABA | Ryzen 7 5825U (integrated)

# Guide
I have personally researched and tested all of the optimization techniques on multiple devices belonging to my friends and family members and optimized according to their needs. I optimized older hardware the most to get as much performance as I can for gaming or overall just smoother OS experience. You will not need to backup your data as all of these do not cause any modification to data present on your storage devices or even corrupt your OS. But it is still recommended you follow each step with care.

## Windows
We all are aware how slow Windows 11 is even on heavy hardware where it performs sluggish. I always recommend Windows 10 for better user experience and performance. But whether you are on Windows 10 or 11 these following steps should improve performance overall and leave a small performance gap between Windows 10 and 11.

### Basic
This is the easy stuff that anyone of any age should be able to do.

#### Delete third party anti-virus software
Third party anti-virus software are not needed. The base windows defender is more than enough. Majority of the anti-virus software eat up extensive amount of resource like CPU and RAM and slows down your device by 80% (I am completely guessing 80% because of how much difference I noticed after removing them). Using anti-virus software is equivalent to download free ram from the internet (All fake). You can use Revo Uninstaller or BC Uninstaller if you want to remove its every trace from the device but normal uninstall is also fine.

#### Update your drivers
While this may not do much for performance but it does improve the stability of different components on your device. Depending on what brand CPU you are running you may download the Driver software.
- [Intel Driver Support Assistant](https://www.intel.com/content/www/us/en/support/detect.html)
- [AMD Adrenalin Support Assistant](https://www.amd.com/en/products/software/adrenalin.html)

Latest GPU drivers do improve performance in the latest games but may not be the most stable one. This is not the case all the time but you may still keep up to date. It is not needed to update the driver to the latest one but after every other update is fine.
- [Nvidia App](https://www.nvidia.com/en-us/software/nvidia-app/)
- [AMD Adrenalin Support Assistant](https://www.amd.com/en/products/software/adrenalin.html)

#### Use Microsoft PC Manager
[PC Manager](https://apps.microsoft.com/detail/9pm860492szd?referrer=psi&hl=en-US&gl=PK) is Microsoft's own product. It is available on Microsoft Store. It makes it easy to remove cache and deep clean storage to free up ram and storage. It is just like using the Cleaning app found in our Android/Apple phones.

#### Use Wintoys
[Wintoys](https://apps.microsoft.com/detail/9p8ltpgcbzxd?hl=en-US&gl=PK) is a free app made for Windows. It is available on Microsoft Store. It brings a lot of options that may be deep in device manager or settings up front. The UI is easy to use and configurations are self explanatory. 

**Recommended Settings**
- Enable Ultimate Performance Power Plan: Ensures your CPU doesn't aggressively downclock during gameplay.
- Turn on Hardware-Accelerated GPU Scheduling (HAGS): Offloads high-frequency task scheduling from the CPU to the GPU. This is excellent for reducing CPU bottlenecks on older processors.
- Turn on Game Mode: Forces Windows to prioritize system resources for your game and suspends background Windows updates.
- Disable Virtualization-Based Security (VBS) & Core Isolation: Highly recommended for gaming. Windows 11 enables this by default, but it can cost you up to 10% in FPS and cause random stutters. Disabling it lowers enterprise-level security slightly but provides a massive free performance boost.
- Disable Background Apps: Stops Microsoft Store apps and built-in Windows apps from running invisibly and consuming precious RAM.
- Disable Telemetry & Activity History: Stops Windows from constantly running background tracking services and using your network bandwidth to send data to Microsoft, which helps prevent random ping spikes in multiplayer games.
- Turn off Fast Startup: Since we already configured "Fast Boot" in the BIOS, disabling Windows' software Fast Startup ensures your PC actually fully shuts down and clears the RAM cache completely, preventing weird OS bugs and stutters over time.
- Disable Visual Effects (Low-End Only): If you are on an older laptop or very weak CPU, turning off transparency effects and UI animations makes desktop navigation feel instantly faster.

### Advanced
This is where things get interesting. A lot of the changes from here will make very noticeable difference in performance and responsiveness but may require care in using them.

#### Use Winhance
[Winhance](https://winhance.net/) is another app free to use for Windows. It is easy to install and use just like Wintoys. You can remove any unwanted Microsoft app which windows may not allow to remove like Microsoft Edge or Copilot (I think you can remove copilot now normally) and use the "Optimize" section to improve the responsiveness of Windows. The optimization doesn't cause any major difference in performance but improves the overall feel of Windows.

Instructions:
- Download and Install it.
- Once opened, it may ask to create a Restore point which is up to you.
- In Apps, you can remove Microsoft Edge which does take up resources by default and any other app you may not use.
- In Optimization, you can go to "Quick Actions" and "Apply Recommended".
- Optional: In Visuals, you can strip down the UI to its fasted and simplest look. This does make UI elements faster and more responsive.

#### Other Drivers
These are other drivers that may improve stability and offer more consistent gameplay. This is optional as windows may have this up to date but should check on outdated hardware.
- Chipset drivers which on older OEM devices may have to do manually like Dell and HP Workstations. This does improve stability. Double check versions to see which is newer.
- Gaming RAM may have driver update as well. I did have an update on my DDR4 Corsair RAM but not on DDR3 ECC Rams or DDR4 Trident RAM, so this depends on brand.

#### Use ISLC
[ISLC](https://www.wagnardsoft.com/content/Download-Intelligent-standby-list-cleaner-ISLC-1041) (Intelligent Standby List Cleaner) is a free software that clears up RAM cache occupied in standby. Online tutorials can better explain the ideal values for checking when to clear that RAM cache than me. Too small or too big values may cause instability or crashes.

#### Use MSI Afterburner
[MSI Afterburner](https://www.msi.com/Landing/afterburner/graphics-cards) is the industry standard for GPU tuning. It allows you to push your hardware past factory limits for extra frames, or optimize it for cooler, quieter operation.

Basic Overclocking (More FPS):
- Power Limit: Slide the power limit to its maximum. This safely allows the GPU to draw more wattage when needed to maintain higher boost clocks during heavy gaming scenes.
- Core & Memory Clocks: Increase these slowly (e.g., +50MHz steps on the Core) to get raw extra frames. If your game crashes or you see visual artifacts, back the numbers down until it is completely stable.

Cooling & Stability Tweaks:
- Undervolting (The Sweet Spot): Instead of just pushing clock speeds, lowering the voltage your GPU uses to hit its target speed drastically reduces temperatures. A cooler GPU won't hit thermal throttling limits, meaning it will sustain a highly stable, flat frame rate instead of dropping frames when it gets hot.
- Custom Fan Curve: The default GPU fan curves prioritize being completely silent, which causes the card to run unnecessarily hot. Setting an aggressive fan curve (e.g., 70% fan speed at 70°C) will keep the card icy and prevent heat-induced stutters.
- RivaTuner Statistics Server (RTSS): This installs alongside Afterburner. It provides the On-Screen Display (OSD) so you can monitor your FPS, 1% lows, and hardware temperatures in real-time while in a game.

#### Use Modded Windows
This is not a separate installation of Windows rather it cleans up unnecessary bloat on system level files and services. You will need to disable Windows Defender to apply these changes but that is fine, no data will be harmed. It is completely safe to use (If the device restarts automatically and no prompt then you may need to redo the process again but it wont do that again next time). I have tested [ReviOS](https://www.revi.cc/) & [AtlasOS](https://atlasos.net/) personally. There are more options available depending on your needs but for gaming AtlasOS & ReviOS are mostly recommended.

If you are not sure about its safety, you can check out their web page or tutorials on Youtube. Instructions to install them can be found online providing a better guide or on official web page of modded OS's.

## Linux

#### Distributions
On Linux you dont need to download individual apps for managing drivers, the package manager handles that automatically by checking your hardware. This is really great of hardware with drivers that may be unlisted online. AMD Athlon CPUs (DDR3 Supported) which fell much behind Intel's CPU work much better on Linux (This is not personally tested but have researched about it). Linux is always recommended for unique pieces of hardware. If you plan to switch to Linux, I have some recommended distros that I have tested are listed below.

Recommended Distros:
- **CachyOS** is best for gaming performance.
- **Bazzite** almost there but provides the best setup for gaming.
- **EndeavourOS** is a good balance for work and gaming.
- **Ubuntu/Fedora** are a safe starting point.

#### Optimizations
On Steam you can use commands to change the behavior of how some games are launched.
- Use GE_Proton, you can download QT Proton and the install the latest version of Proton GE. "sudo pacman -S qt_proton" or "yay -S qt_proton", depending on what package manager you use. Then go to steam settings and compatibility and change default tool to latest version of GE Proton.
- "VKD3D_CONFIG=no_upload_hvv %command%" fixes some VRAM leaking problems of the GPU. It is recommended to use on games where VRAM may be highly utilized. This improves noticeable stability and frames.
- "gamemoderun %command%" gives a slight performance boost by reducing background activity. You will have to downloaded this package from the package manager. "sudo pacman -S gamemode" or "yay -S gamemode", depending on what package manager you use.

#### LACT GPU OverClocking
Since MSI Afterburner is not available on Linux, we use community-built alternatives that provide the exact same functionality.
- For AMD GPUs: Use LACT (Linux AMDGPU Controller). It provides a clean GUI to easily push your Radeon GPU's core clocks, VRAM clocks, and power states for basic overclocking. Once overclocked, you can apply a slight undervolt and set a custom fan curve to keep the card boosting higher for longer.
- For Nvidia GPUs: Use GreenWithEnvy (GWE). Since you have tested Nvidia cards like the GTX 1080 and GTX 1650 on Linux, GWE is the classic tool to adjust Nvidia power limits and apply core/memory clock offsets. (Note: You will need to enable the "Coolbits" registry value via the terminal in your Nvidia X Server settings to unlock overclocking). After overclocking, use GWE to set a custom fan profile to keep temperatures under control. (Note for advanced users: If you are running a modern Wayland desktop environment where GWE struggles, LACT has also recently added unofficial support for Nvidia overclocking).

## Bios
THIS REQUIRES CAREFUL EXECUTION AND KNOWLEDGE! Thinks can get risky here, improper values may brick the components entirely so do it at your own risk. Do set your CPU Power Limits (PL1 / PL2) regardless. 

#### CPU Power Limits (PL1 / PL2)
Motherboard manufacturers often set completely unrestrained power limits out of the box to win benchmark scores, which causes chips to run dangerously hot for very little actual gaming gain. PL1 (Long Duration Power Limit) and PL2 (Short Duration Power Limit) dictate how much wattage your CPU is allowed to pull. Manually setting these limits to Intel or AMD's official specifications—or slightly below them—drastically reduces temperatures and fan noise without dropping your gaming FPS.

#### Performance Mode
Some bios have "Performance Mode" so enabling it will give u a lot of performance but if something works oddly you may go back to normal. We will discuss how to make performance mode changes manually as well.

#### RAM Boot Speed (Fast Boot)
Enabling "Fast Boot" or "Memory Fast Boot" reduces the time it takes for your PC to power on by skipping specific hardware initialization checks during startup. Keep this disabled while you are testing new hardware or applying new overclocks, but enable it once your system is fully stable to significantly speed up your boot times.

#### Memory Training (Memory Context Restore)
When you turn on your PC, the motherboard tests the RAM to find the best signal integrity (Memory Training). This can make boot times painfully slow, especially on newer platforms. Once you know your XMP or EXPO profile is completely stable without any crashes, look for a setting called "Memory Context Restore" and enable it. This forces the system to remember the last successful training configuration, bypassing the training phase and booting much faster.

#### Manual Memory Timing Overclock
If you want to go beyond XMP/EXPO, you can manually "tighten" your RAM timings (such as CL, tRCD, tRP, tRAS). Tight timings drastically reduce system memory latency and heavily boost your 1% low FPS, making gameplay incredibly smooth. However, this is the most tedious, crash-prone optimization you can do. Only attempt this if you are using a detailed guide for your specific RAM die type and are completely comfortable shorting the CMOS pins or removing the motherboard battery when the PC refuses to boot.

#### Turbo Boost Technology 2.0/3.0
This is Intel's built-in boosting algorithm that allows your CPU to automatically clock higher than its base speed when thermal headroom and power limits allow. Always ensure this is Enabled. Disabling it will lock your CPU to its base frequency and severely cripple your performance in modern games.

#### Efficient Turbo Boost
Many modern motherboards have an "Energy Efficient Turbo" setting that tries to balance power consumption with boost clocks. Disabling this forces your CPU to favor maximum clock speeds and responsiveness rather than aggressively downclocking to save a few watts of electricity. For pure gaming performance, keep these power-saving limits disabled.

#### Hyperthreading
This is Intel's technology that splits physical CPU cores into two virtual threads (e.g., an i7 4770 having 4 Cores and 8 Threads). Generally, you should leave this Enabled. However, if you are running an older processor and only play older eSports titles (like CS2 or Valorant), disabling Hyperthreading can sometimes reduce CPU temperatures and slightly improve frame pacing by forcing the game to only use physical cores. Be aware that disabling it will heavily reduce your background multitasking performance.

#### Multithreading (SMT)
This is AMD's equivalent to Hyperthreading, known as Simultaneous Multithreading. The exact same rules apply: leave it Enabled for 99% of modern games, productivity tasks, and multitasking. Disabling it is only recommended if you are trying to squeeze out a few extra frames in very specific, older CPU-bound competitive games that do not know how to handle virtual threads properly.

#### Resizable BAR (ReBAR) / Smart Access Memory (SAM)
This is one of the easiest ways to get a completely free 5–15% performance boost in modern games. By default, your CPU can only access your GPU's VRAM in small 256MB chunks. Enabling Resizable BAR (known as Smart Access Memory on AMD platforms) allows the CPU to access the entire VRAM buffer at once, removing a massive data bottleneck.

To enable it, you must first disable CSM (Compatibility Support Module) to ensure your BIOS is in pure UEFI mode, and then enable Above 4G Decoding. Once those are set, the Resizable BAR option will appear or become toggleable.

Note: This feature is natively supported on newer hardware (like the i7-11700K and RTX 3060 Ti). Older platforms (like the 4th Gen Intels and GTX 10/16 series you tested) do not natively support this, though advanced users sometimes use community UEFI mods like ReBarUEFI to force it on older motherboards.

#### Update Bios
This is optional and risky! This does nothing in terms of performance but maybe do something for stability. It does unlock options and improve any known flaws or security issues. 
