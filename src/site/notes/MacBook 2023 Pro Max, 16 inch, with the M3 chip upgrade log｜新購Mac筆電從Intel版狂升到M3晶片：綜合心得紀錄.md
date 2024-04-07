---
{"dg-publish":true,"permalink":"/mac-book-2023-pro-max-16-inch-with-the-m3-chip-upgrade-log-mac-intel-m3/","noteIcon":"2"}
---

I completed the 10-hour system-to-system transfer following Apple MacOS's onscreen guide after turning on the new laptop. This is a log of my findings. I really appreciate being given more than 40 days to decide whether to keep it or return.

經過十小時無線Wi-fi的系統和內容移植，新電腦可以用了，但一堆楣楣角角要實測。還好，新電腦因爲年底購入，享有長達40多天的退貨期（原本只有14天），可以測到元旦假期過後！
# Quick summary

- The apps that failed aren't exactly surprises. I expected extra costs in software upgrades or alternatives. 一些軟體崩壞了，並不意外。早預料會有額外的開銷。
- Great news regarding Loopback and Arctis Pro Wireless. My work depends so much on them. 最慶幸 Loopback 和 Arctis Pro Wireless 一切正常。吃飯的工具哩！
- Equally great news: a new version of Movavi screen recorder works. Tested.

---
# Todo

## Apple 27" Cinema Display with Mini DisplayPort adapter

# Tested

## The smooth transition

All data and many apps and programs appear to have been transferred over without a hitch. That's a big relief, especially on the data side. The rest of the note documents the exceptions.
### Zoom (video conferencing)

Works as expected. Can even share either of the dual screen after giving security permissions. The Cinema display's camera doesn't have pixellation or freezing as one Amazon user warned.
### Apple 27" Cinema Display with Thunderbolt adapter

Works after getting a thunderbolt to USB-C adapter.
## The manual adjustments or additions
### Loopback 音訊繞接軟體

- [x] One-time config
Requires following a detailed and clear official web guide to config permission settings accessible only through rebooting the Mac in a specific way. After the config, Loopback is working properly. Phew! This is one of my top priorities.
### Input methods 輸入法

Unexpectedly, specific input systems I had are lost after the transfer. I simply needed to reinstall Squirrel as my go-to Chinese input.
#### Squirrel/RIME/鼠鬚管

![Screen Shot 2023-11-22 at 04.36.15.png|200](/img/user/_attachments/_OB/Screen%20Shot%202023-11-22%20at%2004.36.15.png)

- [x] Re-install
Turns out the reason had to do with security, because RIME/Squirrel/鼠鬚管 is not from an Apple-approved developer. Makes sense. 
### The 8-port USB Type C hub

- [x] Ethernet
- [x] USB Type C port 1 (single one on side)
- [x] USB Type C port 2 (one of two on a side, closer to cable)
- [x] USB Type C port 3 (one of two on a side, away from cable)
- [ ] HDMI
- [ ] Card reader (wide)
- [ ] Card reader (narrow)
- [ ] Power port
### Anki

The older version of Anki doesn't work anymore. Luckily, Anki released a new version that works for Apple Silicon. After installing it, everything worked without needing to re-enable existing profiles.
## The ugly surprises

### Movavi Screen Recorder 桌面錄影軟體

Initially, appears to be working after re-entering the serial number from the original purchase. Except that after recording is started, it cannot be stopped and must be forced to quit. Seriously? The result was a bogus video file, almost zero byte, that couldn't be played. This is the older purchased version 11; it is dead on Apple Silicon.

Happily, I just installed a 7-day trial version of the new Movavi 24 (for 2024, I guess), and everything worked like before! It's just a matter of deciding whether I want to shell $73 to buy the lifetime version of the new screen recorder + editor. Comparing that price to $43 for just the screen recorder and for only one-year subscription, it's a steal.

![Screenshot 2023-11-23 at 19.22.56.png|300](/img/user/_attachments/_OB/Screenshot%202023-11-23%20at%2019.22.56.png)

(2023-11-25) I got an even better combo deal and pulled the trigger:

![Screenshot 2023-11-25 at 19.54.30.png|300](/img/user/_attachments/_OB/Screenshot%202023-11-25%20at%2019.54.30.png)
##### Argument for Movavi over QuickTime

Movavi can record dual screens as long as the area is a rectangle. This is better than QuickTime. Also, QuickTime is known to quietly quit recording midway without you knowing. That's murderous! Movavi has never done that. Other features:
- Ability to pause and resume recording. (QuickTime can't).
- Corner web cam with studio light, circular shape.
- Noise cancellation on the microphone.

- [ ] Alternative software
	- [x] Quicktime (free), only for screen recording.
	- [ ] ScreenFlow ($180 to buy)
	- [x] Movavi Screen Recorder 24
### Movavi Video Editor Plus 2020 and Movavi Video Editor 4

- Both stopped working.
- The programs start fine.
- Appear to work.
- Create result video.
	- Before installing Rosetta
		- Result videos don't play normally.
	- After installing Rosetta (through command-line)
		- Result videos seem normal. (right file size, took time to render file, etc.)
			- But freeze at first screen or is black throughout.

影片編輯軟體（同一系列的兩個版本）都GG了，澈底崩壞，無論是否裝了Rosetta。

[Video I followed to install Rosetta successfully](https://www.youtube.com/watch?v=hlG_6Qz1nTw)

- [ ] Find alternatives
	- [x] Movavi Video Editor 24
### Windows 10 VM can't be started. Confirmed dead.

### The CKlau USB 3.0 2-device sharing switch failed

雖然失望卻也在意料中。這個切換兩個電腦的USB 3.0介面完全無法使用了，我之前靠它切換如下的裝置：

- [x] 有線鍵盤（好在新鍵盤有兩種無線模式）
- Nuphy Air75 USB-A dongle doesn't work for both devices, only one (new one) ，扯！
- 無線滑鼠（目前暫用兩個滑鼠）
	- 誇張的是，滑鼠表面上可切換，但無法「按」，只是能看到移動的游標，有夠扯！
- 7個USB-A連接埠：目前這個介面智能直接插入M3的USB C連接埠，所以無法切換電腦
	- 耳機
	- 外接硬碟
	- 其他次要裝置

---
# The old faithful Mac 老當益壯的舊筆電

[[Mid-2014 MacBook Pro (Intel)｜2014年版MacBook Pro\|Mid-2014 MacBook Pro (Intel)｜2014年版MacBook Pro]]