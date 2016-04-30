Watch videos from [vlive.tv](http://www.vlive.tv/) in [mpv](https://mpv.io/).

### Why

* FFmpeg's HLS handler is slow
* mpv currently uses FFmpeg to display HLS
* youtube-dl currently uses FFmpeg to dump HLS
* Livestreamer's maintainer is inactive
* [WebVTT HLS patches](https://github.com/anssih/FFmpeg/commits/hls) for FFmpeg are stalled

### Install

```bash
sudo apt-get install youtube-dl livestreamer
git clone https://github.com/Kagami/mpv_vlive.git ~/mpv_vlive
mkdir -p ~/.local/bin ~/.mpv/scripts
ln -s ~/mpv_vlive/vlive ~/.local/bin
ln -s ~/mpv_vlive/dump_vlive ~/.local/bin
ln -s ~/mpv_vlive/vlive.lua ~/.mpv/scripts
```

### Usage

```bash
# Watch
vlive http://www.vlive.tv/video/1234

# Dump
dump_vlive 1234
```

### License

[CC0.](COPYING)
