Demonstration of a bug where webp images animate progressively slower over time in Safari browser on MacOS and iOS.

View webpage live at: https://catball.dev/bug_reports/animated_webp_bug/25_seconds.html

---

Tested on:

- MacOS 14.6.1
  - Safari 17.6
  - Safari Technology Preview 18.0
- iOS 17.6.1

---

Encoding options:

- 25_seconds.mov was recorded with Mac OS builtin screenshot tool.
- 25_seconds.gif was encoded with gifski.app from 25_seconds.mov at 24 FPS at lowest quality.
- 25_seconds.webp was encoded with ffmpeg from 25_seconds.mov at 24 FPS with a quality setting of 70.
  - `ffmpeg -i ~/Pictures/Screenshots/25_seconds.mov -vcodec libwebp -filter:v fps=fps=24 -lossless 0 -compression_level 3 -q:v 70 -loop 1 -preset text -an -vsync 0 ~/Pictures/Screenshots/25_seconds.webp`
