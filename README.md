Demonstration of a bug where webp images animate progressively slower over time in Safari browser on MacOS and iOS.

- 25_seconds.mov was recorded with Mac OS builtin screenshot tool.
- 25_seconds.gif was encoded with gifski.app from 25_seconds.mov at 24 FPS at lowest quality.
- 25_seconds.webp was encoded with ffmpeg from 25_seconds.mov at 24 FPS with a quality setting of 70.
  - `ffmpeg -i ~/Pictures/Screenshots/25_seconds.mov -vcodec libwebp -filter:v fps=fps=24 -lossless 0 -compression_level 3 -q:v 70 -loop 1 -preset text -an -vsync 0 ~/Pictures/Screenshots/25_seconds.webp`
