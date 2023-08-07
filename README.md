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

Help page:

```
Usage: compress-flac [size] [speed]

Arguments:
    size:        Specify the output size. Options: big, medium, small, tiny
    speed:       Specify the encoding speed. Options: fast, medium, slow, superslow
    -m BITRATE SAMPLERATE SPEED
                 Manually enter the bitrate (kbps), samplerate (Hz), and speed (complexity)


              --- EXPLANATIONS: ---
Sample Rates:

    44100 Hz
        This is the standard sample rate used for CD-quality audio. It provides a good balance between audio quality and file size.
    48000 Hz
        Commonly used for high-quality audio, especially in professional audio production or broadcasting.
    22050 Hz
        Suitable for speech or low-quality audio recordings where file size is a concern.

Bitrates:

    64-96 kbps
        This range is suitable for low-quality audio, such as audiobooks, speech recordings, or voice-only content. It provides small file sizes but sacrifices some audio fidelity.
    128-192 kbps
        A commonly used range for general music recordings. It provides a good balance between audio quality and file size.
    192-256 kbps
        Suitable for higher-quality audio recordings, especially for music genres where audio details are important, such as classical or jazz.
    320 kbps
        This represents the highest quality available in Ogg Vorbis format. It provides excellent audio fidelity but results in larger file sizes.
```
