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
