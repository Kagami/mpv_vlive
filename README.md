Watch videos from [vlive.tv](http://www.vlive.tv/) in [mpv](https://mpv.io/).

### DEPRECATED

Moving steps:

* [ ] Merge [HLS WebVTT patches](https://ffmpeg.org/pipermail/ffmpeg-devel/2016-December/203982.html) to FFmpeg
* [ ] Implement [vlive subtitles info parsing](https://github.com/rg3/youtube-dl/pull/8820) in youtube-dl
* [ ] Create [streamlink](https://github.com/streamlink/streamlink) vlive plugin

See [mpv-player/mpv#3087](https://github.com/mpv-player/mpv/issues/3087) for more info.

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
mkdir -p ~/.local/bin ~/.config/mpv/scripts
ln -s ~/mpv_vlive/vlive ~/.local/bin
ln -s ~/mpv_vlive/dump_vlive ~/.local/bin
ln -s ~/mpv_vlive/vlive.lua ~/.config/mpv/scripts
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
