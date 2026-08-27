# MATLAB Installation on Arch Linux (Hyprland & Xorg)

Installing MATLAB on Arch Linux has been a frustrating journey. After years of segfaults and compatibility issues, **MATLAB R2026a** finally provides a stable solution—especially when combined with the latest community fixes.

## Why This Guide?

- **Laptop**: Arch Linux + Hyprland (Wayland) + NVIDIA MX230 (nouveau drivers)
- **Desktop**: Arch Linux + BSPWM (Xorg) + NVIDIA RTX 3050 (proprietary drivers)

### The Problems We Faced

| Version | Issue | Status |
|---------|-------|--------|
| R2020x, R2024x | Segfaults when launching MATLAB | ❌ Not resolved |
| R2026a (without fix) | Installer segfaults immediately on Intel CPUs | ❌ Still broken |
| R2026a + community fix | **Working perfectly** ✅ | ✅ Resolved |

## The Solution

The key is to follow the `LD_PRELOAD` step from [this GitHub repository](https://github.com/stefanoconiglio/omarchy-customizations/tree/master/matlabR2026a-archlinux-fix). Once applied, MATLAB launches without issues on both systems.

> 💡 **Note**: This fix works for both Wayland (Hyprland) and Xorg (BSPWM) environments.

## References & Credits

- [Arch Linux Wiki: MATLAB Installer Crash Issue](https://wiki.archlinux.org/title/MATLAB#Installer_or_MATLAB_crashes_immediately_with_segfault_on_Intel_CPUs_(R2026+))
- [stefanoconiglio/matlabR2026a-archlinux-fix](https://github.com/stefanoconiglio/omarchy-customizations/tree/master/matlabR2026a-archlinux-fix)
- [chriswifn/Install-Matlab-on-Arch-Linux](https://github.com/chriswifn/Install-Matlab-on-Arch-Linux)

## Screenshots

![MATLAB Installation on Arch Linux](https://github.com/user-attachments/assets/ae425afd-6243-4091-828a-d785ce01cfa2)

---

### Next Steps

If you’d like to:
- Add installation commands step-by-step
- Include troubleshooting tips for specific environments
- Highlight any additional fixes or workarounds

Just let me know! I can help refine this further.
