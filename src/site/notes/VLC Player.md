---
{"dg-publish":true,"permalink":"/vlc-player/","noteIcon":"2"}
---

# Quick verdict: 4.5
# Pros

- Multiple platforms
- Downsampling or downsizing
- Conversion to other formats
- Speed control
- Playlist
# Cons

- Two (or multiple) audio channels
- Sharing of VLC Player playback on Zoom may result in blank video or stuttering
# Quirks
## On MacBook Pro Max M3

*(2023-11-29)* A technical "glitch" during [[EMSIG\|EMSIG]] led me to this discovery:

VLC Player has its own "audio" setting, in this case MacBook Pro Speakers, which may not match the system audio setting, in this case External Headphones (plugged in jack for the second laptop). If I am sharing VLC Player playback from the second computer, I need to remember to plug in the audio jack, and either
- choose "External Headphones" in both settings, or 
- choose "System Sound Output Device" for VLC Player, and "External Headphones" for System.

![vlc independent audio output on Mac M3 from system audio - Screenshot 2023-11-28 at 20.17.31.png|500](/img/user/_attachments/_OB/vlc%20independent%20audio%20output%20on%20Mac%20M3%20from%20system%20audio%20-%20Screenshot%202023-11-28%20at%2020.17.31.png)

# Applications

## Zoom screen sharing with sound - VLC Player playback

To allow Zoom participants hear the sound in VLC, make sure to set its audio device to "system sound output" as shown, or to set it explicitly (as mentioned above).

![Screenshot 2023-12-12 at 19.22.45.png](/img/user/_attachments/_OB/Screenshot%202023-12-12%20at%2019.22.45.png)

# Conversion (into audio, etc.) and downsampling (downsizing) of videos

This [blogpost: how to downsample a video with VLC](https://fabiomarroni.wordpress.com/2018/04/14/compress-video-with-vlc/) recommends the simple factor of 0.75.

I recommend the simple factor of 0.25 to get even better downsizing and still decent video clarity. It's rather amazing.
