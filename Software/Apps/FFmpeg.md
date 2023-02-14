# FFmpeg

A [cross-platform solution](https://ffmpeg.org/) to record/convert audio and video.

---

## m4a > mp4

Find all m4a audio files in a folder and convert to mp4

```bash
find -name "*.m4a" -exec ffmpeg -i {} -acodec libmp3lame -ab 128k {}.mp4 \;
```

## mov > mp4

```bash
ffmpeg -i video.mov -vcodec h264 -acodec mp2 video.mp4
```

[Source](https://mrcoles.com/convert-mov-mp4-ffmpeg/)

## webm > mp4

```bash
ffmpeg -i video.webm video.mp4
```