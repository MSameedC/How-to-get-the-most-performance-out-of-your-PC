# Bios

> *It is strongly recommended that you follow a YouTube guide and research your specific motherboard and CPU before changing values. Otherwise, you can cause boot loops, overheating, or hardware instability.*

**Quick Steps:**

1. Set Storage Mode (AHCI) & Boot Mode (UEFI)
2. Set CPU Power Limits (PL1 / PL2)
3. Enable XMP / EXPO (Memory Profiles)
4. Enable RAM Fast Boot (Fast Boot)
5. Enable Memory Training (Memory Context Restore)
6. Overclock Memory Timing Manually (Extra)
7. Enable Performance Mode / Multi-Core Enhancement (MCE)
8. Enable Turbo Boost Technology 2.0/3.0
9. Disable Efficient Turbo Boost
10. Enable Hyperthreading
11. Enable Resizable BAR (ReBAR) / Smart Access Memory (SAM)
12. Update Bios (Extra)

## Settings

- **CPU Power Limits (PL1 / PL2)**

  Expected Impact: High for Cooling & Safety | Low for Performance

  > Look up your exact CPU's official TDP / PL1 & PL2 specs online before dialing these in.
  
  Motherboards often remove power limits out of the box to boost benchmark scores, causing extreme heat for minimal gaming gain. Manually setting PL1 (Long Duration) and PL2 (Short Duration) to your CPU's official spec—or slightly below—drastically lowers temps and fan noise without hurting FPS.

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

- **Performance Mode / Multi-Core Enhancement (MCE)**

  Expected Impact: Medium for Performance | Medium-High Risk for Cooling & Stability (Proceed with Caution)

  This one-click toggle forces all CPU cores to run at max boost simultaneously. It gives a decent FPS bump, but often overvolts the chip and causes thermal throttling. Test it while watching your temps—if it runs too hot or crashes, revert to Auto.

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
