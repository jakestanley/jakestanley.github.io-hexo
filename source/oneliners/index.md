---
title: oneliners
date: 2019-07-31 17:00:13
---

# youtube-dl

Rip audio from a YouTube video into a sensible filename
```
youtube-dl --extract-audio --audio-format mp3 --output "%(title)s.%(ext)s" \
https://youtu.be/<video_key>
```

