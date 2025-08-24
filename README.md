# Rockbox EQ Presets (Converted from Reddit & AutoEq)

A collection of **Rockbox-compatible EQ presets** (`.cfg`) that I converted from
community posts (primarily Reddit) and **AutoEq** exports. Each preset’s **source
and author are attributed in the header of the `.cfg` file** (look for lines
beginning with `# Source:` and `# Author:`).

> ✅ Purpose: easy, reproducible equalization for Rockbox devices without
> manually re-entering parametric bands every time.

---

## How to use on Rockbox

1. Copy any `.cfg` file to your player at:  
   `/.rockbox/eqs/`
2. On the DAP:  
   `Settings → Sound Settings → Equalizer → Manage EQ Presets → Browse` → select the file.
3. Ensure `Equalizer = Enabled`.  
4. If you hear clipping, increase **precut** in the preset, or apply a global
   `Sound Settings → Advanced EQ settings → Precut`. (Most of these presets
   already include conservative precut.)

**Verify quickly**: open **Graphical EQ** after loading a preset and check that
the band gains roughly match the target shape (sub‑bass lift, 2 kHz dip, etc.).

---

## Folder layout

```
presets/
  brand_model_variant/
    rockbox_<name>.cfg        # Rockbox .cfg with band/Q/gain mapping
    notes.txt                 # (optional) rationale/compromises
```

- Rockbox supports **8 peak filters** plus **low/high shelf**. If a source had
  more bands, the preset notes describe the merges/approximations used.
- Gains in `.cfg` are **tenths of a dB** and Q is **Q×10**, e.g.  
  `eq peak filter 1: 1800, 17, -32` → 1.8 kHz, Q=1.7, –3.2 dB.

---

## Attribution & licenses

- **Reddit**: Each preset’s `.cfg` includes the subreddit thread link and
  username where available. If you are the original author and want your handle
  or link adjusted, open an issue/PR.
- **AutoEq**: Some presets were generated or validated with [AutoEq](https://autoeq.app).
  AutoEq is licensed under GPL‑3. See their repository for details.

---

## Notes

These presets were built and tested primarily on my **HiFi Walker H2 running
Rockbox**. They should transfer cleanly to any Rockbox‑enabled device, but FR
differences between DAC/amp stages may affect final perception. Always trust
your ears first.
