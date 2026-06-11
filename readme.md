# Z-Log2 Stop-Based False Color v1.1

A stop-based false color monitoring LUT for Z CAM Z-Log2 footage, inspired by the EL Zone exposure system.

This project was created to provide a more intuitive and exposure-focused monitoring solution for Z-Log2 than traditional IRE-based false color tools. Instead of mapping colors directly to display values, exposure zones are derived from decoded Z-Log2 scene-linear data and referenced to 18% middle grey.

![Z-Log2 Stop-Based False Color Guide](zlog2_stop_false_color_guide.png)

## Why This Exists

Most false color implementations are based on fixed IRE thresholds. While useful, I wanted a monitoring tool that behaves more like a stop-based exposure system, where each color represents a defined exposure range relative to middle grey.

Using Thatcher Freeman's reverse-engineered Z-Log2 transform as a foundation, this LUT converts Z-Log2 into scene-linear values before assigning exposure zones. The result is a monitoring tool that reflects exposure relationships rather than display brightness.

## Features

* Designed specifically for Z CAM Z-Log2 footage
* Stop-based exposure visualization
* 18% middle grey centered around approximately 40 IRE
* Practical middle grey zone of roughly 37-43 IRE
* White-balance resistant implementation
* EL Zone-inspired color palette
* Compatible with monitors that support custom LUT loading
* Useful for exposure evaluation without relying solely on waveforms

## Included Files

### Z-Log2_to_El-Zone-like_jobsanbiju-v1.1.cube

The monitoring LUT.

Load this LUT into your monitor and use it as an exposure reference while shooting Z-Log2 footage.

### zlog2_stop_false_color_guide.png

Reference chart showing all exposure zones and their corresponding colors.

## Exposure Reference

| Zone    | Relative Exposure             |
| ------- | ----------------------------- |
| +6      | Extreme highlights / clipping |
| +5      | Very bright highlights        |
| +4      | Bright highlights             |
| +3      | Strong highlights             |
| +2      | Bright skin / bright surfaces |
| +1      | Slightly over middle grey     |
| +1/2    | Slightly above middle grey    |
| 18% / 0 | Middle grey                   |
| -1/2    | Slightly below middle grey    |
| -1      | Darker midtones               |
| -2      | Deep midtones                 |
| -3      | Shadows                       |
| -4      | Deep shadows                  |
| -5      | Near black                    |
| -6      | Black / crushed shadows       |

## Recommended Exposure Practice

The LUT is designed around guidance shared by Z CAM regarding Z-Log2 exposure:

* Middle grey approximately 40 IRE
* Avoid significant underexposure
* Monitor skin exposure using false color and waveform tools
* Protect highlights while taking advantage of Z-Log2's available headroom

As with any monitoring tool, this LUT should be used alongside proper exposure practices and not as a replacement for waveform monitoring.

## Technical Notes

This LUT was developed using:

* Thatcher Freeman's reverse-engineered Z-Log2 transform
* Scene-linear stop calculations relative to 18% middle grey
* White-balance stability testing from approximately 2500K to 14000K
* Validation against exposure sweeps across multiple stop values

The LUT is intended purely for monitoring and exposure evaluation.

It is not intended as a display transform, viewing LUT, or final grading LUT.

## Disclaimer

This project is independent and is not affiliated with or endorsed by Z CAM, Panasonic, EL Zone, or Ed Lachman.

"EL Zone" is referenced only to describe the style and methodology of stop-based exposure visualization.

## Credits

Designed and developed by jobsanbiju.

Special thanks to Thatcher Freeman for his work reverse-engineering the Z-Log2 curve and making the transform publicly available.
