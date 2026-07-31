# Hero Background Video Asset

Place the hero background video at:

- `videos/mfc-hero-background.mp4`

Recommended export settings:

- Codec: H.264
- Resolution: 1920x1080
- Framerate: 24 or 25 fps
- Duration: 8 to 14 seconds (seamless loop)
- Audio: none (remove audio track)
- Target size: 3 MB to 8 MB

Optional advanced setup:

- Add a second mobile clip and switch via media queries if desired.
- Add a poster image for slow connections.

Example ffmpeg command:

```bash
ffmpeg -i input.mov -an -c:v libx264 -profile:v high -pix_fmt yuv420p -movflags +faststart -vf "scale=1920:1080:force_original_aspect_ratio=increase,crop=1920:1080" -r 25 -crf 24 videos/mfc-hero-background.mp4
```
