# How to get the most performance out of your PC Guide
The ultimate gamer's guide to fixing PC lag, debloating Windows, improving latency & boosting FPS through deep system tuning.

## WARNING! 
### Disclaimer & Liability
> By proceeding with this guide, you accept full responsibility for your hardware, data, and system stability. I have structured this guide to isolate risks so you know exactly what you are changing.
> 
> Risk Breakdown by Category:
> 
> - **Basic & Advanced Optimizations (Windows):** Completely safe. These steps utilize tested software and standard OS settings. They will not cause data loss, hardware damage, or OS corruption.
> - **Extreme Optimizations (Deep OS):** Installing custom, stripped-down operating systems (ReviOS / AtlasOS), and tuning GPU clocks via MSI Afterburner carry inherent risks. While generally safe if instructions are followed precisely, incorrect values can lead to system instability, thermal throttling, crashes, or the need for a clean Windows reinstall.
> - **Bios Setting:** It is strongly recommended that you follow a YouTube guide and research your specific motherboard and CPU before changing values. Otherwise, you can cause boot loops, overheating, or hardware instability.
> - **Linux Optimizations:** Completely safe. The Linux section relies strictly on standard Steam launch options and basic terminal commands. No deep kernel-level modifications are required.
>
> Safety Measures:
> - Do your own research on your own components like idle/use temps, CPU PL1 & PL2, Overclocking limits based on the options when working on BIOS.
> - Use HWMonitor to keep a check on voltage/wattage of components
> - Use TaskManager or HWMonitor to keep track of your thermals

## Tested Hardware
The hardware mentioned here are my own that were owned at some point.

**PC CPUs & GPUs**
- Z230 Workstation: i5 4570 + GTX 1050 Ti 4gb + 12gb ECC DDR3 RAM
- Asus Q87M-E: Xeon E3 1275 V3 (i7 4770) + GTX 1650 4gb + 16gb DDR3 RAM
- Biostar B450: Ryzen 5 5600X + GTX 1080 8gb + 16gb DDR4 RAM
- Gigabyte Z590D: i7 11700K + RTX 3060 Ti 8gb + 24gb DDR4 RAM

**Laptops**
- HP Probook 6570b | i7 3840QM (integrated)
- Dell Latitude 7389 | i7 7600U vPro (integrated)
- Lenovo Thinkpad E595 | Ryzen 7 3700U (integrated)
- Lenovo Thinkbook 15 G4 ABA | Ryzen 7 5825U (integrated)

## Table of Contents
1. [Windows Optimizations](./windows)
2. [Linux Optimizations](./linux)
3. [BIOS Tweaks & Overclocking](./bios)

# Introduction
I have personally researched and tested all of the optimization techniques on multiple devices belonging to me, my friends and family members have optimized their hardware according to their needs. Most noticeable performance gains are on older outed hardware. It is recommended you learn about these changes first and then perform those changes, regardless of their difficulty.

# Linux
On older hardware, Linux can extend its capabilities. With how far Linux has come, it can even run modern games in some cases faster and smoother than windows.

Used Distros:
- **CachyOS** is best for gaming performance.
- **Bazzite** almost there but provides the best setup for gaming.
- **EndeavourOS** is a good balance for work and gaming.
- **Ubuntu/Fedora** are a safe starting point.

## Optimizations

#### 1. Steam Commands
Expected Impact: High for Performance & Latency | Safe

On Steam you can use commands to change the behavior of how some games are launched.
- `VKD3D_CONFIG=no_upload_hvv %command%` prevents severe VRAM spilling, fixing massive stuttering and freezing in heavy DirectX 12 games.
- `gamemoderun %command%` Provides a minor 1-3% FPS uplift but ensures your CPU stays at maximum clock speeds, preventing random frame drops during explosions or heavy scenes. `sudo pacman -S gamemode` or `yay -S gamemode` *(depending on your package manager)*.

#### 2. Use Proton GE
Expected Impact: High for Performance & Stability (Hardware must support Vulkan 1.3+) | Safe

Proton converts DirectX games to Vulkun. Proton GE is a boosted version of normal Proton. You can download the ProtonUp-Qt tool to easily install the latest version of Proton GE. 

Instruction:
- Run `sudo pacman -S protonup-qt` or `yay -S protonup-qt` (depending on your package manager), or download it via Flatpak.
- Open the app, install the latest GE-Proton.
- Open Steam, go to `Settings > Compatibility` and change the default tool to your newly installed GE-Proton version.

#### 3. LACT
Expected Impact: High for Performance & Stability (Hardware must support Vulkan 1.3+) | Safe

> *Works on discrete GPUs only*
> *It is recommended you follow a youtube guide to use this app.*

An alternative to MSI Afterburner for Linux, we **LACT (Linux GPU Control Application)** that provides the exact same functionality. Originally built just for AMD, LACT now fully supports AMD, Nvidia, and Intel GPUs all inside one unified, easy-to-use GUI.

- **For All GPUs (AMD, Nvidia, Intel):** LACT allows you to easily push your GPU's core clocks, VRAM clocks, and power limits for basic overclocking. 
- **Cooling & Undervolting:** Once your clocks are set, you can use LACT to apply a slight undervolt and set a custom fan curve. This keeps the card icy and allows it to boost higher for longer periods without hitting thermal limits.
- **Why we use it:** Unlike older Nvidia-specific tools (like GreenWithEnvy), LACT does not rely on outdated X11 extensions. It works natively and flawlessly on modern Wayland desktop environments.

