# Audio-Stuff
Some scripts, tools and tricks for Audio on Linux, maybe Android

### compress-flac

Flac files are nice, but way too big. ffmpeg is nice, but a bit complicated. This is a helper script for ffmpeg to convert flacs to ogg vorbis
- help page explains everything (and you can use `help`, `-h`, `--help` or `-help` how you like!)
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

Interesting: [View lost sound data with audacity](https://youtu.be/MmecPiKClHk), when doing lossy compression of Audio files

# Programs

### [EasyEffects](https://github.com/wwmm/easyeffects)
- [Presets](https://github.com/JackHack96/EasyEffects-Presets)



### JamesDSP
- [Linux](https://github.com/Audio4Linux/JDSP4Linux)
- [Linux Flatpak](https://flathub.org/apps/me.timschneeberger.jdsp4linux)
- [Android](https://github.com/ThePBone/RootlessJamesDSP) (may be buggy, as it needs quite a lot of tricks)
- [JamesDSP Library](https://github.com/james34602/JamesDSPManager)


## [Ardour](https://flathub.org/apps/org.ardour.Ardour)

You find Flatpak sound plugins as "runtimes", so not in GUI appstores:

```
flatpak search "LinuxAudio.Plugins"
flatpak install flathub -y A B C
```
There are multiple versions, use the latest if there are no compatibility issues. They are kept seperate because of that I guess.
