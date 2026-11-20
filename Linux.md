# Linux
On older hardware, Linux can extend its capabilities. With how far Linux has come, it can even run modern games in some cases faster and smoother than windows.

Used Distros:
- **CachyOS** is best for gaming performance.
- **Bazzite** almost there but provides the best setup for gaming.
- **EndeavourOS** is a good balance for work and gaming.
- **Ubuntu/Fedora** are a safe starting point.

**Quick Steps**
1. Apply Steam Commands
2. Use Proton GE
3. Use LACT for GPU Overclocking

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
