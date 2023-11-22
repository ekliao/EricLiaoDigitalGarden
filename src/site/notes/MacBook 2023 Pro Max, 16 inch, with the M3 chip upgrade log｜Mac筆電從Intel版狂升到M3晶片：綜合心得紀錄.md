---
{"dg-publish":true,"permalink":"/mac-book-2023-pro-max-16-inch-with-the-m3-chip-upgrade-log-mac-intel-m3/","noteIcon":"2"}
---

Date-created:: 2023-11-20

I completed the 10-hour system-to-system transfer following Apple MacOS's onscreen guide after turning on the new laptop. This is a detailed log of experience.
# Quick summary

- The apps that failed aren't exactly surprises. I expected extra costs in software upgrades or alternatives. 一些軟體崩壞了，並不意外。早預料會有額外的開銷。
- Great news regarding Loopback and Arctis Pro Wireless. My work depends so much on them. 最慶幸Loopback和Arctis Pro Wireless一切正常。吃飯的工具哩！

---
# Todo

## Zoom (video conferencing)

# Tested

## The smooth transition

All data and many apps and programs appear to have been transferred over without a hitch. That's a big relief, especially on the data side. The rest of the note documents the exceptions.
## The manual adjustments or additions
### Loopback 音訊繞接軟體

- [x] One-time config
Requires following a detailed and clear official web guide to config permission settings accessible only through rebooting the Mac in a specific way. After the config, Loopback is working properly. Phew! This is one of my top priorities.
### Input methods 輸入法

Unexpectedly, specific input systems I had are lost after the transfer. I simply needed to reinstall Squirrel as my go-to Chinese input.
#### Squirrel/RIME/鼠鬚管

![Screen Shot 2023-11-22 at 04.36.15.png|200](/img/user/Screen%20Shot%202023-11-22%20at%2004.36.15.png)

- [x] Re-install
Turns out the reason had to do with security, because RIME/Squirrel/ㄎ is not from an Apple-approved developer. Makes sense. 
## The ugly surprises

### Movavi Screen Recorder 桌面錄影軟體

- Initially, appears to be working after re-entering the serial number from the original purchase.
- [x] Test to make sure
##### Verdict: 0/5 

- Sadly, anything "Movavi" (screen recorder, video editor) does not work on Apple Silicon.
- [ ] Find alternative software
	- [x] Quicktime (free), only for screen recording.
	- [ ] Screenflow ($180 to buy)
### Movavi Video Editor Plus 2020 and Movavi Video Editor 4

- Both stopped working; exported videos don't play normally. 影片編輯軟體（同一系列的兩個版本）都GG了，澈底崩壞。
- [ ] Find alternatives.
### Windows 10 VM can't be started. Confirmed dead.

### The USB-C 2-device switch hub failed

很失望。這個切換兩個電腦的 USB-C 介面的硬體完全無法使用了，我靠它切換如下的裝置：

- 有線鍵盤（好在新鍵盤有兩種無線模式）
	- Nuphy Air75 USB-A dongle doesn't work for both devices, only one (new one) - 扯！
- 無線滑鼠（目前暫用兩個滑鼠）
	- 誇張的是，滑鼠表面上可切換，但無法「按」，只是能看到移動的游標，有夠扯！
- 7個USB-A連接埠
	- 耳機
	- 外接硬碟
	- 其他次要裝置