*(Note for Nvidia Users: To unlock overclocking limits, you may still need to enable the "Coolbits" registry value via the terminal in your Nvidia driver settings before LACT can apply clock offsets).*

# Bios

> *It is strongly recommended that you follow a YouTube guide and research your specific motherboard and CPU before changing values. Otherwise, you can cause boot loops, overheating, or hardware instability.*

- **CPU Power Limits (PL1 / PL2)**

  Expected Impact: High for Cooling & Safety | Low for Performance

  > Look up your exact CPU's official TDP / PL1 & PL2 specs online before dialing these in.
  
  Motherboards often remove power limits out of the box to boost benchmark scores, causing extreme heat for minimal gaming gain. Manually setting PL1 (Long Duration) and PL2 (Short Duration) to your CPU's official spec—or slightly below—drastically lowers temps and fan noise without hurting FPS.

- **Performance Mode / Multi-Core Enhancement (MCE)**

  Expected Impact: Medium for Performance | Medium-High Risk for Cooling & Stability (Proceed with Caution)

  This one-click toggle forces all CPU cores to run at max boost simultaneously. It gives a decent FPS bump, but often overvolts the chip and causes thermal throttling. Test it while watching your temps—if it runs too hot or crashes, revert to Auto.

- **XMP / EXPO (Memory Profiles)**

  Expected Impact: High for Performance & Latency | Low Risk for Stability

  By default, RAM runs at slow fallback speeds. Enabling XMP (Intel) or EXPO (AMD) unlocks your RAM's rated speed, giving a free 10–20% FPS boost and smoother 1% lows in CPU-heavy games like CS2 and Valorant. If your PC crashes, drop the RAM frequency down one notch (e.g., 3600MHz to 3200MHz).

- **RAM Boot Speed (Fast Boot)**

  Expected Impact: High for Boot Speed | None for Performance & Latency

  Skips certain hardware checks at startup to power on faster. Keep this Disabled while testing new tweaks so you can easily enter the BIOS if something breaks, then turn it On once everything is stable.

- **Memory Training (Memory Context Restore)**

  Expected Impact: High for Boot Speed | Medium Risk for Stability (Enable Only After Testing)
  
  Forces your motherboard to remember your last successful RAM boot instead of retraining the memory every startup. Only enable this after confirming your XMP/EXPO profile is 100% crash-free. If you get Blue Screens, turn it back off.

- **Manual Memory Timing Overclock**
  
  Expected Impact: High for Latency & 1% Lows | High Risk for Stability (Advanced / Risky)

  > **Warning!**
  > *Bad timings will stop your PC from booting. Only try this if you know how to reset your BIOS by clearing CMOS (shorting motherboard jumper pins or removing the CMOS battery).*
  
  Manually tightening secondary RAM timings (CL, tRCD, tRP, tRAS) slashes latency and boosts 1% lows beyond standard XMP/EXPO. It is tedious and crash-prone—follow a guide for your exact RAM die and stress-test with TestMem5 or OCCT.

- **Turbo Boost Technology 2.0/3.0**

  Expected Impact: High for Performance | Safe
  
  Allows your CPU to automatically boost past its base clock when thermals allow. Always keep this Enabled—turning it off locks your CPU to its slow base speed and tanks gaming performance.

- **Efficient Turbo Boost**

  Expected Impact: Low-Medium for Latency & Performance | Safe
  
  Attempts to save power by aggressively downclocking your CPU between workloads. Keep this Disabled so your CPU maintains higher clocks and snappier responsiveness during gameplay.

- **Hyperthreading**

  Expected Impact: Low-Medium for Performance & Cooling (Situational)
  
  Splits physical cores into virtual threads. Keep this Enabled for 99% of modern games and multitasking. Disabling it only helps on older CPUs playing older eSports titles (like CS2 or Valorant), slightly lowering temps and improving frame pacing at the cost of heavy multitasking performance.

- **Resizable BAR (ReBAR) / Smart Access Memory (SAM)**

  Expected Impact: Medium-High for Performance | Safe

  Lets your CPU access your GPU's entire VRAM buffer at once instead of tiny 256MB chunks, giving a free 5–15% FPS boost in modern games.

  To enable it:
    1. Disable CSM (forces pure UEFI mode).
    2. Enable Above 4G Decoding.
    3. Set Resizable BAR Support to Auto / Enabled.

  *Hardware Note: Natively supported on newer hardware (10th/11th Gen Intel + RTX 30-series or Ryzen 3000/5000 + RX 6000-series and newer). Older hardware requires community UEFI mods.*

- **Storage Mode (AHCI) & Boot Mode (UEFI)**

  Expected Impact: Medium for Stability & Responsiveness | Medium Risk (May Break Existing OS Boot)

  > **Warning!**
  > *Switching these on an existing Windows install can prevent Windows from booting unless you convert your drive from MBR to GPT first.*
  
  Switch Storage Mode from IDE/RAID to AHCI and Boot Mode from Legacy to UEFI for proper SSD TRIM support, faster drive communication, and ReBAR compatibility.

- **Update Bios**

  Expected Impact: Medium for Stability & Compatibility | High Risk for Safety (Proceed with Caution)

  > **Warning!**
  > Never shut down or unplug your PC during a BIOS update. Losing power mid-flash can permanently brick your motherboard unless it has a BIOS Flashback button.
  
  Rarely boosts FPS directly unless an update adds RAM compatibility, security fixes, or ReBAR support. If your PC is already stable and doesn't need a specific feature from the changelog, skip it.
