# Windows
We all are aware of how slow & sluggish the Windows experience is. I always recommend Windows 10 for a far better user experience. Windows 10 or 11 these following steps will give you a significant uplift in performance in gaming latency and fps.

**Quick Steps:**
1. Delete third party anti-virus software
2. Update drivers
3. Use Microsoft PC Manager
4. Use Wintoys for basic optimization
5. Use Winhance for responsiveness
6. Use ISLC for Ram management
7. Use MSI Afterburner for GPU Overclocking
8. Install Modded Windows

## Basic

#### 1. Delete third party anti-virus software
Expected Impact: High for Performance & Latency (on Low-End hardware) | Safe

Third party anti-virus software are a scam. The base Windows Defender is enough and is managed actively by Microsoft. These eat up an extensive amount of resources like CPU and RAM, increasing boot time and slowing down your device significantly. Use Revo Uninstaller or BC Uninstaller if you want to remove its every trace from the device but normal uninstall is also fine.

#### 2. Update drivers
Expected Impact: Low for Performance | Medium for Stability | Safe

While this may not do much for performance but stability of different components on your device is improved. Depending on what brand CPU you are running you may download the Driver software.
- [Intel Driver Support Assistant](https://www.intel.com/content/www/us/en/support/detect.html)
- [AMD Adrenalin Support Assistant](https://www.amd.com/en/products/software/adrenalin.html)

Latest GPU drivers do provide performance uplift in the latest titles.
- [Nvidia App](https://www.nvidia.com/en-us/software/nvidia-app/)
- [AMD Adrenalin Support Assistant](https://www.amd.com/en/products/software/adrenalin.html)
  
#### 3. Use Microsoft PC Manager
Expected Impact: Low for Performance & Stability | Safe

[PC Manager](https://apps.microsoft.com/detail/9pm860492szd?referrer=psi&hl=en-US&gl=PK) is Microsoft's own product, available on Microsoft Store. It makes it easy to remove cache and deep clean storage to free up ram and storage, just like using the cleaning app found in our phones.

#### 4. Use Wintoys
Expected Impact: High for Performance & Latency (on Low-End hardware) | Low Risk for Safety (VBS/Core Isolation)
  
[Wintoys](https://apps.microsoft.com/detail/9p8ltpgcbzxd?hl=en-US&gl=PK) is a free app for Windows, available on Microsoft Store. It brings a lot of options that may be deeply hidden in control panel and settings, up front.
  
**Recommended Settings**
- Enable Ultimate Performance Power Plan: Ensures your CPU doesn't aggressively downclock during gameplay.
- Turn on Hardware-Accelerated GPU Scheduling (HAGS): Offloads high-frequency task scheduling from the CPU to the GPU. This is excellent for reducing CPU bottlenecks on older processors.
- Turn on Game Mode: Forces Windows to prioritize system resources for your game and suspends background Windows updates.
- Disable Virtualization-Based Security (VBS) & Core Isolation: Highly recommended for gaming. Windows 11 enables this by default, but it can cost you up to 10% in FPS and cause random stutters. Disabling it lowers enterprise-level security slightly but provides a massive free performance boost.
- Disable Background Apps: Stops Microsoft Store apps and built-in Windows apps from running invisibly and consuming precious RAM.
- Disable Telemetry & Activity History: Stops Windows from constantly running background tracking services and using your network bandwidth to send data to Microsoft, which helps prevent random ping spikes in multiplayer games.
- Turn off Fast Startup: Since we already configured "Fast Boot" in the BIOS, disabling Windows' software Fast Startup ensures your PC actually fully shuts down and clears the RAM cache completely, preventing weird OS bugs and stutters over time.
- Disable Visual Effects (Low-End Only): If you are on an older laptop or very weak CPU, turning off transparency effects and UI animations makes desktop navigation feel instantly faster.

## Advanced
This is where things get interesting. These changes will provide significant and **very noticeable** uplift in gaming performance and also provide a smoother and faster OS experience.

#### 1. Use Winhance
Expected Impact: Low for Performance | High for Latency & Responsiveness | Low Risk for Stability
  
[Winhance](https://winhance.net/) is a free app for Windows, easy to install and use. You can remove any unwanted Microsoft app which windows may not allow to remove like Microsoft Edge or Copilot etc and use the "Optimize" section to improve the responsiveness of Windows.
  
Instructions:
- Download and Install it.
- Once opened, it may ask to create a Restore point which is up to you.
- In Apps, you can remove Microsoft Edge which does take up resources by default and any other app you may not use.
- In Optimization, you can go to "Quick Actions" and "Apply Recommended".
- Optional: In Visuals, you can strip down the UI to its fasted and simplest look. This does make UI elements faster and more responsive.

#### 2. Use ISLC
Expected Impact: High for Latency & 1% Lows (Stuttering) | Safe

> *It is recommended you follow a youtube guide to use this app.*

[ISLC](https://www.wagnardsoft.com/content/Download-Intelligent-standby-list-cleaner-ISLC-1041) *(Intelligent Standby List Cleaner)* is a free software. This does not increase your fps, but on systems with 8GB or 16GB of RAM, it completely eliminates the micro-stutters caused by Windows failing to free up memory fast enough. 

#### 3. Use MSI Afterburner
Expected Impact: High for Performance & Cooling | Medium Risk for Stability & Cooling (Proceed with Caution)

> *Works on discrete GPUs only*
> *It is recommended you follow a youtube guide to use this app.*

[MSI Afterburner](https://www.msi.com/Landing/afterburner/graphics-cards) is the industry standard for GPU tuning. It allows you to push your hardware past factory limits for extra frames, or optimize it for cooler, quieter operation. 

Basic Overclocking (More FPS):
- Power Limit: Slide the power limit to its maximum. This safely allows the GPU to draw more wattage when needed to maintain higher boost clocks during heavy gaming scenes.
- Core & Memory Clocks: Increase these slowly (e.g., +50MHz steps on the Core) to get raw extra frames. If your game crashes or you see visual artifacts, back the numbers down until it is completely stable.

Cooling & Stability Tweaks:
- Undervolting (The Sweet Spot): Instead of just pushing clock speeds, lowering the voltage your GPU uses to hit its target speed drastically reduces temperatures. A cooler GPU won't hit thermal throttling limits, meaning it will sustain a highly stable, flat frame rate instead of dropping frames when it gets hot.
- Custom Fan Curve: The default GPU fan curves prioritize being completely silent, which causes the card to run unnecessarily hot. Setting an aggressive fan curve (e.g., 70% fan speed at 70°C) will keep the card icy and prevent heat-induced stutters.
- RivaTuner Statistics Server (RTSS): This installs alongside Afterburner. It provides the On-Screen Display (OSD) so you can monitor your FPS, 1% lows, and hardware temperatures in real-time while in a game.

#### 4. Use Modded Windows
Expected Impact: High for Performance & Cooling | Medium Risk for Stability & Cooling (Proceed with Caution)
 
> *It is recommended you follow a youtube guide to use this app.*

This is not a separate installation of Windows, it cleans up unnecessary bloat by removing unnecessary system level processes and services from running. You will need to disable Windows Defender to apply these changes, it is safe to use, no data will be harmed. *If the device restarts automatically and no prompt then you may need to redo the process again but it wont do that again next time*. I have personally used [ReviOS](https://www.revi.cc/) & [AtlasOS](https://atlasos.net/), more options available depending on your requirements.
