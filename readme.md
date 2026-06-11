# Z-Log2 Stop-Based False Color Tool

A stop-based false color monitoring LUT for Z CAM Z-Log2 footage, inspired by the EL Zone exposure system.

This LUT converts Z-Log2 into scene-referred exposure zones centered around 18% middle grey, allowing exposure decisions to be made in stops rather than relying solely on IRE values.

It is designed as an exposure monitoring tool only and is not intended for final image grading.

![Z-Log2 Stop-Based False Color Guide](zlog2_stop_false_color_guide.png)

---

## Why This Exists

After using the EL Zone system across multiple camera systems, I found it fundamentally changed how I approached exposure.

Traditional false color systems are usually built around IRE values. While useful, they become harder to interpret when monitoring log footage because log curves are logarithmically encoded. Different log curves place the same scene exposure at different IRE values, making it difficult to develop a consistent exposure workflow across cameras.

A stop-based system approaches the problem differently.

Instead of monitoring display brightness, exposure is evaluated relative to 18% middle grey in stops. This creates a common exposure language that remains consistent regardless of the camera, monitoring transform, or display LUT being used.

After working with EL Zone across multiple camera systems, I found that:

- Monitoring exposure in stops is easier and more intuitive than monitoring exposure in IRE.
- Exposure decisions become more consistent across different cameras and log curves.
- Highlight and shadow placement are easier to visualize relative to middle grey.
- Exposure can be communicated in a common language regardless of camera brand.

I wanted the same workflow for Z CAM Z-Log2.

Using Thatcher Freeman's reverse-engineered Z-Log2 transform as a foundation, this project converts Z-Log2 into scene-linear values before assigning stop-based exposure zones.

The result is a stop-based monitoring LUT designed specifically for Z-Log2 shooters.

---

## Features

- Stop-based exposure monitoring
- 18% middle grey centered around approximately 40 IRE
- Practical grey zone around 37-43 IRE
- EL Zone-inspired color mapping
- Designed specifically for Z CAM Z-Log2
- Minimal sensitivity to white balance changes
- Works as a monitoring LUT on cameras and external monitors that support LUT loading

---

## Included

- `Z-Log2_to_El-Zone-like_jobsanbiju-v1.1.cube`
- `zlog2_stop_false_color_guide.png`

---

## Exposure Guide

| Zone | Meaning |
|--------|----------|
| +6 | Highlight clipping |
| +5 | Extreme highlights |
| +4 | Very bright highlights |
| +3 | Bright highlights |
| +2 | Light skin / bright surfaces |
| +1 | Bright exposure |
| +1/2 | Slightly above middle grey |
| 0 | 18% Middle Grey |
| -1/2 | Slightly below middle grey |
| -1 | Dark exposure |
| -2 | Deep shadows |
| -3 | Very dark shadows |
| -4 | Near black |
| -5 | Extreme shadow detail |
| -6 | Black / crushed shadows |

---

## Notes

- Designed for exposure monitoring only.
- Not intended as a creative or technical viewing LUT.
- Best used alongside waveform monitoring.
- Exposure zones are referenced to 18% middle grey rather than display brightness.

---

## Credits

Z-Log2 decoding is based on publicly available work by Thatcher Freeman.

Designed and developed by jobsanbiju.

---

## Support the Project

If this LUT has been useful to you and you'd like to support future development, testing, and documentation:

Ko-fi: https://ko-fi.com/jobsanbiju

Support is completely optional, but every contribution helps fund future tools, LUTs, DCTLs, and resources for the Z CAM community.
