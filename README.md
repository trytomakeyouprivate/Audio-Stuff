# Audio-Stuff
Some scripts, tools and tricks for Audio on Linux, maybe Android

### compress-flac

Flac files are nice, but way too big. ffmpeg is nice, but a bit complicated. This is a helper script for ffmpeg to convert flacs to ogg vorbis
- help page explains everything (and you can use `help`, `-h`, `--help` or `-help` how you like!
- Predefined compression levels or manual mode for experts
- automatically finds and compresses all flac files in the current directory
- detects Hardware and uses all cores and GPU when possible
- detects cover image and uses it without compression
- silences ffmpeg output to its bare minimum, adds some more status notifications
- creates and information file about the compression and names the output folder informatively
- outputs a GUI notification once ready, useful for big compression tasks
- ...

have fun!

```
wget https://github.com/trytomakeyouprivate/Audio-Stuff/raw/main/compress-flac -P ~/.local/bin
chmod +x ~/.local/bin/compress-flac
```
